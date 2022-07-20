# innerve_Demo
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>Registration form</title>
	<link rel="stylesheet" href="style.css">
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.15.4/css/all.css" 
    integrity="sha384-DyZ88mC6Up2uqS4h/KRgHuoeGwBcD4Ng9SiP4dIRy0EXTlnuz47vAwmeGwVChigm" 
    crossorigin="anonymous"/>
</head>
<body>
    <div class="container">
        <header>Registration form</header>
        <div class="bar">
            <div class="step">
                <p>Name</p>
                <div class="bullet">
                    <span>1</span>
                </div>
                <div class="check fas fa-check"></div>
            </div>
            <div class="step">
                <p>Contact</p>
                <div class="bullet">
                    <span>2</span>
                </div>
                <div class="check fas fa-check"></div>
            </div>
            <div class="step">
                <p>Submit</p>
                <div class="bullet">
                    <span>3</span>
                </div>
                <div class="check fas fa-check"></div>
            </div>
            
        </div>
        <div class="outer">
            <form>
                <div class="page slidepage">
                    <div class="title">
                        Personal Details:
                    </div>
                    <div class="field">
                        <div class="label">
                            First name
                        </div>
                        <input type="text">
                    </div>
                    <div class="field">
                        <div class="label">
                            Last name
                        </div>
                        <input type="text">
                    </div>
                    <div class="field nextBtn">
                        <button>Next</button>
                    </div>
                </div>

                <div class="page">
                    <div class="title">
                        Contact Details:
                    </div>
                    <div class="field">
                        <div class="label">
                            Email-Id
                        </div>
                        <input type="email">
                    </div>
                    <div class="field">
                        <div class="label">
                            Password
                        </div>
                        <input type="password">
                    </div>
                    
                    <div class="field btns">
                        <button class="prev-1 prev">Previous</button>
                        <button class="next-1 next">Next</button>
                    </div>
                </div>

                
                <div class="page">
                    <div class="title">Final submission:</div>
                    <div class="field">
                        <div class="label">
                            Confirm Password
                        </div>
                        <input type="password">
                    </div>
                    
                    <div class="field btns">
                        <button class="prev-2 prev">Previous</button>
                        <button class="submit next">Submit</button>
                    </div>
                </div>



            </form>
        </div>

    </div>
    <script>
        const slidePage=document.querySelector(".slidepage");
        const firstNextBtn=document.querySelector(".nextBtn");
        const prevBtnSec=document.querySelector(".prev-1");
        const nextBtnSec=document.querySelector(".next-1");
        const prevBtnThird=document.querySelector(".prev-2");
        const submitBtn=document.querySelector(".submit");
        const nextText=document.querySelectorAll(".step p");
        const nextCheck=document.querySelectorAll(".step .check");
        const bullet=document.querySelectorAll(".step .bullet");
        let max=3;
        let current=1;

        firstNextBtn.addEventListener("click",function(event){
            event.preventDefault();
            slidePage.style.marginLeft="-25%";
            bullet[current-1].classList.add("active");
            nextText[current-1].classList.add("active");
            nextCheck[current-1].classList.add("active");
            current +=1;
        });
        
    
        nextBtnSec.addEventListener("click",function(event){
            event.preventDefault();
            slidePage.style.marginLeft="-50%";
            bullet[current-1].classList.add("active");
            nextText[current-1].classList.add("active");
            nextCheck[current-1].classList.add("active");
            current +=1;
        });
        submitBtn.addEventListener("click",function(event){
            event.preventDefault();
            bullet[current-1].classList.add("active");
            nextText[current-1].classList.add("active");
            nextCheck[current-1].classList.add("active");
            current +=1;
            setTimeout(function(){
                alert("registered!");
                location.reload();
            },800);
        });
        prevBtnSec.addEventListener("click",function(event){
            event.preventDefault();
            slidePage.style.marginLeft="0%";
            bullet[current-2].classList.remove("active");
            nextText[current-2].classList.remove("active");
            nextCheck[current-2].classList.remove("active");
            current -=1;
        });
        prevBtnThird.addEventListener("click",function(event){
            event.preventDefault();
            slidePage.style.marginLeft="-25%";
            bullet[current-2].classList.remove("active");
            nextText[current-2].classList.remove("active");
            nextCheck[current-2].classList.remove("active");
            current -=1;
        });
        prevBtnThird.addEventListener("click",function(event){
            event.preventDefault();
            slidePage.style.marginLeft="-50%";
            bullet[current-2].classList.remove("active");
            nextText[current-2].classList.remove("active");
            nextCheck[current-2].classList.remove("active");
            current -=1;
        });
        

    

    </script>
</body>
</html>

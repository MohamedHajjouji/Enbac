<script>
    import logo from "$lib/images/logo.png"
    import bg from "$lib/images/man.jpg"


let formAppear = false

    function showForm(){
        formAppear = !formAppear
    }
</script>
<img src={bg} alt="" class="background-img"/>
{#if formAppear}
    <div class="form-container">
        <form action="https://api.web3forms.com/submit" method="POST">
            <input type="hidden" name="access_key" value="3150cab8-1ced-4fff-b200-63cf7145053a">
            <!-- svelte-ignore a11y_click_events_have_key_events -->
            <!-- svelte-ignore a11y_no_static_element_interactions -->
            <i class="fa-solid fa-xmark" on:click={showForm}></i>
            <h3>Send a Request</h3>
            <p>After sending a request. we will call you and discuss your needs and preferences</p>
            <input type="text" name="name" id="name" placeholder="First Name">
            <input type="text" name="name" id="name" placeholder="Last Name">
            <input type="email" name="email" id="email" placeholder="Email">
            <input type="tel" name="phone" id="phone" placeholder="Phone">
            <button type="submit">Send Request</button>
        </form>
    </div>
    {/if}
<header>
    <div class="logo"><img src={logo} alt=""></div>
    <nav>

           
    </nav>
<!--    <div class="lang-switch">
        En/Fr
    </div>-->
</header>

<main>
    
    
   
    

    <div class="intro">
        <h1>Prepare for Your English Bac Exam</h1>
        <p class="desc">Get weekly online classes that will make sure you are ready for the national bac exam </p>
        <button on:click={showForm}>Reserve Spot</button>
        <div class="contact">
            <div class="sub-contact">
                <i class="fa-regular fa-envelope"></i>
                <div class="contact-text">
                    <p class="text-title">Email</p>
                    <p class="text-desc">devmohamedhajjouji@gmail.com</p>
                </div>
            </div>
            <div class="sub-contact">
                <i class="fa-solid fa-headset"></i>
                <div class="contact-text">
                    <p class="text-title">Call us</p>
                    <p class="text-desc">+212772314000</p>
                </div>
            </div>
        </div>
    </div>
    <div class="offer">
        <h3 class="offer-type">Professional</h3>
        <p class="offer-desc">Ideal for individuals who need help prepare for the national bac exam</p>
        <div class="offer-price">
            <h1>100DH</h1>
            <p>/Month</p>
        </div>
        <div class="offer-features">
            <ul>
                <li><i class="fa-solid fa-check"></i>3 hours of online classes per week</li>
                <li><i class="fa-solid fa-check"></i>PDF documents for revision</li>
                <li><i class="fa-solid fa-check"></i>Revision for the exams</li>
                <li><i class="fa-solid fa-check"></i>Only in a group of up to 6 people</li>
            </ul>
        </div>
        <button class="offer-cta" on:click={showForm}>Get Started Now</button>
        
    </div>
</main>






<style>

   

:root{
        --size-multiplier: 1;
}

@media (max-width: 1100px) {
    :root{
        --size-multiplier: 0.8 ;
}}
@media (max-width: 950px) {
    :root{
        --size-multiplier: 0.7 ;
}
  }
  @media (max-width: 822px) {
    :root{
        --size-multiplier: 0.6 ;
}  }

@media (max-width: 700px) {
    :root{
        --size-multiplier: 0.7 ;
}
    
    main{
        flex-direction: column;
        width: 70%;
        align-self: flex-start;
     
     
     
        
       
        
    }
    
    .intro{
        min-width:100%;
        padding:0;
        
    }
    .offer{
        min-width: 100%;
    }
    .contact{
        flex-wrap: wrap;
    }

  }
  @media (max-width: 550px) {
    main{
        width: 90%;
    }  }


  @media (max-width: 425px) {
    :root{
        --size-multiplier: 0.55 ;
}}
  


    *{
        color: white;
        margin: 0;
        padding: 0;
        font-family: "Manrope", serif;
    }
    
    .background-img{
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        filter: brightness(20%);
        object-fit: cover;
        z-index: -1;

       
    }
  
    header{
        max-width: 1200px;
        padding: 0 calc(95px * var(--size-multiplier));
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: calc(114px * var(--size-multiplier));
        margin-right: calc(20px * var(--size-multiplier));
        width: 90%;

    }
    nav{
        display: flex;
        gap: calc(35px * var(--size-multiplier));
        
    }
    nav a{
        text-decoration: none;
        font-size: calc(18px * var(--size-multiplier));
    }
    .logo img{
        width: calc(196px * var(--size-multiplier));

        height: calc(40px * var(--size-multiplier));
        object-fit: cover;
    }
    .lang-switch{
        font-size: calc(20px * var(--size-multiplier));
    }
    main{
        align-items: center;
        max-width: 1200px;
        display: flex;
        justify-content: space-between;
        gap:calc(150px * var(--size-multiplier));
        
        padding: calc(70px * var(--size-multiplier))  ;
        
        

    }
    .intro{
        max-width:calc(600px * var(--size-multiplier));
        padding-top: calc(50px * var(--size-multiplier));
        
    }
    .intro i{
        font-size: calc(30px * var(--size-multiplier));
        color: white;
        width:calc(60px * var(--size-multiplier)) ;
        height: calc(60px * var(--size-multiplier));
        display: grid;
        place-items: center;
        border-radius: 150em;
        background-color: #405BFE;

    }
    .intro h1{
        font-size: calc(66px * var(--size-multiplier));
        line-height: calc(74px * var(--size-multiplier));
        padding: 0;
        margin: 0;
        margin-bottom: calc(30px * var(--size-multiplier));
    }
    .intro .desc{
        font-size: calc(22px * var(--size-multiplier));
        line-height: calc(32px * var(--size-multiplier));
        padding: 0;
        max-width: 600px;
        margin: 0;
        margin-bottom: calc(30px * var(--size-multiplier));
    }
    .intro button{
        margin-bottom: calc(67px * var(--size-multiplier)); 
    }
    .intro button, .offer button{
        padding: calc(15px * var(--size-multiplier)) calc(20px * var(--size-multiplier));
        font-size: calc(18px * var(--size-multiplier));
        background-color: #405BFE;
       
        border: 3px solid #405BFE;
        
    }
    .text-title{
        font-size: calc(20px * var(--size-multiplier));
    }
    .text-desc{
        font-size: calc(15px * var(--size-multiplier));
        color:#BCBCBC;
    }
    .offer button{
        padding: calc(11px * var(--size-multiplier)) 0;
        width: 100%;
        font-size: calc(16px * var(--size-multiplier));
    }
    .contact{
        display: flex;
        gap: calc(51px * var(--size-multiplier));
    
        
    }
    .sub-contact{
        display: flex;
        gap:calc(24px * var(--size-multiplier));
        align-items: center;
    }
     .contact-text{
        
    }
  

    .offer{
        background-color: rgba(24, 24, 24, 0.7);
        padding:calc(40px * var(--size-multiplier)) calc(24px * var(--size-multiplier)) calc(22px * var(--size-multiplier)) calc(24px * var(--size-multiplier));
        width: calc(396px * var(--size-multiplier));
        max-height: fit-content;
  
        
    }
    .offer-type{
        margin-bottom: calc(11px * var(--size-multiplier));
        font-size: calc(22px * var(--size-multiplier));
        font-weight: bold;
    }
    .offer-desc{
        font-size:calc(16px * var(--size-multiplier));
        color:#F7F8F9;
        margin-bottom: calc(25px * var(--size-multiplier));
        font-weight: 300;
    }
    .offer-price{
        display: flex;
        align-items: center;
        gap:9px;
        margin-bottom: calc(40px * var(--size-multiplier));

    }
    .offer-price h1{
        font-size: calc(52px * var(--size-multiplier));
    }
    .offer-price p{
        font-size: calc(16px * var(--size-multiplier));
        color:#F7F8F9;
        font-weight: 200;
    }
    li{
        list-style-type: none;
        font-size: calc(16px * var(--size-multiplier));
        margin-bottom:calc(15px * var(--size-multiplier));
        display: flex;
        align-items: center;
        gap: calc(17px * var(--size-multiplier));
    }
    ul{
        margin-bottom: calc(35px * var(--size-multiplier));
    }
    li i{
        width: calc(32px * var(--size-multiplier));
        height: calc(32px * var(--size-multiplier));
        border-radius: 150em;
        background-color: #E8EDFB;
        display: flex;
        justify-content: center;
        align-items: center;
        color: #173EAD;
    }
    button{
        cursor: pointer;
        border: none;

    }
    .form-container{
        width: 100dvw;
        height: 100vh;
        background-color: rgba(24, 24, 24, 0.7);
        position: fixed;
        display: flex;
        justify-content: center;
        align-items: center;
        z-index:110;
        
    }
    form{
       
        display: flex;
        flex-direction: column;
        gap: calc(20px * var(--size-multiplier));
        max-width: calc(400px * var(--size-multiplier));
        background-color: #1D2026;
        padding: calc(40px * var(--size-multiplier));
    }
    form i{
        align-self: flex-end;
        position: absolute;
        margin-top: calc(-10px * var(--size-multiplier));
        margin-right: calc(-10px * var(--size-multiplier));
        cursor: pointer;
    }
    form h3{
        font-size: calc(24px * var(--size-multiplier));
        margin-bottom: calc(12px * var(--size-multiplier));
        margin: 0;
        padding: 0;
    }
    form p{
        font-size: calc(16px * var(--size-multiplier));
        color: #BCBCBC;
    }
    input{
        padding: calc(10px * var(--size-multiplier));
        border: none;
        border-radius: calc(5px * var(--size-multiplier));
        font-size: calc(16px * var(--size-multiplier));
        background-color: #2B2F3A;
    }
    form button{
        padding: calc(16px * var(--size-multiplier)) 0;
        margin-top: calc(32px * var(--size-multiplier));
        background-color: #405BFE;
        font-size: calc(18px * var(--size-multiplier));
    }
    button{
        
        transition: 0.5s ease all;
       
    }
    button:hover{
        scale: 110%;
      
      
    }
    .sub-contact:hover{
        scale:110%;
    }
    *{
        transition: 0.5s ease all;
    }


</style>
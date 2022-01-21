# ONYX Electronics
Your home for tech products, web design, and free all access source code library.
!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <h1>ONYX Website</h1>
    <link rel="stylesheet" href="styles.css" />
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.15.4/css/all.css" integrity="sha384-DyZ88mC6Up2uqS4h/KRgHuoeGwBcD4Ng9SiP4dIRy0EXTlnuz47vAwmeGwVChigm" crossorigin="anonymous"/>
</head>
<body>
  <nav class="navbar">
      <div class="navbar__container">
          <a href="/" id="navbar__logo">ONYX</a>
          <div class="navbar__toggle" id="mobile-menu">
              <span class="bar"></span>
              <span class="bar"></span>
              <span class="bar"></span>
        </div> 
        <ul class="navbar__menu">
            <li class="navbar__item">
                <a href="/" class="navbar__links">Home</a>
            </li>
            <li class="navbar__item">
                <a href="/tech.html" class="navbar__links">Tech</a>
            </li>
            <li class="navbar__item">
                <a href="/" class="navbar__links">Products</a>
            </li>
            <li class="navbar__btn">
                <a href="/" class="button">Sign Up</a></li>    
        </ul>
    </div>
</nav>

<!-- Hero Section -->
<div class="hero" id="home">
    <div class="hero__container">
    <h1 class="hero__heading">Create with <span>ONYX</span></h1>
    <p class="hero__description">Unlimited Possibilities</p>
    <button class="main__btn"><a href="#">Explore</a></button>
    </div>
</div>

Skip to content
Pull requests
Issues
Marketplace
Explore
@SubsJoneZ
SubsJoneZ /
ONYX
Public

Code
Issues 1
Pull requests
Actions
Projects
Wiki
Security
Insights

    Settings

ONYX/IMKO Website/styles.css
@SubsJoneZ
SubsJoneZ Add files via upload
Latest commit df2fc07 24 days ago
History
1 contributor
684 lines (591 sloc) 15.1 KB
* {
    box-sizing: border-box;
    margin: 0;
    Padding: 0;
    font-family: 'Kumbh Sans', sans-serif;
}

.navbar {
    background: #131313;
    height: 80px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 1.2rem;
    position: sticky;
    top: 0;
    z-index: 999;
}

.navbar__container {
    display: flex;
    justify-content: space-between;
    height: 80px;
    z-index: 1;
    width: 100%;
    max-width: 1300px;
    margin: 0 auto;
    padding: 0 50px;
}

#navbar__logo {
    background: #403B4A;  /* fallback for old browsers */
background: -webkit-linear-gradient(to right, #E7E9BB, #403B4A);  /* Chrome 10-25, Safari 5.1-6 */
background: linear-gradient(to right, #E7E9BB, #403B4A); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
    display: flex;
    align-items: center;
    cursor: pointer;
    text-decoration: none;
    font-size: 50px;
}

.fa-gem {
    margin-right: 0.5rem;
}

.navbar__menu {
    display: flex;
    align-items: center;
    list-style: none;
}

.navbar__item {
    height: 80px;
}

.navbar__links {
    color: #fff;
    display: flex;
    align-items: center;
    justify-content: center;
    text-decoration: none;
    padding: 0 1rem; 
    height: 100%;
    transition: all 0.3s ease;
}

.navbar__btn {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0 1rem;
    width: 100%;
}

.button {
    display: flex;
    justify-content: center;
    align-items: center;
    text-decoration: none;
    padding: 10px 20px;
    height: 100%;
    width: 100%;
    border: none;
    outline: none;
    border-radius: 4px;
    background: #833ab4;  /* fallback for old browsers */
background: -webkit-linear-gradient(to right, #fcb045, #fd1d1d, #833ab4);  /* Chrome 10-25, Safari 5.1-6 */
background: linear-gradient(to right, #fcb045, #fd1d1d, #833ab4); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
    color: #fff;
    transition: all 0.3s ease;
}

.navbar__links:hover {
    color: #833ab4;
    transition: all 0.3s ease;
}

.button:hover {
    background: #673AB7;  /* fallback for old browsers */
background: -webkit-linear-gradient(to right, #512DA8, #673AB7);  /* Chrome 10-25, Safari 5.1-6 */
background: linear-gradient(to right, #512DA8, #673AB7); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
transition: all 0.3s ease;
}

@media screen and (max-width: 960px) {
    .navbar__container {
        display: flex;
        justify-content: space-between;
        height: 80px;
        z-index: 1;
        width: 100%;
        max-width: 1300px;
        padding: 0;
    }
    
    .navbar__menu {
        display: grid;
        grid-template-columns: auto;
        margin: 0;
        width: 100%;
        position: absolute; 
        /* top: -1000px; */
        opacity: 1;
        transition: all 0.5s ease;
        z-index: -1;
    }

    .navbar__menu.active {
        background: #131313;
        top: 100%;
        opacity: 1;
        transition: all 0.5s ease;
        z-index: 99;
        height: 60vh;
        font-size: 1.6rem;
    }

    #navbar__logo {
        padding-left: 25px;
    }

    .navbar__toggle .bar {
        width: 25%;
        height: 3px;
        margin: 5px auto;
        transition: all 0.3s ease-in-out;
        background: #fff;
    }

    .navbar__item {
        width: 100%;
    }

    .navbar__links {
        text-align: center;
        padding: 2rem;
        width: 100%;
        display: table;
    }

    .navbar__btn {
        padding-bottom: 2rem;
    }

    .button {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 80%;
        height: 80px;
        margin: 0;
        background: #833ab4;  /* fallback for old browsers */
background: -webkit-linear-gradient(to right, #fcb045, #fd1d1d, #833ab4);  /* Chrome 10-25, Safari 5.1-6 */
background: linear-gradient(to right, #fcb045, #fd1d1d, #833ab4); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
    }

    #mobile-menu {
        position: absolute;
        top: 20%;
        right: 5%;
        transform: translate(5%, 20%);
    }

    .navbar__toggle .bar {
        display: block;
        cursor: pointer;
    }

    #mobile-menu.is-active .bar:nth-child(2) {
        opacity: 0;     
    }

    #mobile-menu.is-active .bar:nth-child(1) {
        transform: translateY(8px) rotate(45deg);
    }

    #mobile-menu.is-active .bar:nth-child(3) {
        transform: translateY(-8px) rotate(-45deg);
    }
}

/* Hero Section */
.hero {
    background: #000000;
    background: linear-gradient(to right. #161616, #000000);
    padding: 200px 0;
}

.hero__container {
    display: flex;
    flex-derection: column;
    justify-content: center;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
    height: 90%;
    text-align: center;
    padding: 30px;
}

.hero__heading {
    font-size: 100px;
    margin-bottom: 24px;
    color: #fff;
}

.hero__heading span {
    background: #833ab4;  /* fallback for old browsers */
    background: -webkit-linear-gradient(to right, #fcb045, #fd1d1d, #833ab4);  /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(to right, #fcb045, #fd1d1d, #833ab4); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -mo-text-fill-color: transparent;
}

.hero__description {
    font-size: 60px;
    background: #da22ff;
    background: -webkit-linear-gradient(
        to right,
        #9114ff,
        #da22ff
    );
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
}

.highlight {
    border-bottom: 4px solid rgb(132, 0, 255);
}

@media screen and (max-width: 768px) {
    .hero__heading {
        font-size: 60px;
    }

    .hero__description {
        font-size: 40px;
    }
}

/* About Section */
.main {
    background-color: #131313;
    padding: 10rem 0;
}

.main__container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
    height: 90%;
    z-index: 1;
    width: 100%;
    max-width: 1300px;
    padding: 0 50px;
}

.main__content {
    color: #fff;
    width: 100%;
}

.main__content h1 {
    font-size: 2rem;
    background-color: #fe3b6f;  /* fallback for old browsers */
    background-image: linear-gradient(to top, #ff0844 0%, #ed1a52 100%); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
    text-transform: uppercase;
    margin-bottom: 32px;
}

.main__content h2 {
    font-size: 4rem;
    background: #ff8177;
    background: -webkit-linear-gradient(
        to right,
        #9114ff,
        #da22ff
    );
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent; 
}

.main__content p {
    margin-top: 1rem;
    font-size: 2rem;
    font-weight: 700;
}

.main__btn {
    font-size: 1.8rem;
    background: #833ab4;  /* fallback for old browsers */
    background: -webkit-linear-gradient(to right, #fcb045, #fd1d1d, #833ab4);  /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(to right, #fcb045, #fd1d1d, #833ab4); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
    padding: 20px 60px;
    border: none;
    border-radius: 4px;
    margin-top: 2rem;
    cursor: pointer;
    position: relative;
    transition: all 0.35s;
    outline: none;
}

.main__btn a {
    position: relative;
    z-index: 2;
    color: #fff;
    text-decoration: none;
}

.main__btn:after {
    position: absolute;
    content: '';
    top: 0;
    left: 0;
    width: 0;
    height: 100%;
    background: #833ab4;
    transition: all 0.35s;
    border-radius: 4px;
}

.main__btn:hover {
    color: #fff;
}

.main__btn:hover:after {
    width: 100%;
}

.main__img--container {
    text-align: center;
}

.main__img--card {
    margin: 10px;
    height: 500px;
    width: 500px;
    border-radius: 4px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    color: #fff;
    background-image: linear-gradient(to right, #00dbde 0%, #fc00ff 100%);
}

.fa-layer-group,
.fa-users {
    font-size: 14rem;
}

#card-2 {
    background: #ff512f;  /* fallback for old browsers */
    background: -webkit-linear-gradient(to right, #fcb045, #dd2476, #ff512f);  /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(to right, #dd2476, #ff512f); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}

/* Mobile Responsive */
@media screen and (max-width: 1100px) {
    .main__container {
        display: grid;
        grid-template-columns: 1fr;
        align-items: center;
        justify-content: center;
        width: 100%;
        margin: 0 auto;
        height: 90%; 
    }

    .main__img--container {
        display: flex;
        justify-content: center;
    }

    .main__img--card {
        height: 425px;
        width: 425px;
    }

    .main__content {
        text-align: center;
        margin-bottom: 4rem;
    }

    .main__content h1 {
        font-size: 2.5rem;
        margin-top: 2rem;
    }

    .main__content h2 {
        font-size: 3rem;
    }

    .main__content p {
        margin-top: 1rem;
        font-size: 1.5rem;
    }
}

@media screen and (max-width: 480px) {
    .main__img--card {
        width: 250px;
        height: 250px;
    }

    .fa-users, .fa-layer-group {
        font-size: 4rem;
    }

    .main__content h1 {
        font-size: 2rem;
        margin-top: 3rem;
    }

    .main__content h2 {
        font-size: 2rem;
    }

    .main__content p {
        margin-top: 2rem;
    }

    .main.btn {
        padding: 12px 36px;
        margin: 2.5rem 0;
    }
}

/* Services Section */
.services {
    background: #131313;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100%;
    padding: 10rem 0;
}

.services h1 {
    background: #403B4A;  /* fallback for old browsers */
    background: -webkit-linear-gradient(to right, #E7E9BB, #403B4A);  /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(to right, #E7E9BB, #403B4A); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
        -webkit-background-clip: text;
        -moz-background-clip: text;
        -webkit-text-fill-color: transparent;
        -moz-text-fill-color: transparent;
        margin-bottom: 5rem;
        font-size: 2.5rem;
}

.services__wrapper {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    grid-template-rows: 1fr;
}

.services__card {
    margin: 10px;
    height: 425px;
    width: 300px;
    border-radius: 4px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    color: #fff;
    background-image: linear-gradient(to right, #00dbde 0%,#fc00ff 100%);
    transition: 0.3s ease-in;
}

.services__card:nth-child(2) {
    background: #1FA2FF;  /* fallback for old browsers */
background: -webkit-linear-gradient(to right, #A6FFCB, #12D8FA, #1FA2FF);  /* Chrome 10-25, Safari 5.1-6 */
background: linear-gradient(to right, #A6FFCB, #12D8FA, #1FA2FF); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}
.services__card:nth-child(3) {
    background: #360033;  /* fallback for old browsers */
    background: -webkit-linear-gradient(to right, #0b8793, #360033);  /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(to right, #0b8793, #360033); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}

.services__card h2 {
    text-align: center;
}

.services__card p {
    text-align: center;
    margin-top: 24px;
    font-size: 20px;
}

.services__btn {
    display: flex;
    justify-content: center;
    margin-top: 16px;
}

.services__card button {
    color: #fff;
    padding: 14px 24px;
    border: none;
    outline: none;
    border-radius: 4px;
    background: #131313;
    font-size: 1rem;
}

.services__card button:hover {
    cursor: pointer;
}

.services__card:hover {
    transform: scale(1.075);
    transition: 0.3s ease-in;
    cursor: pointer;
}

@media screen and (max-width: 1300px) {
    .services__wrapper {
        grid-template-columns: 1fr 1fr;
    }
}

@media screen and (max-width: 768px) {
    .services__wrapper {
        grid-template-columns: 1fr;
    }
}

/* Footer CSS */
.footer__container {
    background-color: #131313;
    padding: 5rem 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

#footer__logo {
    color: #fff;
    display: flex;
    align-items: center;
    cursor: pointer;
    text-decoration: none;
    font-size: 2rem;
}

.footer__links {
    width: 100%;
    max-width: 1000px;
    display: flex;
    justify-content: center;
}

.footer__link--wrapper {
    display: flex;
}

.footer__link--items {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin: 16px;
    text-align: left;
    width: 160px;
    box-sizing: border-box;
}

.footer__link--items h2 {
    margin-bottom: 16px;
    color: #fff;
}

.footer__link--items a {
    color: #fff;
    text-decoration: none;
    margin-bottom: 0.5rem;
}

.footer__link--items a:hover {
    color: #e9e9e9;
    transition: 0.3 ease-out;
}

.social__icon--link {
    color: #fff;
    font-size: 24px;
}

.social__media {
    max-width: 1000px;
    width: 100%;
}

.social__media--wrap {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 90%;
    max-width: 1000px;
    margin: 40px auto 0 auto;
}

.social__icons {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 240px;
}

.website__rights {
    color: #fff;
}

@media screen and (max-width: 820px) {
    .footer__links {
        padding-top: 2rem;
    }

    #footer__logo {
        margin-bottom: 2rem;
    }

    .website__rights {
        margin-bottom: 2rem;
    }

    .footer__link--wrapper {
        flex-direction: column;
    }

    .social__media--wrap {
        flex-direction: column;
    }
}

@media screen and (max-width: 480px) {
    .footer__link--items {
        margin: 0;
        padding: 10px;
        width: 100%;
    }
}

    © 2022 GitHub, Inc.

    Terms
    Privacy
    Security
    Status
    Docs
    Contact GitHub
    Pricing
    API
    Training
    Blog
    About

Loading complete

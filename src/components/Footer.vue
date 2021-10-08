<template>
    <footer>
        <div class="container">
            <div class="row text-white">
                <div class="col-6 col-md logo-footer">
                    <img class="img-fluid" src="../assets/img/footer-logo-1.png" alt="logo iAcademy">
                    <ul>
                        <li>Providing Life Changing </li>
                        <li>experiences Through </li>
                        <li>Education. Class That Fit Your </li>
                        <li>Busy Life. Closer to Home </li>
                    </ul>
                    <div>
                        <i class="fas fa-phone-alt"></i>
                        <span>Tel 1-677-124-44227</span>
                    </div>
                    <div>
                        <i class="far fa-clock"></i>
                        <span>Mon - Sat 8.00 - 18.00</span>
                    </div>
                </div>
                <div class="col-6 col-md">
                    <h2>{{ FooterElement[0].popular.title }}</h2>
                    <ul>
                        <li v-for="(course, index) in FooterElement[0].popular" :key="index">
                            <h6>{{ course.type }}</h6>
                            <p>{{ course.name }}</p>
                        </li>
                    </ul>
                </div>
                <div class="col-12 col-md">
                    <h2>Support</h2>
                    <ul>
                        <li>
                            <a href="#">
                                User dashboard
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Contact us
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                FAQ
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Course offer
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                Events
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="col-12 col-md">
                    <h2>Flexible Learning</h2>
                    <ul>
                        <li>
                            <img class="img-fluid" src="../assets/img/footer-img-1.png" alt="">
                        </li>
                    </ul>
                </div>
                <hr>

                <div class="col">
                    <div class="sub-footer">
                        Copyright 2017 &copy;Mikado Themes
                    </div>
                </div>
                <div class="col-12 col-md-6">
                    <div class="social sub-footer">
                        <div>Call +44 300 303 0266</div>
                        <div>Follow Us</div>
                        <div>
                            <a href="https://twitter.com/?lang=it">
                                <i class="fab fa-twitter"></i>
                            </a>
                        </div>
                        <div>
                            <a href="https://www.instagram.com/">
                                <i class="fab fa-instagram"></i>
                            </a>
                        </div>
                        <div>
                            <a href="https://it-it.facebook.com/">
                                <i class="fab fa-facebook-f"></i>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>

    </footer>
</template>

<script>
import FooterElement from '../data/FooterElement.json'

export default {
    name: "footer",
    data(){
        return{
            FooterElement
        }
    },
}
</script>

<style lang="scss">
@import '../style/general.scss';
@import '../style/color.scss';

footer{
    background-color: #222222;
    padding-top: 100px;

    h2, h6{
        font-family: $primaryFont;
    }

    h2{
        font-size: 1.7rem;
    }

    h6{
        font-size: 1.1rem;
    }

    ul{
        list-style: none;
        padding-top: 35px;
        padding-left: 0;
    }
    
    .col-12, .col-md-3{
        padding-bottom: 70px;
    }

    li{
        margin-bottom: 15px;
    }

    a{
        text-decoration: none;
        color: $whiteColor;

        &:hover{
            color: $whiteColor;
            text-decoration: underline;
        }
    }
    
    hr{
        border: 1px solid #414141;
    }

    .sub-footer{
        color: #949494;
        padding: 20px 0;
    }

    .social{
        display: flex;
        justify-content: space-between;
        text-transform: uppercase;
    }

    .fab{
        color: #959595;
        &:hover{
            color: $whiteColor;
        }
    }
}

.logo-footer{
    img{
        max-height: 35px;
    }

    ul li{
        margin-bottom: 3px;
    }

    li:last-child{
        margin-bottom: 25px;
    }

    .fas{
        margin-bottom: 25px;
    }

    span{
        padding-left: 15px;
    }
}




</style>
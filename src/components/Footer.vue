<template>
    <footer>
        <div class="container">
            <div class="row text-white">
                <div class="col-12 col-md-3 logo-footer">
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
                <div class="col-12 col-md-3">
                    <h2>{{ FooterElement[0].popular.title }}</h2>
                    <ul>
                        <li v-for="(course, index) in FooterElement[0].popular" :key="index">
                            <h6>{{ course.type }}</h6>
                            <p>{{ course.name }}</p>
                        </li>
                    </ul>
                </div>
                <div class="col-12 col-md-2">
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
                <div class="col-12 sub-footer">
                    <div class="d-flex justify-content-between">
                        <div>
                            Copyright 2017 &copy;Mikado Themes
                        </div>
                        <div class="social">
                            <div>Call +44 300 303 0266</div>
                            <div>Follow Us</div>
                            <div>
                                <i class="fab fa-twitter"></i>
                            </div>
                            <div>
                                <i class="fab fa-instagram"></i>
                            </div>
                            <div>
                                <i class="fab fa-facebook-f"></i>
                            </div>
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

    created(){
        console.log(this.FooterElement[0].popular);
    }
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

        .social{
            width: 35%;
            display: flex;
            justify-content: space-between;
            text-transform: uppercase;
        }
    }
}

.logo-footer{
    img{
        height: 38px;
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
<template>
    <footer>
        <div class="container">
            <div class="row text-white">
                <div class="col-12 col-md-3 logo-footer">
                    <img class="img-fluid" src="../assets/img/footer-logo-1.png" alt="logo iAcademy">
                    <ul>
                        <li>text</li>
                        <li>text</li>
                        <li>text</li>
                        <li>text</li>
                    </ul>
                    <div>
                        <i class="fas fa-phone-alt"></i>
                        <span>Tel</span>
                    </div>
                    <div>
                        <i class="far fa-clock"></i>
                        <span>ora</span>
                    </div>
                </div>
                <div class="col-12 col-md-3">
                    <h2>Popular Courses</h2>
                    <ul>
                        <li>
                            <h6>Engh</h6>
                            <p>Mar</p>
                        </li>
                        <li>
                            <h6>Social</h6>
                            <p>David</p>
                        </li>
                        <li>
                            <h6>Spani</h6>
                            <p>Jennie</p>
                        </li>
                    </ul>
                </div>
                <div class="col-12 col-md-3">
                    <h2>Support</h2>
                    <ul>
                        <li>User</li>
                        <li>Con</li>
                        <li>Faq</li>
                        <li>Course</li>
                        <li>Event</li>
                    </ul>
                </div>
                <div class="col-12 col-md-3">
                    <h2>Flex</h2>
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
export default {

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
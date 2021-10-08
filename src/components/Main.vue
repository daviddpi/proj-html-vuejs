<template>
    <main>
        <div class="container">
            <div class="row d-flex g-3 row-icon">
                <IconCard v-for="(icon, index) in ElementIconCard" :key="index" :src="ElementIconCard[index].src" 
                :alt="ElementIconCard[index].alt" :text="ElementIconCard[index].text"/>
            </div>

            <!-- sezione trust name -->
            <div class="row trusted-name-section">
                <div class="col-12">
                    <h1>The Trusted Name <br>for In-Home Tutoring.</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat totam facere sapiente nobis commodi eius modi harum labore dolorem assumenda aspernatur rerum hic eaque saepe recusandae, odio error? Ad, odio.</p>
                    <a href="#">Learn More</a>
                    <img class="img-fluid" src="../assets/img/h5-img-1.jpg" alt="Immagine di riferimento ">
                </div>
            </div>

            <!-- sezione empowering -->
            <div class="row empowering-section">
                <div class="col-12 col-md-6 d-flex justify-content-center align-items-center">
                    <img class="img-fluid" src="../assets/img/h8-slide-1-img.png" alt="Immagine della terra">
                </div>

                <div class="col-12 col-md-6 text-empowering">
                    <h2>Empowering <br>Children To Reach<br> Their Potential. </h2>
                    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tenetur excepturi omnis dicta aut labore itaque laudantium, aliquam laboriosam mollitia tempora exercitationem earum repellendus aspernatur? Dicta itaque quos necessitatibus nulla atque.</p>
                    <div class="d-flex number-user-event">
                        <div>
                            <h2>168</h2>
                            <h6>User Stories</h6>
                        </div>
                        <div>
                            <h2>347</h2>
                            <h6>Events</h6>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- sezione world-student-text  -->
        <div class="container-world-section">
            <div class="bg-world">
                <div class="container">
                    <div class="row">
                        <div class="col-12 d-flex align-items-center justify-content-center text-world-student">
                            <StudentExperience :arrayInfo="StudentExperienceInfo"/>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- tab section -->
        <div class="container">
            <Tabs :tabElement="TabsElements" :tabsInfo="TabsInfoElements"/>
        </div>

        <hr>

        <div class="bg-courses-pricing">
   
            <!-- popular courses section -->
            <div class="container container-popular-courses">
                <BoxCourses :arrayCourses="ElementBoxCourses"/>
            </div>

            <hr>

            <!-- plans section -->
            <div class="container">
                <div class="row plans-section">
                    <div class="col-12 text-center">
                        <h1>Pricing Plans</h1>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur aspernatur, saepe cum deserunt vero eius.</p>
                    </div>
                    <div class="col-12">
                        <div class="svg-icon">
                            <img id="icon-circle-svg" src="../assets/svg/svg-0.svg">
                            <img id="cart" src="../assets/svg/svg-2.svg">
                        </div>
                        <table id="table-plans">
                            <!-- Prezzi abbonamenti -->
                            <tr>
                                <th><h4>Save up to 40% by paying weekly</h4></th>
                                <th class="price-plans">
                                    <img class="img-fluid" src="../assets/img/h5-custom-icon-7.png" alt="immagine di una lampadina">
                                    <h4>Standard <br>$12</h4>
                                </th>
                                <th class="price-plans">
                                    <img class="img-fluid" src="../assets/img/h5-custom-icon-7.png" alt="immagine di una lampadina">
                                    <h4>Standard <br>$12</h4>
                                </th>
                                <th class="price-plans">
                                    <img class="img-fluid" src="../assets/img/h5-custom-icon-7.png" alt="immagine di una lampadina">
                                    <h4>Standard <br>$12</h4>
                                </th>
                            </tr>

                            <tr>
                                <td>Number of Courses</td>
                                <td>2</td>
                                <td>2</td>
                                <td>2</td>
                            </tr>
                            <tr>
                                <td>Time</td>
                                <td>15 days</td>
                                <td>15 days</td>
                                <td>15 days</td>
                            </tr>
                            <tr>
                                <td>Web Designing</td>
                                <td>&check;</td>
                                <td>&check;</td>
                                <td>&check;</td>

                            </tr>
                            <tr>
                                <td>Human-Centered Design</td>
                                <td>&check;</td>
                                <td>&check;</td>
                                <td>&check;</td>

                            </tr>
                            <tr>
                                <td>Basic Marketing</td>
                                <td>&cross;</td>
                                <td>&cross;</td>
                                <td>&cross;</td>
                            </tr>
                            <tr>
                                <td>Python for Everybody</td>
                                <td>&cross;</td>
                                <td>&cross;</td>
                                <td>&cross;</td>
                            </tr>
                            <tr>
                                <td>Android Developer</td>
                                <td>&cross;</td>
                                <td>&cross;</td>
                                <td>&cross;</td>
                            </tr>
                            <tr>
                                <td>Business English</td>
                                <td>&cross;</td>
                                <td>&cross;</td>
                                <td>&cross;</td>
                            </tr>
                            <tr>
                                <td></td>
                                <td>
                                    <button class="mybtn btn-table">get it now</button>
                                </td>
                                <td>
                                    <button class="mybtn">get it now</button>
                                </td>
                                <td>
                                    <button class="mybtn btn-table">get it now</button>
                                </td>
                            </tr>
                        </table>
                    </div>
                </div>
            </div>

        </div>

        
        <!-- bagde che ritorna il alto la pagina -->
        <div class="turn-up">
            <a href="#logo-header">
                <div><i class="fas fa-chevron-up"></i></div>
                <div>Top</div>
            </a>
        </div>
    </main>
</template>

<script>
import IconCard from './IconCard.vue'
import ElementIconCard from '../data/ElementIconCard.json'
import StudentExperience from './StudentExperience.vue'
import StudentExperienceInfo from '../data/StudentExperienceInfo.json'
import Tabs from './Tabs.vue'
import TabsElements from '../data/TabsElements.json'
import TabsInfoElements from '../data/TabsInfoElements.json'
import BoxCourses from './BoxCourses.vue'
import ElementBoxCourses from '../data/ElementBoxCourses.json'

export default {
    name: "Main",

    components: {
        IconCard,
        StudentExperience,
        Tabs,
        BoxCourses
    },

    data(){
        return{
            ElementIconCard,
            StudentExperienceInfo,
            TabsElements,
            TabsInfoElements,
            ElementBoxCourses
        }
    }
}
</script>

<style lang="scss">
@import '../style/general.scss';
@import '../style/color.scss';

main{
    position: relative;

    hr{
        margin-bottom: 100px;
        border: 1px solid #ebebeb;
    }
}



.row-icon{
    margin-bottom: 150px;
}

.trusted-name-section{
    margin-bottom: 150px;
    h1{
        font-family: $primaryFont;
        font-weight: 700;
    }

    p{
        margin-bottom: 20px;
    }

    a{
        text-decoration: none;
        text-transform: uppercase;
        color: $backgroundPrimary;
    }
}

.empowering-section{

    margin-bottom: 50px;

    img{
        width: 50%;
        margin-bottom: 50px ;
    }

    .text-empowering{
        width: 40%;

        h2{
            font-family: $primaryFont;
            font-weight: 600;
            margin-bottom: 20px;
        }
    }

    .number-user-event{
        font-family: $primaryFont;
        font-weight: 600;
        color: $backgroundPrimary;
        display: flex;
        width: 50%;
        justify-content: space-between;

        h2{
            margin-bottom: 5px;
        }
    }
    
}


.container-world-section{
    width: 100%;
    height: 530px;
    margin-bottom: 120px;

    .bg-world{
        background-image: url("../assets/img/h5-parallax-img-1.png");
        background-size: 200%;
        background-position: top 10% right 50%;
        width: 100%;
        height: 100%;
    }

    .container{
        height: 100%;

        .row{
            height: 100%;
            
            .text-world-student{
                height: 100%;
                color: $whiteColor;
            }
        }
    }
    
}

.container-popular-courses{
    position: relative;
    margin-bottom: 180px;

}

.bg-courses-pricing{
    height: 100%;
    width: 100%;
    background-image: url("../assets/img/page-background-img.png");
    background-size: cover;
}

.plans-section{

    position: relative;

    .svg-icon{
        position: absolute;
        top: 300px;
        right: -8.5px;
        transform: translate(50%);
        img{
            display: block;
            height: 40px;
            width: 40px;

            &:hover{
                cursor: pointer;
            }
        }

        #icon-circle-svg{
            background-color: #ee2852;
            padding: 2.5px;
            margin-bottom: 7px;
        }

        #cart{
            padding: 5px;
            background-color: $whiteColor;
        }
    }

    h1{
        font-family: $primaryFont;
    }
    p{
        margin-bottom: 100px;
    }

    #table-plans{
        margin: 0 auto;
    }

    #table-plans td, #table-plans th {
        border: 1px solid #ddd;
        padding: 8px;
    }

    #table-plans{

        th{
            width: calc(100% / 4);
            background-color: $whiteColor;
            border-top: 5px solid #d6f2ff;
            padding: 15px;
            font-family: $primaryFont;
        }

        tr:last-child{
            td{
                background-color: #f7fdff;

            }

            td:first-child{
                border-left: none;
                border-bottom: none;
            }
        }

        td{
            height: 60px;
            background-color: $whiteColor;
        }

        td:first-child{
            font-family: $primaryFont;
            padding-left: 20px;
        }

        td:not(:first-child){
            text-align: center;
        }

        .price-plans{
            background-color: #f7fdff;
            text-align: center;
        }

        .btn-table{
            background-color: $whiteColor;
            color: #808080;
            border: 1px solid #eaebeb;
        }

    }

    
}

//css tasto torna alla navbar
.turn-up{
    position: fixed;
    bottom: 0;
    right: 0;
    background-color: $backgroundPrimary;
    text-transform: uppercase;
    text-align: center;
    padding: 3px 8px;
    
    a{
        text-decoration: none;
        color: $whiteColor;
        font-size: 0.8rem;

        &:hover{
            color: $whiteColor;
        }
    }
}

@media screen and (max-width: 768px){

    .empowering-section{

        .text-empowering{
            width: 100%;
            text-align: center;
            p{
                margin-bottom: 25px;

            }
        }

        .number-user-event{
            width: 100%;
            justify-content: space-around;
        }
    }

}


</style>
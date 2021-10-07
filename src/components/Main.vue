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
            <div class="row tab-section">
                <div class="col-4">
                    
                    <ul>
                        <li><h6 class="active-tab">What We do</h6></li>
                        <li><h6>text</h6></li>
                        <li><h6>text</h6></li>
                        <li><h6>text</h6></li>
                        <li><h6>text</h6></li>
                        <li><h6>text</h6></li>
                    </ul>
                    
                </div>
                <div class="col-8">

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

export default {
    name: "Main",

    components: {
        IconCard,
        StudentExperience
    },

    data(){
        return{
            ElementIconCard,
            StudentExperienceInfo
        }
    }
}
</script>

<style lang="scss">
@import '../style/general.scss';
@import '../style/color.scss';

main{
    position: relative;
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

.tab-section{
    ul{
        list-style: none;
        height: 100%;
        li:last-child{
            border-bottom:  1px solid #e5e5e5;
        }
        li{
            display: flex;
            height: 83px;
            align-items: center;
            border: 1px solid #e5e5e5;
            border-bottom: none;
            
            h6{
                display: flex;
                align-items: center;
                height: 100%;
                margin: 0;
                padding-left: 40px;
                border: none;
                border-left: 5px solid transparent;
                font-family: $primaryFont;
                font-weight: 600;
                color: $textColorGrey;
            }

            .active-tab{
                border-left: 5px solid $backgroundPrimary;
                background-color: #fcfcfc;
                color: $backgroundPrimary;
            }
            
        }
    }
}

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
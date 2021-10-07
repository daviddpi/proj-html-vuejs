<template>
    <main>
        <div class="container">
            <div class="row d-flex g-3 row-icon">
                <IconCard v-for="(icon, index) in ElementIconCard" :key="index" :src="ElementIconCard[index].src" 
                :alt="ElementIconCard[index].alt" :text="ElementIconCard[index].text"/>
            </div>
            <div class="row trusted-name-section">
                <div class="col-12">
                    <h1>The Trusted Name <br>for In-Home Tutoring.</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat totam facere sapiente nobis commodi eius modi harum labore dolorem assumenda aspernatur rerum hic eaque saepe recusandae, odio error? Ad, odio.</p>
                    <a href="#">Learn More</a>
                    <img src="../assets/img/h5-img-1.jpg" alt="Immagine di riferimento ">
                </div>
            </div>
        </div>
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


export default {
    name: "Main",

    components: {
        IconCard
    },

    data(){
        return{
            ElementIconCard
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


</style>
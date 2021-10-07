<template>
    <div class="jumbo-container mb-5">
        <div class="img-header">
            <img class="header-jumbotron img-fluid" :src="require(`../assets/img/${Jumbotron[indexImg].src}`)" :alt="Jumbotron[indexImg].alt">
        </div>
        <div class="container">
            <div class="row">
                <div class="col-12 text-jumbo">
                    <div>
                        <h1>Contemporary Ideas</h1>
                        <p class="d-none d-sm-none d-md-block">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Doloremque neque aperiam ipsam debitis quasi molestias nostrum laboriosam cupiditate voluptatem obcaecati omnis, quisquam qui. Et consequuntur, odio dolores magnam aut corporis.</p>
                        <button class="mybtn">Register Now</button>
                    </div>
                </div>
            </div>
        </div>
        <div class="circle-container d-flex">
            <div class="circle-index" @click="activeImage(index)" v-for="(circle, index) in Jumbotron.length" :key="index"
            :class="(index == indexImg) ? activeOuter : ''">
                <div :class="(index == indexImg) ? activeInner : ''"></div>
            </div>
        </div>
    </div>
</template>

<script>
import Jumbotron from '../data/jumbotron.json'

export default {
    name: "JumbotronHeader",

    components: {
    },

    data(){
        return{
            indexImg: 0,
            Jumbotron,
            activeOuter: 'active-outer',
            activeInner: 'active-inner',
        }
    },

    methods: {
        nextImage(){
            this.indexImg++;
            if(this.indexImg >= this.Jumbotron.length){
                this.indexImg = 0;
            }
        },

        behindImage(){
            this.indexImg--;
            if(this.indexImg < 0){
                this.indexImg = this.Jumbotron.length - 1;
            }
        },

        activeImage(index){
            console.log("sto cliccando");
            this.indexImg = index;
        }
    },

    mounted(){
        setInterval( () =>{
            this.nextImage();
        }, 5000);

    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/color.scss';

.jumbo-container{
    height: 680px;
    z-index: -2;
    color: $whiteColor;
}

.header-jumbotron{
    width: 100%;
    height: 680px;
    object-fit: cover;
    z-index: -1;
    filter: brightness(65%);
    position: absolute;
}

.circle-container{
    position: absolute;
    bottom: 5%;
    right: 50%;
    width: max-content;
    transform: translate(50%);
}

.circle-index{
    height: 15px;
    width: 15px;
    background-color: rgba(255, 255, 255, .5);
    border-radius: 50%;
    margin: 0 10px;
}

.active-outer{
    border: 0.5px solid $whiteColor;
    background-color: transparent;
    border-radius: 50%;
    height: 15px;
    width: 15px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.active-inner{
    background-color: $whiteColor;
    width: 5px;
    height: 5px; 
    border-radius:50%;
}

.container{
    height: 100%;
    .row{
        height: 100%;
        .text-jumbo{
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            width: 80%;
            margin: 0 auto;
            h1{
                font-size: 5rem;
                font-family: 'Merriweather', serif;
                margin-bottom: 35px;
            }

            p{
                margin-bottom: 40px;
            }
        }

    }
}

@media screen and (max-width: 576px){


    .container{
        .row{
            .text-jumbo{
                h1{
                    font-size: 3rem;
                }
            }
        }
    }
    
}


</style>
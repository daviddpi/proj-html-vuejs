<template>
    <div class="text-center">
        <img :src="require(`../assets/img/${arrayInfo[indexImg].src}`)" :alt="arrayInfo[indexImg].alt">
        <p><q>{{ arrayInfo[indexImg].exp }}</q></p>
        <h5>{{ name }}</h5>
        <h6>Student</h6>
        <div class="circle-container">
            <div class="circle-index" v-for="(circle, index) in arrayInfo.length" :key="index"
            :class="(index == indexImg) ? active : ''"></div>
        </div>
    </div>
</template>

<script>
export default {
    name: "StudentExperience",
    props: {
        arrayInfo: Array,
    },

    data(){
        return{
            indexImg: 0,
            active: 'active',
        }
    },

    methods: {
        nextImage(){
            this.indexImg++;
            if(this.indexImg >= this.arrayInfo.length){
                this.indexImg = 0;
            }
        },

        behindImage(){
            this.indexImg--;
            if(this.indexImg < 0){
                this.indexImg = this.arrayInfo.length - 1;
            }
        },

    },

    mounted(){
        setInterval( () =>{
            this.nextImage();
        }, 6500);

    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/color.scss';


img{
    margin-bottom: 25px;
}

h5{
    font-family: $primaryFont;
}

h6{
    text-transform: uppercase;
    margin-bottom: 40px;
}

p{
    margin: 0 auto;
    width: 50%;
    margin-bottom: 30px;
}

.circle-container{
    display: flex;
    justify-content: center;
    align-items: center;
}

.circle-index{
    height: 15px;
    width: 15px;
    background-color: rgba(255, 255, 255, .5);
    border-radius: 50%;
    margin: 0 10px;
}

.active{
    background-color: $whiteColor;
}


</style>
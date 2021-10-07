<template>
        <div class="col-md-4 col-lg-2 d-none d-sm-none d-md-block">
            <div class="card-icon">
                <div>
                    <img :src="require(`../assets/img/${src}`)" :alt="`${alt}`">
                    <h3>{{ text }}</h3>
                </div>
            </div>
        </div>  
</template>

<script>

export default {
    name: "IconCard",
    data(){
        return{

        }
    },

    props: {
        src: String,
        alt: String,
        text: String
    }

    
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/color.scss';

.card-icon{
    height: 250px;
    background-color: $backgroundIcon;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    font-family: 'Merriweather', serif;
    border: 1px solid #f2f2f2;
    h3{
        font-size: 1.4rem;
        font-weight: 600;
    }   

    img{
        margin-bottom: 20px;
    }
}

</style>
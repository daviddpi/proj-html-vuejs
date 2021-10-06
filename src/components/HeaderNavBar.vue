<template>
    <div class="bg-nav">
        <div class="container-fluid">
            <div class="row">
                <div class="col-12">
                    <nav class="d-flex ">
                        <ul class="d-flex align-item-center justify-content-evenly">
                            <li>
                                <img src="../assets/img/logo-light.png" alt="Logo iAcademy">
                            </li>
                            <li v-for="(element, index) in elementNav" :key="index"><a :href="element.link"> {{ element.name }} </a></li>
                        </ul>
                        <div class="d-flex align-item-center" id="icon-nav">
                            <i class="fas fa-search"></i>
                            <i class="fas fa-shopping-bag"></i>
                            <i class="fas fa-bars"></i>
                        </div>  
                    </nav>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "HeaderNavBar",

    props: {
        elementNav: Array,
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/color.scss';

nav{
    background: black;
    img{
        width: 200px;
    }
}

ul{
    list-style: none;
    margin: 0;
    padding: 0;
    width: 100%;
    li{
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        width: 100%;
        a{
            display: inline-block;
            text-decoration: none;
            text-transform: uppercase;
            color: $whiteColor;
        }
    }
}

#icon-nav{
    align-self: center;
    flex-basis: 15%;
    justify-content: space-evenly;
    color: $whiteColor;

    .fa-search{
        transform: rotate(90deg);
    }
}

</style>
<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-12 nav-container">
                <nav class="d-flex">
                    <ul class="d-flex align-item-center justify-content-evenly">
                        <li class="d-block">
                            <img id="logo-header" src="../assets/img/logo-light.png" alt="Logo iAcademy">
                        </li>
                        <li class="d-none d-lg-flex" v-for="(element, index) in elementNav" :key="index"><a :href="element.link"> {{ element.name }} </a></li>
                    </ul>
                    <div class="d-flex align-item-center" id="icon-nav">
                        <i class="fas fa-search"></i>
                        <i class="fas fa-shopping-bag">
                            <div id="number-buy">0</div>
                        </i>
                        <i class="fas fa-bars"></i>
                    </div>  
                </nav>
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


.nav-container{
    position: absolute;
    top: 0;
}

nav{
    padding: 15px;
    #logo-header{
        width: 200px;
        z-index: 2;
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

            &:hover{
                text-decoration: underline;
                color: $whiteColor;
            }
        }
    }
}

.fa-shopping-bag{
    position: relative;
}

#icon-nav{
    align-self: center;
    flex-basis: 15%;
    justify-content: space-evenly;
    color: $whiteColor;

    .fa-search{
        transform: rotate(90deg);
    }

    i{
        height: 100%;
        padding: 10px;


        &:hover{
            background-color: rgba(255, 255, 255, 0.35);
            border-radius: 50%;
            padding: 10px;
            cursor: pointer;
        }
    }
}

#number-buy{
    position: absolute;
    top: 3px;
    right: 3px;
    background-color: $backgroundPrimary;
    border-radius: 50%;
    padding: 2px 4px;
    font-size: 0.8rem;
}

@media screen and (max-width: 768px){
    img{
        width: 150px;
    }

    #icon-nav{
        i{
            padding: 0 10px;
        }
    }
}

</style>
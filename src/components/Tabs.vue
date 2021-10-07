<template>
    <div class="row tab-section">
        <div class="col-12 col-md-4">
            <ul>
                <li @click="changeTabs(index)" v-for="(tab, index) in tabElement" :key="index"><h6 :class="{'active-tab': index == indexTab}"> {{ tab.name }} </h6></li>
            </ul>
            
        </div>
        <div class="col-12 col-md-8 text-tab">
            <div>
                <h1> {{ tabsInfo[indexTab].title }} </h1>
                <p> {{ tabsInfo[indexTab].text }} </p>
                <ul>
                    <li v-for="(element, index) in tabsInfo[indexTab].list" :key="index"><i class="fas fa-check"></i> {{ element }} </li>
                </ul>
                <img class="img-tab" :src="require(`../assets/img/${tabsInfo[indexTab].src}`)" alt="Immagine">
            </div>   
        </div>
    </div>
</template>

<script>
export default {
    name: "tabs",

    data(){
        return{
            indexTab: 0,
        }
    },

    props: {
        tabElement: Array,
        tabsInfo: Array
    },

    methods: {
        changeTabs(index){
            this.indexTab = index;
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/color.scss';


.tab-section{
    min-height: 540px;
    margin-bottom: 150px;
    ul{
        list-style: none;
        height: 100%;
        li:last-child{
            border-bottom:  1px solid #e5e5e5;
        }
        li{
            display: flex;
            height: 80px;
            align-items: center;
            border: 1px solid #e5e5e5;
            border-bottom: none;

            &:hover{
                cursor: pointer;
            }
            
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


    .text-tab{
        padding: 25px;
        div{
            width: 75%;
            position: relative;
            
            h1{
                font-family: $primaryFont;
                font-weight: bold;
                margin-bottom: 25px;
            }

            p{
                margin-bottom: 70px;
            }

            ul{
                list-style: none;
                margin-left: 0;
                padding-left: 1rem;

                li{
                    border: none;
                    height: max-content;
                    margin-bottom: 25px;
                    color: #808080;
                    width: 80%;

                    .fa-check{
                        color: $backgroundPrimary;
                        margin-right: 15px;
                    }
                }

            }
            .img-tab{
                position: absolute;
                bottom: -20px;
                right: -20px;
                width: 100px;
            }
        }
    }
}

</style>
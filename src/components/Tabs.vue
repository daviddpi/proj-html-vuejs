<template>
    <div class="row tab-section">
        <div class="col-4">
            <ul>
                <li @click="changeTabs(index)" v-for="(tab, index) in tabElement" :key="index"><h6 :class="{'active-tab': index == indexTab}"> {{ tab.name }} </h6></li>
            </ul>
            
        </div>
        <div class="col-8 text-tab">
            <div>
                <h1>Learning Possibilites</h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit exercitationem in fugiat nemo magnam eaque. Repudiandae aperiam eveniet dolorem tempora tenetur alias voluptate facere provident. Culpa id perferendis ut provident?</p>
                <ul>
                    <li><i class="fas fa-check"></i> testo</li>
                    <li>testo</li>
                    <li>testo</li>
                    <li>testo</li>
                </ul>
                <img class="img-tab" src="../assets/img/h12-tabs-icon-1.png" alt="Immagine di una squadra$backgroundPrimary">
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
        tabElement: Array
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
                margin-bottom: 75px;
            }

            ul{
                list-style: none;
                margin-left: 0;
                padding-left: 1rem;
                // text-indent: -1.2rem;

                li{
                    border: none;
                    height: max-content;
                    margin-bottom: 30px;
                    color: #808080;

                    .fa-check{
                        color: $backgroundPrimary;
                        margin-right: 15px;
                    }
                }

            }
            .img-tab{
                position: absolute;
                bottom: -30px;
                right: 0;
                width: 100px;
            }
        }
    }
}

</style>
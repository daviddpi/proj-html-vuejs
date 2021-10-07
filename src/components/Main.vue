<template>
    <main>
        <div class="container">
            <div class="row d-flex g-3">
                <IconCard v-for="(icon, index) in ElementIconCard" :key="index" :src="ElementIconCard[index].src" 
                :alt="ElementIconCard[index].alt" :text="ElementIconCard[index].text"/>
            </div>
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



</style>
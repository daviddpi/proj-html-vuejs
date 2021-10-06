<template>
    <header>
        <HeaderNavBar :elementNav="ElementNavBar"/>
    </header>
</template>

<script>
import ElementNavBar from '../data/headerNavBar.json'
import HeaderNavBar from './HeaderNavBar.vue'

export default {
    name: 'Header',

    data(){
        return{
            ElementNavBar,
        }
    },

    components: {
        HeaderNavBar
    }
}
</script>

<style lang="scss">
@import '../style/general.scss';
@import '../style/color.scss';


</style>
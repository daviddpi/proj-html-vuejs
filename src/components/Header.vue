<template>
    <header>
        <HeaderNavBar :elementNav="ElementNavBar"/>
        <JumbotronHeader />
    </header>
</template>

<script>
import ElementNavBar from '../data/headerNavBar.json'
import HeaderNavBar from './HeaderNavBar.vue'
import JumbotronHeader from './JumbotronHeader'

export default {
    name: 'Header',

    data(){
        return{
            ElementNavBar,
        }
    },

    components: {
        HeaderNavBar,
        JumbotronHeader,
    }
}
</script>

<style lang="scss">
@import '../style/general.scss';
@import '../style/color.scss';

header{
    position: relative;
}

</style>
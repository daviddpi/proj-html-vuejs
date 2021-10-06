<template>
    <header>
        <h1 class="text-danger">Header</h1>
    </header>
</template>

<script>
import ElementNavBar from '../data/headerNavBar.json'
export default {
    name: 'Header',
    data(){
        return{
            ElementNavBar
        }
    },
    components: ""
}
</script>

<style lang="scss">
@import '../style/general.scss';

</style>
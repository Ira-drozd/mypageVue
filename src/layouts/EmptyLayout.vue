<template>
    <div class="container">

        <BurgerMenu></BurgerMenu>

        <div class="main-content">

            <router-view/>

        </div>

    </div>
</template>

<script>
    import BurgerMenu from "../components/app/BurgerMenu";

    export default {
        //name: "EmptyLayout"
        name: 'empty-layout',
        components: {
            BurgerMenu
        }
    }
</script>

<style scoped>

</style>
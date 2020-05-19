<template>

<div>
    <div class="burger-open burger-open_style">
        <i class="fas fa-bars   fa-3x"></i>
    </div>

    <div class="burger-menu burger-menu_style">

        <div class="burger-menu__burger-clause burger-menu__burger-clause_style">
            <i class="fas fa-times "></i>
        </div>

        <div class="burger-menu__burger-panel">
            <ul class="burger-menu__burger-items">
                <li class="burger-menu__burger-item burger-menu__burger-item_style"><a href="#"><i
                        class="fas fa-user-alt"></i>Summary</a></li>
                <li class="burger-menu__burger-item burger-menu__burger-item_style"><a href="#"><i
                        class="fas fa-angle-double-down"></i>Download summary</a></li>
            </ul>
        </div>
    </div>

</div>

</template>

<script>
    export default {
        name: "BurgerMenu"
    }
</script>

<style scoped>

</style>
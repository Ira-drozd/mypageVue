<template>

    <div>
        <div class="burger-open burger-open_style" v-if="!burgerOpen" @click="burgerOpen=true">
            <i class="fas fa-bars   fa-3x"></i>
        </div>

        <transition
                    name="custom-classes-transition"
                    enter-active-class="animate__animated animate__slideInLeft speed"
                    leave-active-class="animate__animated animate__slideOutLeft speed"
        >

        <div class="burger-menu burger-menu_style" v-if="burgerOpen">

            <div class="burger-menu__burger-clause burger-menu__burger-clause_style" @click="burgerOpen=false">
                <i class="fas fa-times "></i>
            </div>

            <div class="burger-menu__burger-panel">
                <ul class="burger-menu__burger-items">

                    <router-link
                            v-for="page in pages"
                            :key="page.url"
                            tag="li"
                            class="burger-menu__burger-item burger-menu__burger-item_style"
                            active-class="burger-menu__burger-item_active"
                            :to="page.url"
                            :exact="page.exact"
                    >
                        <a href="#" @click="burgerOpen=false"><i :class="page.icon"></i>{{page.name}}</a>
                    </router-link>

                </ul>
            </div>
        </div>

        </transition>

    </div>

</template>

<script>
    export default {
        name: "BurgerMenu",
        data: function () {
            return {
                burgerOpen: false,
                pages: pages
            }
        },
        methods: {
            /* callingFunction:function (event) {
                 if (event) {
                     alert(event.target.tagName)
                 }
             }*/
        }
    }

    let pages = [
        {
            name: "Summary",
            icon: "fas fa-user-alt",
            url: "/main"
        },
        {
            name: "Download summary",
            icon: "fas fa-angle-double-down",
            url: "/",
            exact:true
        }
    ];
</script>

<style scoped>

</style>
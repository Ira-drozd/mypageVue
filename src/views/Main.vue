<template>
    <div class="main-content__container">

        <div class="main-content__nav-buttons main-content__nav-buttons_style">
                <a
                    v-for="tab in tabs"
                    v-bind:key="tab.name"
                    v-bind:class="['main-content__item-button main-content__item-button_style', { 'main-content__item-button_active': currentTab.name === tab.name }]"
                    v-on:click="currentTab = tab"
            >
                <i :class="tab.icon"></i> {{tab.name}}
                <div class="main-content__item-button_line"></div>
            </a>

        </div>





            <div class="main-content__profile-photo main-content__profile-photo_style">
                <div class="main-content__photo main-content__photo_style">
                    <svg width="113" height="67" viewBox="0 0 113 67" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M1 16.8011V66H111L1 1V16.8011Z" fill="#fffef6" stroke="white"/>
                    </svg>

                    <svg width="113" height="67" viewBox="0 0 113 67" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M112 16.8011V66H2L112 1V16.8011Z" fill="#fffef6" stroke="white"/>
                    </svg>

                </div>
                <div class="main-content__short-profile main-content__short-profile_style">
                    <p class="main-content__short-profile_name">Ira Matveichuk</p>
                    <p class="main-content__short-profile_profession">Front-End Developer</p>
                    <div class="main-content__short-contact main-content__short-contact_style">
                        <div class="main-content__short-contact-item"><a title="Telegram"
                                                                         href="tg://resolve?domain=dia130396"><i
                                class="fab fa-telegram-plane"></i></a>
                        </div>
                        <div class="main-content__short-contact-item"><a title="Viber"
                                                                         href="viber://chat?number=+375291606474"><i
                                class="fab fa-viber"></i></a></div>
                        <div class="main-content__short-contact-item"><a title="Vk" href="https://vk.com/id74865139"><i
                                class="fab fa-vk"></i></a></div>
                        <div class="main-content__short-contact-item"><a title="facebook"
                                                                         href="https://www.facebook.com/ira.matveichuk.1"><i
                                class="fab fa-facebook-f"></i></a>
                        </div>
                        <div class="main-content__short-contact-item"><a title="skype" href="skype:dia130396?call"><i
                                class="fab fa-skype"></i></a>
                        </div>
                        <div class="main-content__short-contact-item"><a title="email"
                                                                         href="mailto:dia130396@gmail.com"><i
                                class="far fa-envelope"></i></a>
                        </div>
                    </div>
                </div>
            </div>

        <div class="main-content__effect-tabs">
            <transition mode="out-in"
                        name="custom-classes-transition"
                        enter-active-class="animate__animated animate__slideInLeft speed"
                        leave-active-class="animate__animated animate__slideOutLeft speed"
            >

                <about-tab v-if="currentTab.name=='About'"></about-tab>

                <resume-tab v-if="currentTab.name=='Resume'"></resume-tab>

                <work-tab v-if="currentTab.name=='Works'"></work-tab>

                <contact-tab v-if="currentTab.name=='Contact'"></contact-tab>

            </transition>

        </div>



    </div>
</template>

<script>

    let tabs = [
        {
            name: "About",
            icon:"fas fa-user-alt",
            component: {
                template: "<div>Home component</div>"
            }
        },
        {
            name: "Resume",
            icon:"fas fa-file-contract",
            component: {
                template: "<div>Posts component</div>"
            }
        },
        {
            name: "Works",
            icon:"fas fa-paint-brush",
            component: {
                template: "<div>Archive<p>dsd</p> component</div>"
            }
        },
        {
            name: "Contact",
            icon:"fas fa-at",
            component: {
                template: "<div>Posts component</div>"
            }
        }
    ];

    import AboutTab from "../components/app/AboutTab";
    import ResumeTab from "../components/app/ResumeTab";
    import WorkTab from "../components/app/WorkTab";
    import ContactTab from "../components/app/ContactTab";

    export default {
        name: "Main",
        data:function () {
            return{
                tabs: tabs,
                currentTab: tabs[0],
                show: false
            }
        },
        components: {
            AboutTab, ResumeTab, WorkTab, ContactTab
        }
    }
</script>

<style scoped>

</style>
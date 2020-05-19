<template>

    <div class="main-content__tabs main-content__tabs_style">

        <div class="main-content__tab_title"><span>Get</span> in Touch</div>

        <div class="main-content__tab_content">

            <div class="main-content__item main-content__item_contact-width">
                <div class="main-content__tab_title-contact"><span>Address . . . . .</span></div>
                <p>Belarus, Minsk</p>
            </div>

            <div class="main-content__item main-content__item_contact-width">
                <div class="main-content__tab_title-contact"><span>Phone . . . . .</span></div>
                <p><a href="tel:+375291606474">+375&nbsp;29&nbsp;160&nbsp;64&nbsp;74</a></p>
            </div>

            <div class="main-content__item main-content__item_contact-width">
                <div class="main-content__tab_title-contact"><span>Email . . . . .</span></div>
                <p><a href="mailto:dia130396@gmail.com">dia130396@gmail.com</a></p>
            </div>

            <div class="main-content__item main-content__item_contact-width">
                <div class="main-content__tab_title-contact"><span>Freelance . . . . .</span></div>
                <p>Available</p>
            </div>

            <div class="main-content__item main-content__item_full-flex">
                <div class="main-content__tab_title"><span>Contact</span> Form</div>
                <form action="post" name="contact-form" class="main-content__item_formstyle">
                    <div class="main-content__name-form">
                        <input type="text" name="full-name" placeholder="Full name">
                        <input type="email" name="email" placeholder="Email Adress">
                    </div>
                    <div class="main-content__message-form">
                        <textarea rows="5" name="message" placeholder="Your Message"></textarea>
                    </div>
                    <button>SEND MESSAGE <i class="fas fa-chevron-right"></i></button>
                </form>
            </div>

        </div>

    </div>

</template>

<script>
    export default {
        name: "ContactTab"
    }
</script>

<style scoped>

</style>
<template>
    <div id="app">
      <component :is="layout">
        <router-view/>
      </component>
    </div>
</template>

<script>
  import EmptyLayout from "./layouts/EmptyLayout";
    export default {
        computed: {
          layout () {
               // console.log(this.$route.meta);
               // return 'EmptyLayout'
            return (this.$route.meta.layout || "empty") +'-layout'
            }
        },
      components:{
        EmptyLayout
      }
    }
</script>

<style lang="scss">
    /*@import "~folser in node";*/
    @import "~animate.css";
    @import 'assets/summaryVue';
</style>

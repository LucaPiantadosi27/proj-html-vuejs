<script>

import { store } from "../store.js";

import AppMainDream from "./AppMainDream.vue";

import AppMainCounter from "./AppMainCounter.vue";

import AppMainCourses from "./AppMainCourses.vue";

import AppMainLearn from "./AppMainLearn.vue";

import AppMainEvent from "./AppMainEvent.vue";

import AppMainTestimonials from "./AppMainTestimonials.vue";



export default {

    data() {

        return {

            store,

        }

    },

    components: {

        AppMainDream,

        AppMainCounter,

        AppMainCourses,

        AppMainLearn,

        AppMainEvent,

        AppMainTestimonials




    }

}

</script>




<template>
    <main>
        <AppMainDream></AppMainDream>

        <AppMainCounter></AppMainCounter>

        <AppMainCourses></AppMainCourses>

        <AppMainLearn></AppMainLearn>

        <AppMainEvent></AppMainEvent>

        <AppMainTestimonials></AppMainTestimonials>
    </main>
</template>




<style lang="scss" scoped>
main{
    padding-left:250px ;
    padding-right:250px ;
}
</style>
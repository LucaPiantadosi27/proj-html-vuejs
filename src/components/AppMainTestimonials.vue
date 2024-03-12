<script>
import { store } from "../store.js";
import AppTitle from "./AppTitle.vue";
export default {
    data() {
        return {
            store,
        };
    },
    components: { AppTitle }
}
</script>

<template>
    <div class="wrapper">
        <AppTitle :Mono="store.titleSections[5].titleMono" :Purple="store.titleSections[5].titlePurple"
            :Green="store.titleSections[5].titleGreen" :class_align="'text-center'" />
    </div>
</template>

<style lang="scss" scoped></style>
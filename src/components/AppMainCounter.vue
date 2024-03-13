<script>
import { store } from "../store.js";
export default {
    data() {
        return {
            store,
        }
    }
}
</script>

<template>
<div class="bck">
    <div class="numbers my-5">
        <div class="wrapper d-flex justify-content-between p-5">
            <div class="numbers_card" v-for="item in store.numbersInfo">
                <h1 class="ms_h1 ms_color_green text-center fw-bold">{{ item.num }}</h1>
                <span class="text-uppercase font-monospace fw-bold text-center">{{ item.string }}</span>
            </div>
        </div>
    </div>
</div>
</template>

<style lang="scss" scoped>


.numbers {
    border-radius: 50px;
    background-color: rgb(245, 241, 237);
}
h1{
    color: rgb(32, 173, 150);
}

</style>
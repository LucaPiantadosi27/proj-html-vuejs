<script>
import { store } from "../store.js";
import AppTitle from "./AppTitle.vue";
export default {
    data() {
        return {
            store,
        };
    },
    components: { 
        AppTitle 
    },

    methods: {
        getImgUrl(state) {
            return new URL(`../assets/img/${state}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="ms custom-bg p-5 custom-rounded-top">
        <div class="wrapper my-5">
            <AppTitle :Mono="store.titleSections[5].titleMono" :Purple="store.titleSections[5].titlePurple"
                :Green="store.titleSections[5].titleGreen" :class_align="'text-center'" />
            <div class="row row-cols-3 ms_margin">
                <div class="col" v-for="(item, index) in store.opinionsCardInfo" :key="index">
                    <div class="card text-center pt-5 px-5 border-0 position-relative ms_height">
                        <p class="ms_color_violet my-4">{{ item.text }}</p>
                        <p class="text-uppercase fw-bold"> {{ item.name }}</p>
                        <p class="text-secondary">{{ item.pos }}</p>
                        <img class="rounded-circle position-absolute top-0 start-50 translate-middle"
                            :src="getImgUrl(item.img)" :alt="item.img">
                    </div>
                </div>
            </div>
            <div class="text-center">
                <i class="fa-solid fa-circle ms_color_violet"></i>
                <i class="fa-solid fa-circle fa-2xs text-secondary ms-3 my-5"></i>
                <i class="fa-solid fa-circle fa-2xs text-secondary ms-3 my-5"></i>
                <i class="fa-solid fa-circle fa-2xs text-secondary ms-3 my-5"></i>
            </div>
            <div class="ms_color_violet text-center fw-bold my-5 position-relative ">
                <span class="fs-4">Start today for getting <span class="ms_color_green fw-normal">Online
                        Certification</span></span>
                <p class="fs-2">You can be your own guiding star with our help!</p>
                <img src="../assets/img/maxcoach-shape-01.png" alt="image" class="ms_img position-absolute">
                <img src="../assets/img/maxcoach-shape-02.png" alt="image" class="ms_img_two position-absolute">
                <span class="p-2 rounded-circle d-inline-block ms_span position-absolute">
                    <span
                        class="p-4 rounded-circle d-inline-block position-absolute top-50 start-50 translate-middle"></span>
                </span>    
                    
            </div>
            <div class="text-center my-5">
                <button type="button" class="btn btn-success fw-bold border-0 ms_button ms_button_padding">
                    Get started now
                </button>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

.custom-bg{
    background-color:rgb(236, 232, 228) ;
    background: linear-gradient(to bottom, rgb(252, 251, 248, ), rgb(252, 250, 246),rgb(242, 245, 238),rgb(245, 242, 234),rgb(245, 241, 237));
    border-radius: 50px;
}

.ms_span {
    background-color: #f1c6aa;
    width: 60px;
    aspect-ratio: 1;
    top: 15%;
    left: 3.4%;
    span {
        background-color: white;
        width: 30px;
        aspect-ratio: 1;
    }
}
.ms_img {
    width: 135px;
    top: 100%;
    left: 5%;
    z-index: 1;
}
.ms_img_two {
    width: 135px;
    top: 100%;
    right: 3%;
    z-index: 1;
}

.ms_bg_op {
    background-color: #f8f8f8;
}
.ms_margin {
    margin-top: 7rem;
}
.ms_button_padding {
    padding: 1rem 5rem;
}
.ms_height {
    height: 300px;
}
img {
    width: 120px;
}
.custom-rounded-top {
    border-top-left-radius:50px;
    border-top-right-radius: 50px;
}

button {
    background-color:rgb(32, 173, 150);
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    transition: background-color 0.3s ease;
}
.wrapper{
    color: rgb(63, 58, 100);
}

button:hover {
    background-color:rgb(63, 58, 100);
}
</style>
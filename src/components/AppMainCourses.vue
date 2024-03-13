<script>
import { store } from "../store.js";
import AppTitle from "./AppTitle.vue";
import AppMainCoursesCard from "./AppMainCoursesCard.vue";


export default {
    data() {
        return {
            store,
        };
    },
    components: { 
        AppTitle, 
        AppMainCoursesCard 
    }
}
</script>

<template>
<div class="bk">
    <div class="courses">
        <div class="wrapper py-5">
            <AppTitle :Mono="store.titleSections[1].titleMono" :Purple="store.titleSections[1].titlePurple"
                :Green="store.titleSections[1].titleGreen" :class="'text-capitalize'" :class_align="'text-center'" />

            <div class="row row-cols-3 my-5">
                <div class="col mb-4" v-for="(item, index) in store.coursesCardInfo" :key="index">
                    <AppMainCoursesCard :title="item.title" :name="item.name" :nameImg="item.nameImg" :img="item.img"
                        :price="item.price" :lessons="item.lessons" :students="item.students" />
                </div>
            </div>

            <div class="text-center">
                <button type="button" class="btn btn-success fw-bold border-0 ms_button">
                    View all courses
                    <i class="fa-solid fa-arrow-right-long ms-2"></i>
                </button>
            </div>
        </div>
    </div>
</div>
</template>

<style lang="scss" scoped>

.courses {
    background-color: rgb(245, 241, 237);
    border-radius: 100px;
    background-image:linear-gradient(to bottom, rgb(252, 251, 248, ), rgb(252, 250, 246),rgb(245, 242, 234),rgb(245, 241, 237));
}  
// rgb(252, 251, 248, ), rgb(252, 250, 246),rgb(245, 242, 234),rgb(245, 241, 237)
// rgb(245, 241, 237), rgb(245, 242, 234),rgb(252, 250, 246),rgb(252, 251, 248));
button {
    background-color:rgb(32, 173, 150);
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color:rgb(63, 58, 100);
}
</style>
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
    <div id="head">
        <div class="wrapper d-flex justify-content-between align-items-center ms_color_violet py-3">
            <div>
                <img src="../assets/img/dark-logo.png" alt="logo">
            </div>

            <div class="d-flex gap-4 align-items-baseline">
                <ul class="d-flex gap-4">
                    <li v-for="item in store.headerList">
                        <span>{{ item }}</span>
                        <i class="fa-solid fa-angle-down fa-xs"></i>
                    </li>
                </ul>
                
            <div class="d-flex align-items-center gap-4">
                <div class="position-relative">
                    <i class="fa-solid fa-cart-shopping"></i>
                    <span
                        class="position-absolute top-0 start-100 translate-middle badge rounded-circle custom-text-color custom-font-size">o</span>
                </div>

            <div class="d-flex align-items-baseline gap-4">
                <i class="fa-regular fa-circle-user"></i>
                <div class="position-relative">
                    <input class="py-2 px-3 rounded border-0 bg-white" type="text" v-model="store.stringToSearch"
                                id="input" placeholder="Search...">
                    <i
                    class="ms_glass ms custom-text-colorf fa-solid fa-magnifying-glass position-absolute top-50 translate-middle-y"></i>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

i{
    cursor: pointer;
        z-index: 3;
}

.custom-text-color{
        cursor: pointer;
        background-color: rgba(32, 173, 149, 0.767);
        height: 20px;
        font-size: small;
        z-index: 3;
        
    }
    .custom-text-colorf{
        color:rgba(32, 173, 149, 0.767) ;
        cursor: pointer;
        z-index: 3;

    }
#head {
    background-color: rgb(245, 241, 237);
    padding-left:250px ;
    padding-right:250px ;
    img {
        width: 150px;
        
    }
    ul {
        list-style: none;
        li {
            cursor: pointer;
            line-height: 100%;
            z-index: 3;

            i {
                cursor: pointer;
                margin-left: .3rem;
                z-index: 3;
                
            }
        }
    }
    input {
        cursor: pointer;
        width: 200px;
        z-index: 3;
    }
    .ms_glass {
        right: 15px;
    }

    
}
</style>
<script>
export default {
    data() {
        return {
        }
    }
}
</script>

<template>
<div class="overlay">
    <div id="jumbo" class="py-5">
        <div class="wrapper py-5 d-flex align-items-center">
            <div class="w-50 ms_index">
                <h1 class="ms_h1 ms_color_violet w-75 fw-bold">Complete Your Dreams in JavaS Programming</h1>
                <p class="w-75 my-5 ms_color_violet">Learn any coding program in distance and for a reasonable fee. You
                    don't have
                    to
                    struggle
                    alone, you've
                    got our assistance and help.</p>
                <button type="button" class="btn btn-success fw-bold border-0 ms_button">
                    <i class="fa-solid fa-download me-2"></i>
                    Download free E-book
                </button>
            </div>
            <div class="w-50 ms_index">
                <img src="../assets/img/home-5-hero-image.png" alt="image" class="float-end">
            </div>
        </div>
    </div>
</div>
</template>

<style lang="scss" scoped>

#jumbo {
    padding-left:250px ;
    padding-right:250px ;
    background-color: rgb(245, 241, 237);
    
    .ms_index {
        z-index: 1;
    }
}
// da fixare
#jumbo::before {
    content: "";
    position: absolute;
    bottom: 7.5%;
    height: 800px;
    width: 100%;
    background-image: url(../assets/img/jumbo-overlay.svg);
    background-size: cover;
    // background-size: contain;
    background-repeat: no-repeat;
  
    transform: scaleY(-1);
    
}


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
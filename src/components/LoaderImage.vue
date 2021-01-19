<template>
    <div>
        <h2>Image Loader Spinner</h2>
        <button @click="toggleimg">{{ btntext }}</button>
        <div v-if="isLoading" class="loading"></div>
        <img v-show="isLoaded" :src="imgsrc" width="400" @load="loaded">
    </div>
</template>

<script>
export default {
    data () {
        return {
            imgsrc: "https://placeimg.com/500/300/nature",
            btntext: "Show Image",
            isLoaded: false,
            isLoading: false
        }
    },
    methods: {
        loaded() {
            this.isLoaded = true;
            this.isLoading = false;
        },
        toggleimg: function(){
            if (this.imgsrc == "") {
                this.isLoaded =  false;
                this.isLoading = true;
                this.imgsrc = "https://placeimg.com/500/300/nature?t=" + Math.random()
                // this.imgsrc = "../assets/logo.png"
                this.btntext = "Hide Image"
            }else{
                this.imgsrc = ""
                this.btntext = "Show Image"
            }
        }
    }
}
</script>

<style>
    .loading {
        background: transparent url('https://miro.medium.com/max/882/1*9EBHIOzhE1XfMYoKz1JcsQ.gif') center no-repeat;
        height: 200px;
        width: 200px;
    }
</style>
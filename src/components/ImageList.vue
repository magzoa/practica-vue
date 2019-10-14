<template>
    <div>


     <div class="row">
       <div class="col-sm-8 col-12">
         <img :src="selectedImage.imageLink" class="img-fluid">
       </div>
       <div class="col-sm-4 col-12">
         <h1>{{selectedImage.title}}</h1>
         <p>{{selectedImage.description}}</p>
       </div>
     </div>

    <div class="row">
     <div v-for="image in images" :key="image.id" class="col-md-3 col-sm-4 col-6"><a href="#" v-on:click="showImage(image)"><img class="img-fluid" v-bind:src="image.thumbnail" /></a></div>

    </div>
   




    </div>



</template>


<script>
export default {
    props:['images'],
    data(){
        return{
            selectedImage:''

        }

    },
    methods:{
        showImage:function(image){
            this.selectedImage=image
        }
    }
    
}
</script>
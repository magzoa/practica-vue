<template>
  <div class="galeria">
   <div class="container mt-4">
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
  </div>
</template>

<script>
export default {
  data () {
    return {
      selectedImage: '',
      images: [
        {id: 1, title: 'Primera Imagen', description: 'Descripción Primera Imagen', thumbnail: 'https://videotutoriales.com/egipto01.png', imageLink: 'https://videotutoriales.com/egipto01b.png'},
        {id: 2, title: 'Segunda Imagen', description: 'Descripción Segunda Imagen', thumbnail: 'https://videotutoriales.com/egipto02.png', imageLink: 'https://videotutoriales.com/egipto02b.png'},
        {id: 3, title: 'Tercera Imagen', description: 'Descripción Tercera Imagen', thumbnail: 'https://videotutoriales.com/egipto03.png', imageLink: 'https://videotutoriales.com/egipto03b.png'},
        {id: 4, title: 'Cuarta Imagen', description: 'Descripción Cuarta Imagen', thumbnail: 'https://videotutoriales.com/egipto04.png', imageLink: 'https://videotutoriales.com/egipto04b.png'},
        {id: 5, title: 'Quinta Imagen', description: 'Descripción Quinta Imagen', thumbnail: 'https://videotutoriales.com/egipto05.png', imageLink: 'https://videotutoriales.com/egipto05b.png'},
        {id: 6, title: 'Sexta Imagen', description: 'Descripción Sexta Imagen', thumbnail: 'https://videotutoriales.com/egipto06.png', imageLink: 'https://videotutoriales.com/egipto06b.png'},
        {id: 7, title: 'Séptima Imagen', description: 'Descripción Séptima Imagen', thumbnail: 'https://videotutoriales.com/egipto07.png', imageLink: 'https://videotutoriales.com/egipto07b.png'},
        {id: 8, title: 'Octava Imagen', description: 'Descripción Octava Imagen', thumbnail: 'https://videotutoriales.com/egipto08.png', imageLink: 'https://videotutoriales.com/egipto08b.png'}
]
    }
 
  },
  methods: {
            showImage: function (image) {
                this.selectedImage = image
            }
        }
    }

</script>

<style>
  img {
    -webkit-box-shadow: 0px 1px 6px 1px rgba(0,0,0,0.2);
    -moz-box-shadow: 0px 1px 6px 1px rgba(0,0,0,0.2);
    box-shadow: 0px 1px 6px 1px rgba(0,0,0,0.2);
    margin-bottom:20px;
  }

  img:hover {
    filter: gray; /* IE6-9 */
    -webkit-filter: grayscale(1); /* Google Chrome, Safari 6+ & Opera 15+ */
  }
</style>

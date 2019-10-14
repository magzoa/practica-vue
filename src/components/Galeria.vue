<template>
  <div class="gallery container mt-4">

    <single-image :selectedImage="selectedImage"></single-image>
    <image-list :images="images" @emitImage="showImage"></image-list>

  </div>


</template>

<script>

import ImageList from './ImageList';
import SingleImage from './SingleImage';

export default {
name:'galeria',
components:{SingleImage,ImageList},

  data () {
    return {
      selectedImage:'',
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
  methods:{
    showImage:function(image){
      this.selectedImage=image
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

<script setup>

import Sidebar from './components/Sidebar.vue'
import ImageGallery from './components/ImageGallery.vue'
import {ref} from "vue"


  const isWithColor = ref(true)

  const onSelectOption = (isColor) => {
        isWithColor.value= isColor
  }

</script>

<template>
  <VApp>
    <Sidebar @selectOption="onSelectOption" />


    <VMain>
      <!-- {{ isWithColor }} -->
      <ImageGallery :isWithColor="isWithColor"/>
    </VMain>
  </VApp>


</template>


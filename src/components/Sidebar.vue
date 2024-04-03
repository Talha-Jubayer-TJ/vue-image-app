<script setup>

import { defineEmits } from 'vue';

  const emits = defineEmits(['selectOption'])

  const selectOption = (isColor) =>{

      emits("selectOption", isColor)
  }

</script>

<template>
    <VNavigationDrawer 
        expand-on-hover
        rail
    >
    <VList>
          <VListItem
            prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
            title="Talha"
            subtitle="Talha@gmail.com"
          ></VListItem>
    </VList>

    <VDivider></VDivider>

    <VList density="compact" nav>
          <VListItem
           prepend-icon="mdi-folder"
           title="Color Gallery" 
           value="color"
           @click="selectOption(true)"
          />
          <VListItem 
            prepend-icon="mdi-dialpad" 
            title="GraySpace Gallery" 
            value="gray"
            @click="selectOption(false)"
          />

    </VList>

    </VNavigationDrawer>

    
</template>
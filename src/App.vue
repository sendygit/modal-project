<script setup>
import { ref } from "vue";
import Modal from "@/components/Modal.vue";

const title = ref('My First Vue App');
// const header = ref('Sign Up for the giveaway');
// const text = ref('Grab your ninja swag for half price!');
const showModal= ref(false);

function toggleModal () {
  showModal.value = !showModal.value
}
</script>

<template>

 <router-view />


<!-- <header>
<div class="flex flex-col">

  <h1>{{ title }}</h1>
  <div > 
     <Modal :header="header" :text="text" theme="sale" @close="toggleModal"></Modal>
     <Modal  v-if="showModal"  theme="sale" @close="toggleModal">
     <template #header>
       <h1 class="text-2xl">Sign Up for the giveaway</h1>
     </template>
     <template #body>
       <p>Grab your ninja swag for half price!</p>
     </template>
      <template #footer>
       <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. </p>
     </template>
     </Modal>
  </div>
  <button class="py-4 bg-red-600" @click  ="toggleModal">Open Modal</button>
</div>
</header> -->



</template>

<style>
#app {
  font-family: Arial, Helvetica, sans-serif;
  text-align: center;
  margin-top: 60px;
}
  h1{
    border-bottom: 1px solid #ddd ;
        display: inline-block;
        padding-bottom: 10px;
  }
</style>
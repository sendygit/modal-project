<template>
    <div class="backdrop" @click.self="closeModal">
        <div class="modal" :class="{ sale: theme === 'sale' }">
            <slot name="header"></slot>
            <slot name="body"></slot>
            <slot name="footer"></slot>
        </div>
    </div>
</template>

<script setup>
const props = defineProps({
  title : String,
  header: String,
  text: String,
  theme: String
});
const emits = defineEmits(['close'])
function closeModal() {
    emits('close')
}
</script>

<style scoped>
    .modal {
        width: 400px;
        padding: 20px;
        margin: 100px auto;
        background: white;
        border-radius: 10px;
    }
    .backdrop {
        top: 0; 
        position: fixed;
        background: rgba(0, 0, 0, 0.5);
        width: 100%;
        height: 100%;
    }
    h1 {
        color: blue;
        border: none;
        padding: 0;
    }
    .modal.sale {
        background: crimson;
        color: white;
    }
    .modal.sale h1{
        color: white    ;
    }
</style>
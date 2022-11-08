<template>
    <div class="backdrop" @click.self="closeModal">
        <div class="modal" :class="{sale: theme === 'sale'}">
           <slot></slot>
        </div>
    </div>
    
</template>

<script>
export default {
    props: ['theme'],
    methods: {
        closeModal() {
            this.$emit('close')
        }
    }
    }
</script>
<style scoped>
.modal{
    padding: 20px;
    width: 400px;
    text-align: center;
    font-size: 20px;
    background: white;
    border-radius: 10px;
    margin: 100px auto;
}
    .backdrop{
        top: fixed;
        width: 100%;
        height: 100%;
        background: rgba(0,0,0,0.5);
        position: fixed;
    }
    .modal.sale {
        background: crimson;
        color: white;
    }
    .modal.sale h1 {
        color: white;
    }
</style>


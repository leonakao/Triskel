<template>
    <div
        id="barra"
        class="elevation-4"
    />
</template>

<script>
export default {
    props: {
        tamanho: {
            type: String,
            default:"",
        }
    }
};
</script>

<style scoped>
  #barra{
    color: #a91d21ff;
    background-color: #a91d21ff;
    height: 8px;
    width: 55%;
    box-shadow: 10px 8px 10px #888888;
    margin-bottom: 1%;
  }
</style>


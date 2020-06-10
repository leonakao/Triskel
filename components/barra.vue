<template>
  <div
    id="barra"
    :width="tamanho"
  >
  </div>
</template>

<script>
export default {
  props: {
      tamanho: {
        type: String,
        default:"5",
      }
    }
}
</script>

<style scoped>
  #barra{
    color: #a91d21ff;
    background-color: #a91d21ff;
    height: 10px;
  }
</style>


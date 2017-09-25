<template>
  <div class="components-container" style='height:100vh'>
    <div class='chart-container'>
      <line-marker height='30%' width='30%'></line-marker>
    </div>
  </div>
</template>

<script>
import lineMarker from '@/components/Charts/lineMarker'

export default {
  components: { lineMarker }
}
</script>

<style scoped>
.chart-container{
  position: relative;
  width: 100%;
  height: 80%;
}
</style>


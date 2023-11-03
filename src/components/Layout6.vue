<template>
     <div class="layout6">
      <span class="layout6_text">CD PROJEKT®, Cyberpunk®, Cyberpunk 2077®</span>
    </div>
</template>

<script>
export default {
  name: 'Layout6Component'
}
</script>

<style lang="scss">
.layout6 {
  height: 40px;
  background-color:  #000000; 
  display: flex;
  align-items: center;
  justify-content: center;
    &_text {
      font-family: Roboto;
      font-size: 12px;
      font-weight: 400;
      line-height: 14px;
      letter-spacing: 0em;
      text-align: center;
      color: #FFFFFF;
  }
}
</style>
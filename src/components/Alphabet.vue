<template>
  <div>
    <ul class="list">
      <li class="item">a</li>
      <li class="item">b</li>
      <li class="item">c</li>
      <li class="item">d</li>
      <li class="item">e</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Alphabet'
}
</script>

<style lang="stylus" scoped>
  .list
    display: flex
    flex-direction: column
    justify-content: center
    position: absolute
    top: 1.58rem
    right: 0
    bottom: 0
    width: .4rem
    .item
      @import '../assets/styles/varibles.styl'
      line-height: .4rem
      text-align: center
      color: $bgColor
</style>

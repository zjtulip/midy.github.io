<template>
  <div class="index">
    <Main></Main>
  </div>
</template>

<script>
import Main from '@/components/main'
export default {
  name: 'apps',

  components: { Main }
}
</script>
<style lang="stylus" scoped>
.index
  width 100%
  height 100%
  background-color #fdebea
  display flex
  justify-content center
  align-items center
</style>

<template>
  <div class="singer">
    歌手
  </div>
</template>

<script>
  import { getSingerList } from '@/service/singer'

  export default {
    name: 'singer',
    data() {
      return {
        singers: []
      }
    },
    async created() {
      const result = await getSingerList()
      console.log(result)
      this.singers = result.singers
    }
  }
</script>

<style lang="scss" scoped>

</style>

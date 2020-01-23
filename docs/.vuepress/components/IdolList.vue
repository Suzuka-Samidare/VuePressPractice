<template>
  <div>
    <img class="all-idol-image" v-for="idol in idolArray" :src="`/idol/${idol.id}${idol.name}.png`" height="300">
  </div>
</template>

<script>
export default {
  data () {
    return {
      idolArray: [
        { id: '001', name: 'haruka' },
        { id: '002', name: 'chihaya'},
        { id: '003', name: 'miki' },
        { id: '004', name: 'yukiho' },
        { id: '005', name: 'yayoi' },
        { id: '006', name: 'makoto' },
        { id: '007', name: 'iori' },
        { id: '008', name: 'takane' },
        { id: '009', name: 'ritsuko' },
        { id: '010', name: 'azusa' },
        { id: '011', name: 'ami' },
        { id: '012', name: 'mami' },
        { id: '013', name: 'hibiki' }
      ]
    }
  }
}
</script>

<style scope>
img.all-idol-image {
  border-bottom: 1px solid lightgray;
}
</style>
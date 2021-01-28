<template>
    <div>
<!--      <img :src="'/'+item+'.png'" alt="" width="200px" v-for="item in list">-->
      <img :src="`/${item}.png`" alt="" width="200px" v-for="item in list">
    </div>
</template>

<script>
export default {
  data(){
    return{
      list:[1,2,3,4]
    }
  }
}
</script>

<style scoped>

</style>

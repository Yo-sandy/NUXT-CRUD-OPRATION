<template>
  <post-form :post="post" @save-post="savePost" title="Create post"/>
</template>

<script>
export default {
  data(){
    return{
      post:{
        title: "",
        userId: 10,
        body: "",
      },
    };
  },

  methods:{
    async savePost(){
      try{
        const  response = await  this.$axios.post(
          "https://jsonplaceholder.typicode.com/posts",
          {
            title: this.post.title,
            body: this.post.body,
            userId: this.post.userId,
          }
        );
        this.$toast.success("post to save").goAway(2000)
      }catch (e) {
        this.$toast.error("error to save").goAway(2000)
      }
    },
  },
}
</script>

<style scoped>

</style>

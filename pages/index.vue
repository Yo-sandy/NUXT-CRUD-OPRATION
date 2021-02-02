
<template>
  <div class="container">
    <div class="row">
      <div class="col-md-12" v-if="isEditing">
        <post-form :post="post" @save-post="updatePost" title="Edit post"/>
      </div>
      <div class="col-md-12 mt-3">
        <h2 class="text-center bg-success text-white p-3 rounded-pill">All Post</h2>
        <ul class="list-group mb-2">
          <li class="list-group-item" v-for="post in posts" :key="post.id">
            {{ post.title }}
            <span class="float-end">
              <button class="btn-outline-primary" @click="editPost(post)">Edit</button>
              <button class="btn-outline-danger" @click="deletePost(post.id)">Delete</button>
            </span>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: "Post",
  data() {
    return {
      posts: [],
      isEditing: false,
      post: {
        title: "",
        body: "",
        id: null,
        userId: null,
      }
    }
  },
  mounted() {
    this.getPosts();
  },
  methods: {
    async getPosts() {
      const url = "https://jsonplaceholder.typicode.com/posts";
      const {data} = await this.$axios.get(url);
      this.posts = data;
    },
    async editPost(post) {
      this.post.title = post.title;
      this.post.body = post.body;
      this.post.id = post.id;
      this.post.userId = post.userId;

      this.isEditing = true;
    },
    async updatePost() {
      if (this.post.id === null || !this.isEditing) return;
      const url = `https://jsonplaceholder.typicode.com/posts/${this.post.id}`;
      try {
        await this.$axios.put(url, this.post);
        this.$toast.success("updated").goAway(2000);
        this.post = {
          title: "",
          body: "",
          id: null,
          userId: null
        };
        this.isEditing = false;
      } catch (e) {
        this.$toast.error("unable to update")
      }
    },
    async deletePost(id) {
      const url = `https://jsonplaceholder.typicode.com/posts/${id}`;
      try {
        await this.$axios.delete(url);
        this.$toast.success("post delete").goAway(1000);
        await this.getPosts();
      } catch (e) {
        this.$toast.error("unable to delete post").goAway(1000);
      }
    },
  },
};
</script>

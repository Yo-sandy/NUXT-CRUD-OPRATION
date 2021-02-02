<template>
  <div class="container mt-3">
    <h2 class="col-md-12 p-2 text-center bg-success">{{ title }}</h2>
    <label for="title">Title</label>
    <input
      type="text"
      id="title"
      class="form-control"
      v-model="post.title"
    />
    <label for="body">Body</label>
    <textarea
      type="text"
      id="body"
      class="form-control"
      v-model="post.body"
    />
    <div class="text-center mt-3">
      <button class="btn btn-outline-primary" @click="$emit('save-post')">Save Post</button>
    </div>
    <br>
     <div>
       <button
         class="btn btn-outline-success rounded-pill"
         style="box-shadow: 1px 1px 5px 7px ">Iran man</button>
     </div>
  </div>

</template>


<script>
export default {
  props:{
    post:{
      type:Object,
      required:true
    },
    title:{
      type:String,
      required: true
    }
  }
}
</script>

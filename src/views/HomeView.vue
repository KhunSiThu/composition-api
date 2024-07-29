<template>
  <div class="home">
    <PostsLists :posts="posts"></PostsLists>
  </div>
</template>

<script>
import PostsLists from '../components/PostsLists'
import { computed, ref } from 'vue';




export default {
  components: { PostsLists },
  setup(){
    let posts = ref([
      {title : "post title 1", body: "lorem ipsm",id: 1,},
      {title : "post title 2", body: "vLorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.", id:2}
    ])

    return {posts}
  }
}
</script>

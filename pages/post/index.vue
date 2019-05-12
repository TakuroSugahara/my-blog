<template>
  <div>
    <h1 class="mt-4 text-xs-center title font-weight-bold">
      記事一覧
    </h1>
    <PostList :posts="posts" class="mt-4" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import PostList from '../../components/molecules/PostList'

@Component({
  components: {
    PostList
  },
  data() {
    return {
      posts: ['', '', '', '', '', '', '', '', '', '']
    }
  }
})
export default class Home extends Vue {}
</script>

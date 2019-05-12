<template>
  <div>
    <h1 class="mt-4 text-xs-center title font-weight-bold">
      {{ post.title }}
    </h1>
    <div v-for="i in 10" :key="i">
      <v-img src="https://source.unsplash.com/random" class="mt-3" />
      <p class="mt-4 px-2" v-text="post.content" />
    </div>
    <v-btn to="/post">戻る</v-btn>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
  data() {
    return {
      post: {
        title: 'タイトルだよ',
        content:
          '2019年4月20日（土）、スポル品川大井町にて開催した、ウィメンズヘルスのフィットネス・フェス「Women`s Health FIT NIGHT OUT 2019 SPRING」。DAYセッション、NIGHTセッション合計で1000人を超えるフィットネス女子たちが集い、共に汗をかき、自分の限界を超えた一日の模様をお届け！'
      }
    }
  }
})
export default class Home extends Vue {}
</script>

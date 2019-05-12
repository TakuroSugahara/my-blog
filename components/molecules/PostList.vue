<template>
  <div>
    <v-layout row wrap>
      <v-flex
        v-for="(post, index) in posts"
        :key="index"
        xs12
        sm6
        class="pt-3 px-2"
      >
        <v-card>
          <v-img
            class="white--text"
            height="200px"
            src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
          >
            <v-container fill-height fluid>
              <v-layout fill-height>
                <v-flex xs12 align-end flexbox>
                  <span class="headline">Top 10 Australian beaches</span>
                </v-flex>
              </v-layout>
            </v-container>
          </v-img>
          <v-card-title>
            <div>
              <span class="grey--text">Number 10</span><br />
              <span>Whitehaven Beach</span><br />
              <span>Whitsunday Island, Whitsunday Islands</span>
            </div>
          </v-card-title>
        </v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
  props: {
    posts: {
      type: Array,
      default: () => []
    }
  }
})
export default class PostList extends Vue {}
</script>

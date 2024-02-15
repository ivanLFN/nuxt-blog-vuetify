<template>
  <v-container>
    <v-row>
      <v-col v-for="article in articles" :key="article.slug" cols="12" sm="6" md="4">
        <v-card>
          <v-img :src="article.img" :alt="article.alt"></v-img>
          <v-card-title>{{ article.title }}</v-card-title>
          <v-card-text>{{ article.description }}</v-card-text>
          <v-card-actions>
            <v-btn text color="primary">Read more</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const articles = await $content('articles')
      .where({
        'tags': {
          $regex: params.tag,
          $options: 'i'
        }
      })
      .sortBy('createdAt', 'asc')
      .fetch()

    return {
      articles
    }
  }
}
</script>

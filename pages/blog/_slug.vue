<template>
  <article>
    <v-list>
      <NuxtLink
        v-for="link of article.toc"
        :key="link.id"
        :to="`#${link.id}`"
        class="text-decoration-none"  
      >
        <v-list-item>
          <v-list-item-title>{{ link.text }}</v-list-item-title>
        </v-list-item>
      </NuxtLink>
    </v-list>
    <h1>{{ article.title }}</h1>
    <p>{{ article.description }}</p>
    <img
      :src="require(`~/static/articles/${article.img}`)"
      :alt="article.alt"
    />
    <p>Article last updated: {{ formatDate(article.updatedAt) }}</p>

    <nuxt-content :document="article" />

    <AuthorComponent :author="article.author" />

    <prev-next :prev="prev" :next="next" />
    
  </article>
</template>

<script>
import AuthorComponent from '../../components/AuthorComponent.vue'

  export default {
    components: { AuthorComponent },
    async asyncData({ $content, params }) {
      const article = await $content('articles', params.slug).fetch()

      const [prev, next] = await $content('articles')
        .only(['title', 'slug'])
        .sortBy('createdAt', 'asc')
        .surround(params.slug)
        .fetch()

      return {
        article,
        prev,
        next
      }
    },
    methods: {
        formatDate(date) {
            const options = { year: 'numeric', month: 'long', day: 'numeric' };
            return new Date(date).toLocaleDateString('en', options);
        }
    }
}
</script>

<style lang="scss">

.nuxt-content h2 {
  font-weight: bold;
  font-size: 28px;
}

.nuxt-content h3 {
  font-weight: bold;
  font-size: 22px;
}

.nuxt-content p {
  margin-bottom: 20px;
}
</style>

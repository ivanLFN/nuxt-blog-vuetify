<template>
    <div>
      <img :src="author.image" />
      <div>
        <h4>Author</h4>
        <p>{{ author.name }}</p>
        <p>{{ author.bio }}</p>
      </div>
      <NuxtLink :to="`/blog/author/${author.name}`">
        <img :src="author.img" />
        <div>
          <h4>Author</h4>
          <p>{{ author.name }}</p>
          <p>{{ author.bio }}</p>
        </div>
      </NuxtLink>
    </div>
</template>

<script>
  export default {
    props: {
      author: {
        type: Object,
        required: true
      }
    }
  }
</script>

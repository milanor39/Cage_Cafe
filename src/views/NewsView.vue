<template>
  <h2>NEWS</h2>
  <ul>
    <li v-for="i in 3" :key="i">
      <router-link :to="`/news/${i}`">/news/{{ i }}</router-link>
    </li>
  </ul>
</template>

<script>
export default {
  data () {
    return {}
  }
}
</script>

<template>
    <li>
        <div class="lightmeal-card">
            <img :src="img" :alt="name">
            <p>{{name}}</p>
            <p>${{price}}</p>
        </div>
    </li>
</template>

<script>
export default {
  props: [
    'name', 'price', 'img'
  ]
}
</script>

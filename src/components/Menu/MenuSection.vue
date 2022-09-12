<template>
    <li>
        <div class="lightmeal-card">
            <img :src="img" :alt="name">
                <p>{{name}}</p>
            <span>${{price}}</span>
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

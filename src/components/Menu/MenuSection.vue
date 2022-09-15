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
  props: {
    name: {
      type: String,
      required: true
    },
    price: {
      type: Number,
      required: true
    },
    img: {
      type: String,
      required: true
    }
  }
}
</script>

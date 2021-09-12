<template>
  <div class="home">
    <section class="hero is-medium is-dark mb-6">
    <div class="hero-body has-text-centered">
      <p class="title mb-6">
        Welcome to the ShoeStore. This is a demo website on django and vue
      </p>
      <p class="subtitle">
        Fun Project
      </p>
    </div>

    <div class="columns is-multiline">
      <div class="column is-12">
        <h2 class="is-size-2 has-text-centered">Latest Products</h2>
      </div>

      <div class="column is-3" v-for="product in LatestProducts" v-bind:key="product.id">
        <div class="box">
          <figure class="image mb-4">
            <img v-bind:src="product.get_thumbnail">
          </figure>

          <h3 class="is-size-4">{{ product.name }}</h3>
          <p class="is-size-6 has-text-grey">${{product.price}}</p>

          View Details
        </div>
      </div>
    </div>


    </section>
  </div>
</template>

<script>

export default {
  name: 'Home',
  components: {
    
  }
}
</script>

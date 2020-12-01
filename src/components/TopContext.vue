<template lang="pug">
  div
    div(class="topcontext")
      router-link(to="/").home__title
        | Vue.js Demo Store

      div(class="snipcart-summary")
        a(href="#" class="snipcart-checkout")
          | view cart (
          span(class="snipcart-total-items") 0
          | )

    p(class="notice")
      | Pre-Rendering with Vue.js Prerender SPA plugin, e-commerce with Snipcart

    <h1 v-if="seen">Rene</h1>
    <h1 v-else>buuuh</h1>
    <button :on-press="toggleSeen">Click to Toggle</button>

</template>

<script>
export default {
  name: 'TopContext'
}
</script>
<script>
export default {
  data() {
    return {
      seen: false
    };
  },
  toggleSeen() {
    this.seen = !this.seen;
  }
};
</script>

<style>
  .topcontext{
      padding-top: 20px;
      width: 100%;
      height: 100px;
      background-color: #212121;
      color: #FAFAFA;
      text-align: center;
      font-weight: bold;
      font-size: 25pt;
  }

  .notice{
    font-style: italic;
    font-size: 18pt;
    color: #212121;
    text-align: center;
  }

  .snipcart-summary{
    float: right;
    font-size: 20pt;
    padding-right: 30px;
    position: absolute;
    float: right;
    float: none;
    margin-left: 90%;
  }

  .home__title{
    text-decoration: none;
    color: white;
  }

  .snipcart-checkout{
    text-decoration: none;
    color: gray;
  }
</style>

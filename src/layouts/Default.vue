<template>
  <div class="layout">
    <bulma-nav/>
    <div class="container" id="topContainer">
      <slot/>
    </div>
  </div>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>
<script>
import BulmaNav from '~/components/bulma-nav'
export default {
  components: {
    BulmaNav
  } 
};
</script>

<style>
@import "https://cdnjs.cloudflare.com/ajax/libs/bulma/0.7.2/css/bulma.min.css";
/* Give the top a little more breathing room */
#topContainer{
  margin-top: 20px;
}
</style>

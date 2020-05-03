<template>
  <v-app>
    <div>
      <nuxt />
    </div>
  </v-app>
</template>

<script>
(function(w, d, s, l, i) {
  w[l] = w[l] || [];
  w[l].push({ "gtm.start": new Date().getTime(), event: "gtm.js" });
  var f = d.getElementsByTagName(s)[0],
    j = d.createElement(s),
    dl = l != "dataLayer" ? "&l=" + l : "";
  j.async = true;
  j.src = "https://www.googletagmanager.com/gtm.js?id=" + i + dl;
  f.parentNode.insertBefore(j, f);
})(window, document, "script", "dataLayer", "GTM-5DDZVKS");
</script>

<script
  async
  src="https://www.googletagmanager.com/gtag/js?id=UA-154217511-2"
></script>
<script>
window.dataLayer = window.dataLayer || [];
function gtag() {
  dataLayer.push(arguments);
}
gtag("js", new Date());

gtag("config", "UA-154217511-2");
</script>

<script>
export default {
  data() {
    return {};
  }
};
</script>

<style lang="scss">
html {
  font-family: "Times New Roman", Times, serif;
}
</style>

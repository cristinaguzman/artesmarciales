<template>
      <section class="bienvenida bg-dark2">
        <Welcome />
    </section>
</template>

<script>
import Welcome from '@/components/Welcome.vue'
export default {
  name: "home",
  components: {Welcome}
};
</script>

<style>
.bienvenida {
  display: flex;
  justify-content: center;
  vertical-align: middle;
  text-align: center;
  margin-top: 10%;
}

.bg-dark2 {
    background-color: #f7a0e1!important;
    font-family: 'Courier New', Courier, monospace;
}
</style>
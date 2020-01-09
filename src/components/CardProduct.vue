<template>
  <div class="my-card flex flex-center q-ma-sm">
    <q-card class="">
      <q-img class="imageProduct" src="https://cdn.quasar.dev/img/parallax2.jpg">
        <div class="text-subtitle2 absolute-top text-right text-orange withOutBg">
          <q-icon name="add_shopping_cart" />add
        </div>
      </q-img>
    </q-card>
    <span class="text-center text-semi-bold">Café 3 corações tradicional</span>
    <span class="text-center">R$ 5,99</span>
  </div>
</template>
<style scoped>

.text-semi-bold {
  font-weight: 500;
}
.my-card {
  width: 120px;
  /* height: 160px */
}

.imageProduct {
  width: 120px;
  height: 140px
}

.withOutBg {
  background: linear-gradient(to bottom, #00000070, transparent);
}
</style>
<script>
export default {

}
</script>

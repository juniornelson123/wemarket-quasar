<template>
  <q-page class="">
    <div class="col-6">
      <q-img
        class="imageBg"
        src="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcRYu8fbesH2CsVF_0V0Q7sZlxIf8I4-vZLsQ8YPWSCxFwGmDnMt"
        style="width: 100%"
      >
        <div class="column absolute-bottom text-subtitle1 withOutBg">
          <span class="col subtitleHeader">Quarta feira</span>
          <span class="col titleHeader">Dia da horta</span>
        </div>

      </q-img>
    </div>
    <q-tabs
      v-model="tab"
      dense
      class="text-grey bg-grey-3"
      active-color="orange"
      indicator-color="orange"
      align="justify"
      narrow-indicator
    >
      <q-tab style="font-size: 9px;" :ripple="false" class="labelStar" name="destack" icon="star" label="destaques" />
      <q-tab :ripple="false" class="labelStar" name="more" icon="bookmark" label="mais procurados" />
      <q-tab :ripple="false" class="labelStar" name="favorites" icon="favorite" label="selecionadas" />
    </q-tabs>
    <q-separator />
    <div class="row q-pa-sm listCards">
      <card-product />
      <card-product />
      <card-product />
      <card-product />
    </div>
  </q-page>
</template>
<style scoped>
.q-img__image {
  filter: blur(1px) !important;
}
.withOutBg {
  background: linear-gradient(to top, #00000070, transparent);
}
.subtitleHeader {
  font-size: 14px;
}

.titleHeader {
  font-size: 18px;
}

.listCards {
  justify-content: center;
}



</style>
<script>
import CardProduct from "../components/CardProduct";
export default {
  components: {
    CardProduct
  },
  name: 'PageIndex',
  data() {
    return {
      tab: 'destack'
    }
  },
}
</script>

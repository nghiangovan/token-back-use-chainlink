<template>
  <div class="content-my-products">
    <header-componet />
    <div class="div-show">
      <div class="strip-show">
        <div class="content-strip">
          <div class="row">
            <div class="col-12 col-sm-6 col-md-4" :span="6" v-for="item in itemsOf" :key="item.id">
              <ItemComponent
                :name="item.name"
                :price="item.price"
                :itemImg="item.imageUrl"
                :id="item.id"
                :type="item.id"
                :myProduct="true"
                :priceONEonUSD="priceONEonUSD"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import HeaderComponet from '@/components/HeaderComponent';
import ItemComponent from '@/components/ItemComponent.vue';
import { mapState, mapActions } from 'vuex';
export default {
  name: 'my-product',
  components: { HeaderComponet, ItemComponent },
  computed: {
    ...mapState(['account', 'itemsOf', 'priceONEonUSD'])
  },
  methods: {
    ...mapActions(['getItemsOf', 'loadWallet', 'initMarket', 'fetchPriceONEonUSD'])
  },
  async created() {
    await this.loadWallet();
    await this.initMarket();
    await this.fetchPriceONEonUSD();
    if (this.account) {
      await this.getItemsOf(this.account);
    }
  }
};
</script>

<style lang="scss">
.content-my-products {
  background: #eef2f7;
  min-height: 100vh;
}

.bottom-card > h5 {
  color: black;
}
</style>

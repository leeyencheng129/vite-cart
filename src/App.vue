<template>
  <div class="app-container">
    <h1>app</h1>
    <Header title="購物車案例"></Header>
    <Footer></Footer>
  </div>

</template>

<script>
import Header from './components/Header/Header.vue'
import Footer from './components/Footer/Footer.vue'

export default {
  name: 'myApp',
  data() {
    return {
      goodsList: []
    }
  },
  created() {
    this.getGoodsList()
  },
  methods: {
    async getGoodsList() {
      const { data: res } = await this.$http.get('/api/cart')
      if(res.status !== 200) return alert('failed')
      this.goodsList = res
    }
  },
  components: {
    Header,Footer
  }
}
</script>

<style lang="less">
.app-container {
  padding-top: 45px;
}
</style>
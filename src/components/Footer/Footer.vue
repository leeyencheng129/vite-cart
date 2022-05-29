<template>
  <div class="footer-container">
    <div class="form-check">
      <input class="form-check-input" type="checkbox" value="" id="fullCheck">
      <label class="form-check-label" for="fullCheck">
        全選
      </label>
    </div>

    <div>
      <span>合計：</span>
      <span class="amount">${{amount.toFixed(2)}}</span>
    </div>

    <button type="button" class="btn btn-primary myBtn" :disabled="total === 0">結算({{total}})</button>

  </div>

</template>

<script>
export default {
  name: 'Footer',
  props: {
    amount: {
      default: Number,
      default: 0
    },
    total: {
      default: Number,
      default: 0
    }
  }
}
</script>

<style lang="less" scoped>
.footer-container {
  position: fixed;
  bottom: 0;
  width: 100%;
  height: 50px;
  background: rgb(38, 176, 148);
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 10px;
}
.amount {
  font-weight: 500;
  color: red;
}
.myBtn {
  min-width: 90px;
  height: 39px;
  border-radius: 50px;
}
</style>
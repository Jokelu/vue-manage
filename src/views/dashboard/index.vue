<template>
  <div class="dashboard-container">
    <div class="dashboard-text">数组各种迭代</div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
// import { getInfo } from '@/api/user'
export default {
  name: 'Dashboard',
  computed: {
    ...mapGetters(['name'])
  },
  created() {
    this.arrayMap()
  },
  methods: {
    arrayMap() {
      const array = [1, 2, 3, 4, 5, 6, 7, 8]
      // for (let index = 0; index < array.length; index++) {
      //   const element = array[index]
      //   console.log(element)
      // }
      // array.forEach((item, index, array) => {
      //   if (item === 3) {
      //     throw new Error('报错')
      //   }
      //   console.log(item)
      // })
      // var newArr = array.filter((item, index) => item > 5)
      // console.log(newArr)
      // const newArr = array.map((item, index) => item + 2)
      // console.log(newArr)
      // var newArr = array.reduce((acc, item, index, array) => acc + item, 10)
      // console.log(newArr)
      // var newArr = array.some((item, index, array) => item > 6)
      // console.log(newArr)
      // var newArr = array.every((item, index, array) => item > 0)
      // console.log(newArr)
      // var newArr = array.find((item, index, array) => item > 2)
      // console.log(newArr)
      var newArr = array.findIndex((item, index, array) => item > 4)
      console.log(newArr)
      const obj = {}
      Object.defineProperty(obj, 'name', {
        configurable: false,
        enumerable: true,
        value: 'dada',
        writable: false
      })
      obj.name = 'dadada'
      console.log(obj.name)
    }
  }
}
</script>

<style lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}
</style>

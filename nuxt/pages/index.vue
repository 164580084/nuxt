<template>
  <div>
    weriowerojwernmms

    <banner :listImg="listImg"></banner>



  </div>
</template>

<script>
  //轮播图
  import banner from '~/components/banner/banner'
  export default {
    name: "index",
    data() {
      return {
        listImg:true
      }
    },

    mounted() {

    },
    methods:{
      tap(){
        this.$router.push('/two')
      }
    },
    components:{
      banner
    }
  }
</script>

<style lang="less" scoped>

</style>

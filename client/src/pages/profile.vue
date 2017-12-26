<template>
  <div class="profile">
    我的页面
  </div>
</template>

<script>
  import { mapState, mapMutations } from "vuex";
  export default {
    name: 'Profile',
    data() {
      return {

      }
    },
    computed: {
      ...mapState([
        'isLogin',
        'userInfo'
      ])
    },
    mounted(){
      if (!this.isLogin) {
        this.$router.push({path: '/login'})
        console.log(this.$route)
      }
    }
  }
</script>

<style scoped>

</style>



<template>
</template>
<script>
var frontpage = "FrontPage" //env로 설정하게 바꿀예정
export default {
  mounted() {
    this.$router.push('/w/'+frontpage);
  }
}
</script>
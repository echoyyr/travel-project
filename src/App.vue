<template>
  <div id="app">
    <keep-alive exclude="Detail">
    </keep-alive>
<!--    显示的是当前路由地址所对应的内容-->
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>

</style>

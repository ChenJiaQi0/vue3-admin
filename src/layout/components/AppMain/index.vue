<template>
  <div class="app-main">
    <router-view v-slot="{ Component, route }">
      <transition name="fade-transform" mode="out-in">
        <keep-alive>
          <component :is="Component" :key="route.path" />
        </keep-alive>
      </transition>
    </router-view>
  </div>
</template>

<script setup>
import {} from 'vue'
</script>

<style lang="scss" scoped>
.app-main {
  min-height: calc(100vh - 50px - 43px);
  padding: 104px 20px 20px 20px;
  width: 100%;
  position: relative;
  overflow: hidden;
  padding: 100px 20px 20px 20px;
  box-sizing: border-box;
}
</style>

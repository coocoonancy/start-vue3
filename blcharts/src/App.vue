<script setup>
import components from "./components";
</script>

<template>
  <div id="app">
    <component
      :is="componentId"
      :pid="pid"
      :did="did"
      :type="type"
      :mode="mode"
      :parentbusiness="parentbusiness"
      :business="business"
      :allChecked="allChecked"
      :externalInfo="externalInfo"
      :filterAble="false"
    ></component>
  </div>
</template>

<style scoped></style>

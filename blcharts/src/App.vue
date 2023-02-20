<script setup>
import components from './components'
import { shallowRef, ref } from 'vue'
const pid = ref('00000000000000000000000071140100')
const did = ref('100071140100000000003ba443d82327')
const type = ref('cardmode')
const mode = ref('detail')
const allChecked = ref(false)
const parentbusiness = ref('') // '1000348901000000000000b81f9e9376'
const business = ref('') // 10003489010000000000b9a4083a8156
const externalInfo = ref({
  isFilterExcludesParentBusiness: true
})
const componentsRef = {
  ...components
}
let componentId = ref(shallowRef(componentsRef['DiankyAuth']))
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

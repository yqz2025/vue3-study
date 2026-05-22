<script setup lang="ts">
function clickButton(e: Event) {
  console.log('点击了按钮');
}
function clickButton1(name: string, e: Event) {
  console.log('点击了按钮', name, e);
}
function dblclickButton2(name: string, e: Event) {
  console.log(name, e);
}
function rightclickButton3(name: string, e: Event) {
  console.log("点击了右键",name, e);

}

</script>

<template>
<div>
  事件绑定
  <div>点击事件<button @click="clickButton">点击我</button></div>
  <div>点击事件<button @click="clickButton1('---单击', $event)">点击我</button></div>
  <div>点击事件<button @dblclick="dblclickButton2('---双击', $event)">点击我</button></div>
  <div>点击事件<button @click.right="rightclickButton3('---右击', $event)">点击我</button></div>
</div>
</template>

<style scoped></style>

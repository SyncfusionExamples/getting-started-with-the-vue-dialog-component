<script setup>
import {DialogComponent as EjsDialog} from '@syncfusion/ej2-vue-popups';
import {ref} from 'vue';
const visible = ref(true);
const dlgBtnClick = () => {
  visible.value = false
};
const buttons = [{click: dlgBtnClick, buttonModel: {content: 'Cancel'}}];
const handleClick = () => {
  visible.value = true
};
const position = {X:'center',Y:'center'};
const resizeHandles = ['All'];
const animation = {effect:'FlipXUp'};
</script>

<template>
<button class="e-btn" @click="handleClick">Open Dialog</button>
<ejs-dialog height="160px" width="350px"
header="Dialog" content="This is a Dialog with content"
:buttons="buttons" :visible="visible"
showCloseIcon="true" :position="position"
allowDragging="true"  enableResize="true"
:resizeHandles="resizeHandles" :animationSettings="animation"
isModel="true">
</ejs-dialog>
</template>

<style scoped>
@import "../node_modules/@syncfusion/ej2-base/styles/material.css";
@import "../node_modules/@syncfusion/ej2-popups/styles/material.css";
@import "../node_modules/@syncfusion/ej2-buttons/styles/material.css";
</style>


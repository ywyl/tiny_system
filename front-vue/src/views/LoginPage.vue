<template>
  <div class="background">
    <div class="left-pic"></div>
    <div class="right-login">
      <ElForm label-position="top">
        <ElFormItem label="Account">
          <ElInput v-model="account" />
        </ElFormItem>
        <ElFormItem label="Password">
          <ElInput v-model="password" />
        </ElFormItem>
      </ElForm>
			<ElButton type="primary" class="sign-button">Sign in</ElButton>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const account = ref<string>('');
const password = ref<string>('');
</script>

<style lang="scss">
.background {
  box-sizing: border-box;
  margin: 1rem;
  background-color: #f5f5f5;
  border: 1px solid red;
  height: calc(100vh - 2rem);
  display: flex;

  .left-pic {
    flex: 2;
    height: 100%;
    background-color: skyblue;
  }

  .right-login {
    flex: 1;
    height: 100%;
    background-color: pink;

		.sign-button {
			width: 100%;
		}
  }
}
</style>

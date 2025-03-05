<template>
	<view>
		<childVue :msg="msg"></childVue>
		<childVue></childVue>
		{{msg}}
	</view>
</template>

<script setup>
import { ref } from 'vue';
import childVue from '@/components/child.vue';
const msg = ref('父组件参数');
</script>

<style></style>

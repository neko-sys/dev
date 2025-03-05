<template>
	<view>
		displayMsg : {{ displayMsg }}
		msg : {{msg}}
	</view>
</template>

<script setup>
import { defineProps, onMounted, ref, toRef } from 'vue';

// 正确定义 props 和默认值
const props = defineProps({
	msg: {
		type: String,
		default: '子组件参数'
	}
});

// 使用 ref 创建一个本地响应式变量，而不是直接修改 prop
const displayMsg = toRef(props.msg);

onMounted(() => {
	displayMsg.value = '114514'; // 修改本地变量而不是 prop
});
</script>

<style></style>

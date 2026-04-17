<template>
	<div>
		<div class="flex w-full">
			<div v-for="(item, index) in data.results" :key="index">
				<img :src="item.image" alt="" />
				<p>{{ item.name }}</p>
			</div>
		</div>
	</div>
</template>

<script lang="ts" setup>
const { data, status, error, refresh, clear } = await useFetch(
	"https://rickandmortyapi.com/api/character",
);
console.log(data.value);
</script>

<template>
	<TaskHw />
	<IndexPage/>
	<BlogPage/>
	<BlogDetailsPage/>
</template>

<script>
import IndexPage from './components/IndexPage.vue';
import BlogPage from './components/BlogPage.vue';
import BlogDetailsPage from './components/BlogDetailsPage.vue';
import TaskHw from './components/TaskHw.vue';

export default { 
	components: {
		IndexPage,
		BlogPage,
		BlogDetailsPage,
		TaskHw
	},
};
</script>

<style lang="scss">
</style>

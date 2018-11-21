<template>
	<div class='clist'>
		<cmit v-for='c in comments' :comment='c' :key='c.id' @shanchuwo='doDelete'>
		</cmit>
	</div>
</template>

<script>
	import commentItem from './comment-item.vue';

	export default {
		props: ['comments'],
		methods: {
			doDelete(id) {
				this.$emit('shanchuwo', id);
			}
		},
		components: {
			cmit: commentItem
		}
	}
</script>

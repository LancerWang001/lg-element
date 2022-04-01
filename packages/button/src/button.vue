<template>
	<div>
		<button v-bind="$attrs" @click="handleClick"><slot /></button>
	</div>
</template>

<script>
export default {
	name: 'LgButton',
	inheritAttrs: false,
	methods: {
		handleClick (evt) {
			this.$emit('click', evt)
			evt.preventDefault()
		}
	}
}
</script>

<style lang="scss" scoped>

</style>

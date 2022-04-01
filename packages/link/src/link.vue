<template>
	<a
		:href="disabled ? null : href"
		:class="{ disabled, 'no-underline': !underline }"
	>
		<slot />
	</a>
</template>

<script>
export default {
	name: 'LgLink',
  props: {
    href: {
			type: String,
		},
		disabled: {
			type: Boolean,
			default: false
		},
		underline: {
			type: Boolean,
			default: false
		}
  }
}
</script>

<style scoped>
.disabled {
	cursor: pointer;
}
.no-underline {
	text-decoration: none;
}
</style>

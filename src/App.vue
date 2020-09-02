<template>
	<div class="container-fluid"> 
		<div class="row">
			<div class="col-md-3">
				<vertical-sidebar></vertical-sidebar>
			</div>
			<div class="col-md-9">
				<main-content></main-content>
			</div>
		</div>
	</div>
</template>

<script>
import MainContent from './components/MainContent.vue'
import VerticalSidebar from './components/VerticalSidebar.vue'
export default {
	components: { VerticalSidebar, MainContent }
}
</script>

<style>
.container-fluid {
	padding: 0 !important;
	overflow: hidden;
	height: 100vh;
}
.col-md-9 {
  padding: 0px !important;
}
</style>

<template>
	<div class="container-fluid"> 
		<div class="row">
			<div class="col-md-3 position-fixed">
				<vertical-sidebar></vertical-sidebar>
			</div>
      <div class="col-md-3">
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
	height: 100vh;
}
.row {
  margin: 0 !important;
}
.position-fixed {
  padding: 0px !important;
}
.col-md-9 {
  margin-left: 25vw !important;
  padding: 0px !important;
}
</style>

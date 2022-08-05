<template>
	<div class="entry-title d-flex justify-content-between p-2">
		<div>
			<span class="text-sucess fs-3 fw-bold">15</span>
			<span class="mx-1 fs-3">Julio</span>
			<span class="mx-2fs-4 fw-light">2022, Domingo</span>
		</div>

		<div>
			<button class="btn btn-danger mx-2">
				Borrar
				<i class="fa fa-trash-alt"></i>
			</button>

			<button class="btn btn-primary">
				Subir Foto
				<i class="fa fa-upload"></i>
			</button>
		</div>
	</div>

	<hr />

	<div class="d-flex flex-column px-3 h-75">
		<textarea placeholder="Que sucedio hoy?"></textarea>
	</div>

	<fab v-bind:icon="'fa-save'" />

	<img
		src="https://media.istockphoto.com/photos/taj-mahal-mausoleum-in-agra-picture-id1146517111?k=20&m=1146517111&s=612x612&w=0&h=vHWfu6TE0R5rG6DJkV42Jxr49aEsLN0ML-ihvtim8kk="
		alt="entry-image"
		class="img-thumbnail"
	/>
</template>

<script>
	import { defineAsyncComponent } from 'vue';

	export default {
		components: {
			Fab: defineAsyncComponent(() => import('../components/Fab.vue')),
		},
	};
</script>

<style lang="scss" scoped>
	textarea {
		border: none;
		font-size: 20px;
		height: 100%;
		&:focus {
			outline: none;
		}
	}

	img {
		width: 200px;
		position: fixed;
		bottom: 150px;
		right: 20px;
		box-shadow: 0px 5px 10px rgba($color: #000000, $alpha: 0.2);
	}
</style>

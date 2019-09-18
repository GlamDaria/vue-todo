<template>
<div>
	<div class="form-group">
		<label>Song Author</label>
		<input type="text" class="form-control" v-model="author">
	</div>
	<div class="form-group">
		<label>Song Name</label>
		<input type="text" class="form-control" v-model="name">
	</div>
	<button class="btn btn-dark" @click="sendSong">Add Your Super Song (by Adam Lambert)</button>
</div>
</template>
<script>
	export default{
		data(){
			return{
				name: '',
				author: ''
			}
		},
		methods:{
			sendSong(){
				let song = {
					name : this.name,
					singer : this.author
				};
				this.$emit('sendSongToTheApp', song);
				console.log(song)
			}
		}
	}
</script>
<template>
	<div class="mt-5 d-flex justify-content-between flex-wrap">
		<div v-for="song in displaySongs" class="card text-white bg-dark mb-3" style="min-width: 288px;">
 			<div class="card-header">New Song</div>
  			<div class="card-body">
   				<h5 class="card-title">{{song.name}}</h5>
    			<h6 class="card-subtitle text-muted">{{song.singer}}</h6>
  			</div>
		</div>
	</div>
</template>
<script>
	export default{
		props:{
			displaySongs : Array
		}
	}
</script>
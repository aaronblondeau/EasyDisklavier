<div class="play cell">
	<div on:click={handleClick}>
		Play
		<svg xmlns="http://www.w3.org/2000/svg" width="256" height="256" fill="currentColor" class="bi bi-play" viewBox="0 0 16 16">
			<path d="M10.804 8 5 4.633v6.734L10.804 8zm.792-.696a.802.802 0 0 1 0 1.392l-6.363 3.692C4.713 12.69 4 12.345 4 11.692V4.308c0-.653.713-.998 1.233-.696l6.363 3.692z"/>
		</svg>
	</div>
</div>

<script>
	export let baseUrl
	function handleClick() {
		// This plays the first stong on the USB Drive
		// To just issue a standard play command use : /ctrl/setSeq.php?status=play
		const url = baseUrl + 'ctrl/setSong.php?prefix=s&song_id=1'
		fetch(url)
	}
</script>

<style lang="css">
.play>div {
	cursor: pointer;
	background-color: rgb(50, 255, 118);
	font-size: 5em;
	width: 100%;
	display: flex;
    justify-content: center;
    align-items: center;
	font-family: sans-serif;
	flex-direction: column;
}
</style>

<div class="pause cell">
	<div on:click={handleClick}>
		Pause
        <svg xmlns="http://www.w3.org/2000/svg" width="256" height="256" fill="currentColor" class="bi bi-stop" viewBox="0 0 16 16">
            <path d="M3.5 5A1.5 1.5 0 0 1 5 3.5h6A1.5 1.5 0 0 1 12.5 5v6a1.5 1.5 0 0 1-1.5 1.5H5A1.5 1.5 0 0 1 3.5 11V5zM5 4.5a.5.5 0 0 0-.5.5v6a.5.5 0 0 0 .5.5h6a.5.5 0 0 0 .5-.5V5a.5.5 0 0 0-.5-.5H5z"/>
        </svg>
	</div>
</div>

<script>
	export let baseUrl
	function handleClick() {
		const url = baseUrl + 'ctrl/setSeq.php?status=pause'
		fetch(url)
	}
</script>

<style lang="css">
.pause>div {
	cursor: pointer;
	background-color: rgb(253, 92, 92);
	font-size: 5em;
	width: 100%;
	display: flex;
    justify-content: center;
    align-items: center;
    font-family: sans-serif;
    flex-direction: column;
}
</style>

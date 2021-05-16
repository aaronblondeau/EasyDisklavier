<div class="next cell">
	<div on:click={handleClick}>
		Next
        <svg xmlns="http://www.w3.org/2000/svg" width="256" height="256" fill="currentColor" class="bi bi-arrow-right" viewBox="0 0 16 16">
            <path fill-rule="evenodd" d="M1 8a.5.5 0 0 1 .5-.5h11.793l-3.147-3.146a.5.5 0 0 1 .708-.708l4 4a.5.5 0 0 1 0 .708l-4 4a.5.5 0 0 1-.708-.708L13.293 8.5H1.5A.5.5 0 0 1 1 8z"/>
        </svg>
	</div>
</div>

<script>
	export let baseUrl
	function handleClick() {
		const url = baseUrl + 'ctrl/setSong.php?control=next'
		fetch(url)
	}
</script>

<style lang="css">
.next>div {
	cursor: pointer;
	background-color: rgb(162, 142, 253);
	font-size: 5em;
	width: 100%;
	display: flex;
    justify-content: center;
    align-items: center;
	font-family: sans-serif;
    flex-direction: column;
}
</style>
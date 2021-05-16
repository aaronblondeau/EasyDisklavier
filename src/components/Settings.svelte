<div class="settings">
	<div on:click={handleClick}>Settings</div>
</div>

<script>
export let baseUrl
function handleClick() {
    var newBaseUrl = prompt('Piano Address (include protocol and trailing /)', baseUrl)
    localStorage.setItem('baseUrl', newBaseUrl)
}
</script>

<style lang="css">
.settings {
    width: 100%;
    height: 20px;
    background-color: black;
}
</style>

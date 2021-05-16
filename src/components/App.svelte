<div class="app">
	<main class="wrapper">
		<div class="row">
			<Play baseUrl={baseUrl} />
			<Pause baseUrl={baseUrl} />
		</div>
		<div class="row">
			<Back baseUrl={baseUrl} />
			<Next baseUrl={baseUrl} />
		</div>
		<Settings baseUrl={baseUrl} />
	</main>
</div>

<script>
	import Play from '@components/Play';
	import Pause from '@components/Pause';
	import Next from '@components/Next';
	import Back from '@components/Back';
	import Settings from '@components/Settings';

	let baseUrl=localStorage.getItem('baseUrl')  || "http://192.168.88.1/"

	window.addEventListener('storage', (e) => {
		if (e.key === 'baseUrl' && e.newValue === null) {
			baseUrl=e.newValue
		}
	})
</script>

<style lang="css">

</style>

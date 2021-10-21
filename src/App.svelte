<script>
	import TodoCard from "./ToDoCard.svelte";
	let toDo = ["Pelatihan", "Kunjungan"];
	let inProgress = ["Pelatihan"];
	let done = ["Rapat Bulanan"];
</script>

<div class="container is-fluid">
	<h1 class="is-size-3">Daftar Kegiatan Bulanan</h1>
	<h2 class="is-size-5">Bulan Oktober Tahun 2021</h2>
	<hr />
	<div class="columns">
		<div class="column is-4">
			<div class="card has-background-light">
				<div class="card-header">
					<div class="card-header-title">Rencana kegiatan</div>
				</div>
				<div class="card-content">
					{#each toDo as toDo}
						<TodoCard content={toDo} />
					{/each}
					<input type="text" class="input is-primary mb-1" />
					<button class="button is-primary">Tambah Kegiatan</button>
				</div>
			</div>
		</div>
		<div class="column is-4">
			<div class="card has-background-light">
				<div class="card-header">
					<div class="card-header-title">
						Kegiatan sedang berlangsung
					</div>
				</div>
				<div class="card-content">
					{#each inProgress as inProgress}
						<TodoCard content={inProgress} />
					{/each}
				</div>
			</div>
		</div>
		<div class="column is-4">
			<div class="card has-background-light">
				<div class="card-header">
					<div class="card-header-title">Kegiatan telah selesai</div>
				</div>
				<div class="card-content">
					{#each done as done}
						<TodoCard content={done} />
					{/each}
				</div>
			</div>
		</div>
	</div>
</div>

<svelte:head>
	<link rel="stylesheet" href="/build/bulma.min.css" />
	<link rel="stylesheet" href="/build/custom.css" />

	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
	<link
		href="https://fonts.googleapis.com/css2?family=Racing+Sans+One&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

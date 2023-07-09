<script>
	import '../app.postcss';
</script>

<svelte:head>
	<title>Hello</title>
	<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css" />
</svelte:head>

<section class="h-[100vh] w-full flex bg-black">
	<div class="h-full w-1/5 border-white border-2 text-white  ">
		<a href="#/home">Home</a>
		<a href="#/khedma">khedma</a>
		<a href="#/about">about</a>
		<a href="#/contact">Contact</a>
	</div>
	<slot />
</section>

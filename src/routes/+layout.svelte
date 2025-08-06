<script lang="ts">
    import '../app.css';
    import favicon from '$lib/assets/favicon.svg';
    import Header from '$lib/components/Header.svelte';
    let { children } = $props();
</script>

<svelte:head>
    <link rel="icon" href={favicon} />
</svelte:head>

<Header />
<main class="mt-14 mx-4">
    {@render children?.()}
</main>
<!-- </script> -->
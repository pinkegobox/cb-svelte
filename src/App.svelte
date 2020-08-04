<script>
	import AnnouncementBar from './AnnouncementBar.svelte';
	import Modal from './Modal.svelte';
	import Header from './Header.svelte';
	import Main from './Main.svelte';
	import Footer from './Footer.svelte';

	let isBarVisible = true;

    const handleClick = () => {
        alert('you clicked the bar');
        isBarVisible = false;
        localStorage.setItem("isBarVisible", false);
    }

    if (localStorage.getItem("isBarVisible")) {
        isBarVisible = false;
    }
</script>

{#if isBarVisible}
	<AnnouncementBar {handleClick}/>
{:else}
	<div></div>
{/if}


<Modal />
<Header />
<Main />
<Footer />
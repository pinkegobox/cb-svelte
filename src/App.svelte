<script>
	import AnnouncementBar from './AnnouncementBar.svelte';
	import Modal from './Modal.svelte';
	import Header from './Header.svelte';
	import Main from './Main.svelte';
	import Footer from './Footer.svelte';

	let isBarVisible = true;
	let isModalVisible = true;

    const handleBarClick = () => {
        alert('you clicked the bar');
        isBarVisible = false;
        localStorage.setItem("isBarVisible", false);
	}
	
	const handleModalClick = () => {
        alert('you clicked the modal');
        isModalVisible = false;
        localStorage.setItem("isModalVisible", false);
    }

    if (localStorage.getItem("isBarVisible")) {
        isBarVisible = false;
	}
	
	 if (localStorage.getItem("isModalVisible")) {
		isModalVisible = false;
    }
</script>

{#if isBarVisible}
	<AnnouncementBar {handleBarClick}/>
{:else}
	<div></div>
{/if}

{#if isModalVisible}
	<Modal {handleModalClick}/>
{:else}
	<div></div>
{/if}

<Header />
<Main />
<Footer />
<script>
	import AnnouncementBar from './AnnouncementBar.svelte';
	import Modal from './Modal.svelte';
	import Header from './Header.svelte';
	import Main from './Main.svelte';
	import Footer from './Footer.svelte';

	let isBarVisible = true;
	let isModalVisible = true;

	//once user clicks element, data about the user's visit is stored on their browser through localStorage
    const handleBarClick = () => {
        isBarVisible = false;
        localStorage.setItem("isBarVisible", false);
	}

	const handleModalClick = () => {
        isModalVisible = false;
        localStorage.setItem("isModalVisible", false);
    }
	
	//checks if string of false exists to indicate whether the user has visited the page & interacted with the bar and modal before
  	//if the user has, then update isBarVisible and/or isModalVisible to false to prevent announcement bar & modal from appearing again
    if (localStorage.getItem("isBarVisible") === 'false') {
        isBarVisible = false;
	}
	
	if (localStorage.getItem("isModalVisible") === 'false') {
		isModalVisible = false;
	}
</script>

<style>
.overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.3);
  z-index: 99;
}
</style>

<!-- show transparent overlay effect over entire page if modal is visible -->
<!-- dismiss modal if user clicks outside of it -->
{#if isModalVisible} 
	<div class="overlay" on:click={handleModalClick} />
{:else}
	<div></div>
{/if}

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
<script>
	import AnnouncementBar from './AnnouncementBar.svelte';
	import Modal from './Modal.svelte';
	import Header from './Header.svelte';
	import Main from './Main.svelte';
	import Footer from './Footer.svelte';
	import {clickOutside} from './clickOutside.js';

	let isBarVisible = true;
	let isModalVisible = true;

    const handleBarClick = () => {
        isBarVisible = false;
        localStorage.setItem("isBarVisible", false);
	}
	
	const handleModalClick = () => {
        isModalVisible = false;
        localStorage.setItem("isModalVisible", false);
    }

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

{#if isModalVisible} 
	<div class="overlay" use:clickOutside on:click={handleModalClick} />
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
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

    if (localStorage.getItem("isBarVisible") === 'false') {
		console.log(localStorage.getItem("isBarVisible"))
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
	<div class="overlay" />
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
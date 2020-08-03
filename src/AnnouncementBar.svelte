<script>
    import CloseButton from './CloseButton.svelte';
</script>

<style>
    .container {
    background-color: #545759;
    color: #fff;
    font-weight: bold;
    font-size: 1.4rem;
    text-align: center;
    letter-spacing: 1px;
    padding: 1.2rem 0;
    position: relative;
    z-index: 1;
}

:global([ref=barClose]) {
    background-color: rgba(0,0,0,.15);
    height: 100%;
    width: 3.5rem;
}
</style>


<div class="container">
    <CloseButton ref="barClose"/>
    <p>
        <span role="img" aria-label="confetti emoji">🎉</span>See us in the press: Furniture Today, Business of Home, and Causal
        Living
    </p>
</div>
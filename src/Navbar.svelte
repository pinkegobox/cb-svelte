<script>
    import NavLinks from './NavLinks.svelte';
    import Button from './Button.svelte';
</script>

<style>
.logo {
    height: auto;
    width: 31rem;
}

.flexContainer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: relative;
    z-index: 1;
    padding: 2rem;
    font-weight: 500;
}
</style>

<nav class="flexContainer">
    <div>
        <a href="/">
        <img src="/assets/logo.png" class="logo" alt="CommerceBear Logo" />
        </a>
    </div>
    <div class="flexContainer">
        <NavLinks />
        <Button text={"Get Started"} url={"https://commercebear.com/getstarted"} padding="1.5rem 2rem" />
    </div>
</nav>
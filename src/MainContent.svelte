<script>
    import Features from './Features.svelte';
    import Button from './Button.svelte';
</script>

<style>
.container {
    padding: 96px 32px;
    color: #545759;
}

.container > *:not(:last-child) {
    margin-bottom: 2.5rem;
}

.desc {
    padding: 0 3rem;
}

h2 {
    line-height: 1.3;
    margin-bottom: 3rem;
}

.horizontalRule {
    margin: 5rem 0;
    border: none;
    background-color: rgba(84,87,89,.15);
    height: 1px;
}

.learnMore {
    margin: 5rem 0;
}

.learnMore h2 {
    margin-bottom: 5rem;
}
</style>

<main class="wrapper container">
    <div class="desc">
        <h2>
            Generate new revenue, profits, and establish an effective
            omni-channelbusiness.
        </h2>
        <h2>Over 53,720 furniture SKUs published.</h2>
    </div>
    <img src="/assets/ecommerce.png" alt="omni-channel marketing strategy" />
    <h2>
        Designed to drive sales and automate operations.
    </h2>
    <Features />
    <hr class="horizontalRule" />
    <div class="learnMore">
        <h2>
            From start to scale, say hello to your next chapter of growth.
        </h2>
        <Button text="Talk to us to learn more" padding="2rem 3rem" url="https://calendly.com/sam-bear/30min?back=1&month=2020-08"/>
    </div>
</main>
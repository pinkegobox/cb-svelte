<script>
	import FeatureItem from './FeatureItem.svelte';
</script>

<style>
.list {
    margin-top: 4rem;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-column-gap: 5px;
    grid-row-gap: 5px;
}

.list > * {
    text-align: left;
}

.list > li {
    display: flex;
    padding: 1.7rem;
}

.list p {
    line-height: 1.5;
}

.list img {
    width: 8rem;
    margin-right: 1.5rem;
}

.list h3 {
    font-size: 2.5rem;
    margin-bottom: 0.5rem;
}
</style>

<ul class="list">
    <FeatureItem
        fileName="multichannel.jpeg"
        title="Multi Channel Publishing"
        desc="Fully built-out product data and content deployed to all channels"
    />
    <FeatureItem
        fileName="inventory-app.png"
        title="Inventory App"
        desc="Automated multi-marketplace inventory management"
    />
    <FeatureItem
        fileName="automated-promotions.png"
        title="Automated Promotions"
        desc="Full setup and optimization of unpaid promotions across all channels"
    />
    <FeatureItem
        fileName="support-plus.png"
        title="Support Plus"
        desc="Troubleshooting, insight, and best practices to help you scale"
    />
    <FeatureItem 
        fileName="channel-setup.png" 
        title="Channel Setup"
        desc="Streamlined marketplace onboarding"
    />
</ul>
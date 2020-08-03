<script>
    import Icon from 'fa-svelte';
    export let iconName;
    export let url;
    export let text;
</script>

<style>
.socialLinks > *:not(:last-child) {
    margin-right: 0.6rem;
}
</style>

<a
    href={url}
    target="_blank"
    rel="noopener noreferrer"
    aria-label={`Visit us at our ${text} account (opens in a new tab)`}
>
    <Icon icon={iconName}></Icon>
</a>
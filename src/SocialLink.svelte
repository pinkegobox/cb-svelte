<script>
    import Icon from 'fa-svelte';
    export let iconName;
    export let url;
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
    aria-label="This is an external link (opens in a new tab)"
>
    <Icon icon={iconName}></Icon>
</a>
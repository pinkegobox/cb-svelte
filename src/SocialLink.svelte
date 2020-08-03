<script>
    import Icon from 'fa-svelte';
    export let iconName;
</script>

<a
    href="/"
    target="_blank"
    rel="noopener noreferrer"
    aria-label="This is an external link (opens in a new tab)"
>
    <Icon icon={iconName}></Icon>
</a>
<script>
    export let text;
    export let url;
    export let padding;
</script>

<style>
.btn {
    color: #fff;
    background-color: rgba(46,25,112,.63);
    border-radius: 300px;
    letter-spacing: 2px;
    font-weight: 500;
}
</style>

<a href={url} class="btn" style="padding: {padding}">
    {text}
</a>
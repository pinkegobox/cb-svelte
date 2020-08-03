<script>
    export let fileName;
    export let title;
    export let desc;
</script>

<style>
.desc {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
}
</style>

<li>
    <img src={`/assets/${fileName}`} alt={`${title} icon`} />
    <div class="desc">
        <h3>{title}</h3>
        <p>{desc}</p>
    </div>
</li>
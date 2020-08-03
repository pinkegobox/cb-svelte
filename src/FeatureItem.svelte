<script>
    export let fileName;
    export let title;
    export let desc;
</script>

<style>
li {
    display: flex;
    padding: 1.7rem;
    text-align: left;
}

p {
    line-height: 1.5;
}

img {
    width: 8rem;
    margin-right: 1.5rem;
}

h3 {
    font-size: 2.5rem;
    margin-bottom: 0.5rem;
}

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
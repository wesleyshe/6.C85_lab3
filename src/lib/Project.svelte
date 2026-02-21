<script>
    export let data = {};
</script>

<article>
    <img src={data.image} alt={data.title} />
    <h3>{data.title}</h3>
    <p>{data.description}</p>
</article>

<style>
    article {
        display: grid;
        grid-template-rows: subgrid;
        grid-row: span 3;
    }
    article img {
        grid-row: 1;
        width: 100%;
        height: 220px;
        object-fit: cover;
        display: block;
    }
    article h3 {
        grid-row: 2;
        margin: 0;
    }
    article p {
        grid-row: 3;
    }
</style>

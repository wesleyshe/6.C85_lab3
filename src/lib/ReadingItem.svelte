<script>
    export let data = {};
</script>

<article>
    <img src={data.image} alt="Cover of {data.title}" />
    <div class="details">
        <h3>
            {#if data.link}
                <a href={data.link} target="_blank">{data.title}</a>
            {:else}
                {data.title}
            {/if}
        </h3>
        <p class="author">
            {data.author}{#if data.year}
                · {data.year}{/if}
        </p>
        {#if data.description}
            <p class="desc">{data.description}</p>
        {/if}
    </div>
</article>

<style>
    article {
        display: flex;
        gap: 1em;
        align-items: flex-start;
    }
    article img {
        width: 80px;
        height: 110px;
        object-fit: cover;
        flex-shrink: 0;
        border-radius: 3px;
        box-shadow: 2px 2px 6px oklch(0% 0 0 / 25%);
    }
    .details {
        display: flex;
        flex-direction: column;
        gap: 0.25em;
    }
    h3 {
        margin: 0;
        font-size: 1rem;
        line-height: 1.3;
    }
    .author {
        margin: 0;
        font-size: 0.875rem;
        font-style: italic;
        opacity: 0.7;
    }
    .desc {
        margin: 0;
        font-size: 0.85rem;
        opacity: 0.85;
    }
</style>

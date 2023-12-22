<script>
    /**
   * @type {{ title: string; items: Array<{text: string, subitem?: string}>; }}
   */
    export let content;
</script>


<section class="resume-section">
    <h3 class="title">{content.title}</h3>
    <ul class="section-items">
        {#each content.items as item}
        <li class="item">
            {item.text}
			{#if item.subitem}
                <p class="subitem">{item.subitem}</p>
            {/if}
        </li>
        {/each}
    </ul>
</section>

<style>
    .resume-section {
        padding: 0 var(--container) 32px;
    }

    .resume-section .title {
        font-size: 1.5rem;
        margin: 0 0 16px;
    }

    .resume-section .section-items {
        margin: 0;
        padding: 0;
        list-style: none;
    }

    .resume-section .section-items .item {
        font-size: 1.25rem;
        font-weight: 500;
        margin-top: 8px;

    }

    .resume-section .section-items .item .subitem{
        font-size: 1.125rem;
        display: block;
        width: 100%;
        margin: 0 0 8px;
    }
</style>

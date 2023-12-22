<script>
    import Contact from './contact.svelte';

    let textSummary = "Graduada em Ciência da Computação, atua em desenvolvimento web há quatro anos, principalmente como Front-end. Tem experiência ampla com React e WordPress, entre outras linguagens e frameworks. Interessada também em acessibilidade na web."
</script>

<section class="summary">
    <p class="text">{textSummary}</p>
    <Contact />
</section>

<style>
    .summary {
        display: flex;
        padding: 0 var(--container) 32px;
    }

    @media (max-width: 1024px) {
        .summary {
            flex-direction: column-reverse;
        }
    }
    .summary .text {
        margin: 0 32px 0 0;
        font-size: 1.25rem;
    }
</style>

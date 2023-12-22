<script>
    import {contacts} from "../objects"
</script>

<div class="contact-container">
    <ul class="contacts">
        {#each contacts as { icon, text, link }}
            <li class="item">
                <img class="icon" src={icon.src} alt={icon.alt} />
                <a class="link" href={link} rel="noopener" target="_blank">{text}</a>
            </li>
        {/each}
    </ul>
</div>

<style>
    .contact-container {
        background-color: var(--color-background);
        transform: translateY(-40px);
    }

    .contact-container .contacts {
        margin: 0;
        padding: 0;
        list-style: none;
    }

    .contact-container .contacts .item {
        display: flex;
        justify-content: flex-start;
        align-items: center;
    }
    .contact-container .contacts .icon {
        width: 24px;
        height: 24px;
        margin: 0 4px;
    }

    .contact-container .contacts .link {
        text-decoration: none;
        color: var(--color-primary);
        font-size: 1.5rem;
    }

    @media (max-width: 1024px) {
        .contact-container {
            transform: none;
            margin: 0 0 16px;
        }

        .contact-container .contacts .link {
            font-size: 1.25rem;
        }
    }

</style>

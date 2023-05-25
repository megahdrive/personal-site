<script lang="ts">
    type LinkSet = {
        name: string,
        description: string,
        url: string,
    };

    export let header = "";
    export let links: LinkSet[] = []; // Format: displayName: linkUrl,
    export let style = "";
</script>

<div style={style}>
    <h2>{header}</h2>
    <ul>
        {#each links as link}
            <li><a title={link.description} href={link.url}>{link.name}</a></li>
        {/each}
    </ul>
</div>
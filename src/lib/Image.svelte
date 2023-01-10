<script>
    export let src = ""
    export let width = ""
    export let alt = ""
    export let caption = ""
</script>

<figure>
    <img src={src} alt={alt} class={width}>
    <figcaption>{caption}</figcaption>
</figure>
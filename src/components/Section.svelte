<script>
    export let id;
    export let cls = "";
</script>

<section style="margin: 60px 0" {id} class={cls}>
    <slot />
</section>

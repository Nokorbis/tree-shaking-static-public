<script>
    import {PUBLIC_FEATURE_FLAG_C, PUBLIC_FEATURE_FLAG_D} from '$env/static/public';
    let noShow = false;

    let featureFlagC = PUBLIC_FEATURE_FLAG_C == 'true';
    let featureFlagD = PUBLIC_FEATURE_FLAG_D == 'true';
</script>
<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>


{#if true}
<p>TRUE This appear, normal ! </p>
{/if}

{#if false}
<p>FALSE This does not appear, great</p>
{/if}

{#if noShow}
<p>NO SHOW This does not appear either, fantastic</p>
{/if}

{#if featureFlagC}
<p>FEATUREFLAGC This feature flag is in the build, cool</p>
{/if}

{#if featureFlagD}
<p>FEATUREFLAGD This feature flag is in the build, not cool</p>
{/if}



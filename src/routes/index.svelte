<script lang="ts" context="module">
  import type { Load } from "@sveltejs/kit"

  export const load: Load = async (event) => {
    await GQL_Characters.fetch({
      event,
    })

    return {}
  }
</script>

<script lang="ts">
  import { GQL_Characters } from "$houdini"
  import { browser } from "$app/env"

  $: browser && GQL_Characters.fetch()
</script>

<pre>
  {JSON.stringify($GQL_Characters.data, null, 2)}
</pre>

<script context="module" lang="ts">
  import client from "../client"

  client.init()
</script>

<script lang="ts">
  import { GQL_Characters } from "$houdini"
</script>

<!-- Comment this line out and it will start working -->
{$GQL_Characters}

<slot />

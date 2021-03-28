<script lang="ts">
  import Lights from "./Lights.svelte";
  import { lifxClient } from "/home/billy/dev/typescript/lifx/lifx";

  const client = new lifxClient({
    token: import.meta.env.VITE_LIFX_API_KEY as string,
  });
</script>

<Lights lights={client.listLights()} />

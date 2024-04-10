<script>
    import * as Drawer from "$lib/components/ui/drawer";
    import { BadgeInfo } from 'lucide-svelte';

    export let text = "text";
    export let opentext = "Informácie";

</script>

<Drawer.Root>
    <Drawer.Trigger>
        <div class="flex items-center gap-2">
        <BadgeInfo class="h-5 w-5" />
        <p>{opentext}</p>
        </div>
    </Drawer.Trigger>
    <Drawer.Content>
        <center>
      <Drawer.Header>
        <center>
        <Drawer.Title>Sieťové vzdelanie</Drawer.Title>
        <Drawer.Description>{text}</Drawer.Description>
    </center>
      </Drawer.Header>
      <Drawer.Footer>
       <p>© {new Date().getFullYear()} <a href="https://michalhicz.eu">Michal Hicz</a></p>
      </Drawer.Footer>
    </center>
    </Drawer.Content>
  </Drawer.Root>
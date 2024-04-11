<script>
    import * as Drawer from "$lib/components/ui/drawer";
    import { BadgeInfo } from 'lucide-svelte';
    import { Button } from "$lib/components/ui/button/index.js";

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
        <Drawer.Title><br>Podmienky služby</Drawer.Title>
        <Drawer.Description>
            <br>
            <p>Všetok náš obsah je voľne šíritelný a dostupný pre každého bez akýchkoľvek poplatkov. Obsah nebude nikdy spoplatnený a slúži len na informačné účely.</p>
            <br>
            <p>Zdrojový kód tejto webovej stránky spolu s celým obsahom je voľne dostupný na githube pod licenciou GNU GENERAL PUBLIC LICENSE Version 3.</p>
            <br>
            <Button href="https://github.com/Sietove-vzdelanie/" variant="outline" size="sm">Github</Button>
        </Drawer.Description>
    </center>
      </Drawer.Header>
      <Drawer.Footer>
       <p>© {new Date().getFullYear()} <a href="https://michalhicz.eu">Michal Hicz</a></p>
      </Drawer.Footer>
    </center>
    </Drawer.Content>
  </Drawer.Root>
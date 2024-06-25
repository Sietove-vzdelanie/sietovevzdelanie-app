<script>
  import ChevronLeft from "lucide-svelte/icons/chevron-left";
  import { Book } from "lucide-svelte";
  import LineChart from "lucide-svelte/icons/line-chart";
  import Package from "lucide-svelte/icons/package";
  import Package2 from "lucide-svelte/icons/package-2";
  import PanelLeft from "lucide-svelte/icons/panel-left";
  import CirclePlus from "lucide-svelte/icons/circle-plus";
  import ShoppingCart from "lucide-svelte/icons/shopping-cart";
  import Upload from "lucide-svelte/icons/upload";
  import UsersRound from "lucide-svelte/icons/users-round";

  import { Badge } from "$lib/components/ui/badge/index.js";
  import * as Breadcrumb from "$lib/components/ui/breadcrumb/index.js";
  import { Button } from "$lib/components/ui/button/index.js";
  import * as Card from "$lib/components/ui/card/index.js";
  import * as DropdownMenu from "$lib/components/ui/dropdown-menu/index.js";
  import { Input } from "$lib/components/ui/input/index.js";
  import { Label } from "$lib/components/ui/label/index.js";
  import * as Select from "$lib/components/ui/select/index.js";
  import * as Sheet from "$lib/components/ui/sheet/index.js";
  import * as Table from "$lib/components/ui/table/index.js";
  import { Textarea } from "$lib/components/ui/textarea/index.js";
  import * as ToggleGroup from "$lib/components/ui/toggle-group/index.js";
  import * as Tooltip from "$lib/components/ui/tooltip/index.js";
  import * as Drawer from "$lib/components/ui/drawer";
  import InfoDrawer from "./InfoDrawer.svelte";

  export let updateDate = "Máj 2024";
</script>

<div class="flex min-h-screen w-full flex-col bg-muted/15">
  <aside
    class="fixed inset-y-0 left-0 z-10 hidden w-60 flex-col border-r bg-background sm:flex"
  >
    <nav class="flex flex-col items-center gap-4 px-2 py-6">
      <a
        href="##"
        class="group transition-all hover:bg-opacity-90 flex h-9 w-9 shrink-0 items-center justify-center gap-2 rounded-full bg-primary text-lg font-semibold text-primary-foreground md:h-8 md:w-24 md:text-base"
      >
        <div class="flex items-center gap-2">
          <Book class="h-4 w-4 transition-all" />
          <p>Kurzy</p>
          <span class="sr-only">Kurzy</span>
        </div>
      </a>
      <Tooltip.Root>
        <Tooltip.Trigger asChild let:builder>
          <a
            href="##"
            class="flex h-9 w-9 items-center justify-center rounded-lg text-muted-foreground transition-colors hover:text-foreground md:h-8 md:w-8"
            use:builder.action
            {...builder}
          >
            <Book class="h-5 w-5" />
            <span class="sr-only">Dashboard</span>
          </a>
        </Tooltip.Trigger>
        <Tooltip.Content side="right">Dashboard</Tooltip.Content>
      </Tooltip.Root>
      <Tooltip.Root>
        <Tooltip.Trigger asChild let:builder>
          <a
            href="##"
            class="flex h-9 w-9 items-center justify-center rounded-lg transition-colors hover:text-foreground md:h-8 md:w-8"
            use:builder.action
            {...builder}
          >
            <ShoppingCart class="h-5 w-5" />
            <span class="sr-only">Orders</span>
          </a>
        </Tooltip.Trigger>
        <Tooltip.Content side="right">Orders</Tooltip.Content>
      </Tooltip.Root>
      <Tooltip.Root>
        <Tooltip.Trigger asChild let:builder>
          <a
            href="##"
            class="flex h-9 w-9 items-center justify-center rounded-lg bg-accent text-accent-foreground transition-colors hover:text-foreground md:h-8 md:w-8"
            use:builder.action
            {...builder}
          >
            <Package class="h-5 w-5" />
            <span class="sr-only">Products</span>
          </a>
        </Tooltip.Trigger>
        <Tooltip.Content side="right">Products</Tooltip.Content>
      </Tooltip.Root>
      <Tooltip.Root>
        <Tooltip.Trigger asChild let:builder>
          <a
            href="##"
            class="flex h-9 w-9 items-center justify-center rounded-lg text-muted-foreground transition-colors hover:text-foreground md:h-8 md:w-8"
            use:builder.action
            {...builder}
          >
            <UsersRound class="h-5 w-5" />
            <span class="sr-only">Customers</span>
          </a>
        </Tooltip.Trigger>
        <Tooltip.Content side="right">Customers</Tooltip.Content>
      </Tooltip.Root>
      <Tooltip.Root>
        <Tooltip.Trigger asChild let:builder>
          <a
            href="##"
            class="flex h-9 w-9 items-center justify-center rounded-lg text-muted-foreground transition-colors hover:text-foreground md:h-8 md:w-8"
            use:builder.action
            {...builder}
          >
            <LineChart class="h-5 w-5" />
            <span class="sr-only">Analytics</span>
          </a>
        </Tooltip.Trigger>
        <Tooltip.Content side="right">Analytics</Tooltip.Content>
      </Tooltip.Root>
    </nav>
    <nav class="mt-auto flex flex-col items-center gap-4 px-2 py-6">
      <InfoDrawer />
      <span class="sr-only">Info</span>
    </nav>
  </aside>
  <div class="flex flex-col sm:gap-14 sm:py-4 sm:pl-60">
    <header
      class="sticky top-0 z-30 flex h-14 items-center gap-4 border-b bg-background px-4 sm:static sm:h-auto sm:border-0 sm:bg-transparent sm:px-6"
    >
      <Sheet.Root>
        <Sheet.Trigger asChild let:builder>
          <Button
            builders={[builder]}
            size="icon"
            variant="outline"
            class="sm:hidden"
          >
            <PanelLeft class="h-5 w-5" />
            <span class="sr-only">Toggle Menu</span>
          </Button>
        </Sheet.Trigger>
        <Sheet.Content side="left" class="sm:max-w-xs">
          <nav class="grid gap-6 text-lg font-medium">
            <a
              href="##"
              class="group flex h-10 w-10 shrink-0 items-center justify-center gap-2 rounded-full bg-primary text-lg font-semibold text-primary-foreground md:text-base"
            >
              <Package2 class="h-5 w-5 transition-all group-hover:scale-110" />
              <span class="sr-only">Acme Inc</span>
            </a>
            <a
              href="##"
              class="flex items-center gap-4 px-2.5 text-muted-foreground hover:text-foreground"
            >
              <Package class="h-5 w-5" />
              Dashboard
            </a>
            <a
              href="##"
              class="flex items-center gap-4 px-2.5 text-muted-foreground hover:text-foreground"
            >
              <ShoppingCart class="h-5 w-5" />
              Orders
            </a>
            <a href="##" class="flex items-center gap-4 px-2.5 text-foreground">
              <Package class="h-5 w-5" />
              Products
            </a>
            <a
              href="##"
              class="flex items-center gap-4 px-2.5 text-muted-foreground hover:text-foreground"
            >
              <UsersRound class="h-5 w-5" />
              Customers
            </a>
            <a
              href="##"
              class="flex items-center gap-4 px-2.5 text-muted-foreground hover:text-foreground"
            >
              <LineChart class="h-5 w-5" />
              Info
            </a>
          </nav>
        </Sheet.Content>
      </Sheet.Root>
      <Breadcrumb.Root class="hidden md:flex">
        <Breadcrumb.List>
          <Breadcrumb.Item>
            <Breadcrumb.Link href="##">Dashboard</Breadcrumb.Link>
          </Breadcrumb.Item>
          <Breadcrumb.Separator />
          <Breadcrumb.Item>
            <Breadcrumb.Link href="##">Products</Breadcrumb.Link>
          </Breadcrumb.Item>
          <Breadcrumb.Separator />
          <Breadcrumb.Item>
            <Breadcrumb.Page>Edit Product</Breadcrumb.Page>
          </Breadcrumb.Item>
        </Breadcrumb.List>
      </Breadcrumb.Root>
    </header>
    <main class="grid flex-1 items-start gap-4 p-4 sm:px-6 sm:py-0 md:gap-8">
      <div class="mx-auto grid max-w-[59rem] flex-1 auto-rows-max gap-6">
        <div class="flex items-center gap-4">
          <Button variant="outline" size="icon" class="h-7 w-7">
            <ChevronLeft class="h-4 w-4" />
            <span class="sr-only">Back</span>
          </Button>
          <h1
            class="flex-1 shrink-0 whitespace-nowrap text-4xl font-semibold tracking-tight sm:grow-0"
          >
            Sieťové technológie
          </h1>
          <div class="hidden items-center gap-2 md:ml-auto md:flex">
            <Badge variant="outline" class="ml-auto sm:ml-0"
              >Upravené: {updateDate}</Badge
            >
          </div>
        </div>
        <div class="grid gap-4 lg:grid-cols-1 lg:gap-8">
          <div
            class="grid auto-rows-max items-start gap-4 lg:col-span-2 lg:gap-8"
          >
            <Card.Root>
              <Card.Header>
                <Card.Title>Product Details</Card.Title>
                <Card.Description>
                  Lipsum dolor sit amet, consectetur adipiscing
                </Card.Description>
              </Card.Header>
              <Card.Content>
                <div class="grid gap-6">
                  <div class="grid gap-3">
                    <Label for="name">Name</Label>
                    <Input
                      id="name"
                      type="text"
                      class="w-full"
                      value="Gamer Gear Pro Controller"
                    />
                  </div>
                  <div class="grid gap-3">
                    <Label for="description">Description</Label>
                    <Textarea
                      id="description"
                      value="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam auctor, nisl nec ultricies ultricies, nunc nisl ultricies nunc, nec ultricies nunc nisl nec nunc."
                      class="min-h-32"
                    />
                  </div>
                </div>
              </Card.Content>
            </Card.Root>
            <Card.Root>
              <Card.Header>
                <Card.Title>Stock</Card.Title>
                <Card.Description>
                  Lipsum dolor sit amet, consectetur adipiscing elit
                </Card.Description>
              </Card.Header>
              <Card.Content>
                <Table.Root>
                  <Table.Header>
                    <Table.Row>
                      <Table.Head class="w-[100px]">SKU</Table.Head>
                      <Table.Head>Stock</Table.Head>
                      <Table.Head>Price</Table.Head>
                      <Table.Head class="w-[100px]">Size</Table.Head>
                    </Table.Row>
                  </Table.Header>
                  <Table.Body>
                    <Table.Row>
                      <Table.Cell class="font-semibold">GGPC-001</Table.Cell>
                      <Table.Cell>
                        <Label for="stock-1" class="sr-only">Stock</Label>
                        <Input id="stock-1" type="number" value="100" />
                      </Table.Cell>
                      <Table.Cell>
                        <Label for="price-1" class="sr-only">Price</Label>
                        <Input id="price-1" type="number" value="99.99" />
                      </Table.Cell>
                      <Table.Cell>
                        <ToggleGroup.Root
                          type="single"
                          value="s"
                          variant="outline"
                        >
                          <ToggleGroup.Item value="s">S</ToggleGroup.Item>
                          <ToggleGroup.Item value="m">M</ToggleGroup.Item>
                          <ToggleGroup.Item value="l">L</ToggleGroup.Item>
                        </ToggleGroup.Root>
                      </Table.Cell>
                    </Table.Row>
                    <Table.Row>
                      <Table.Cell class="font-semibold">GGPC-002</Table.Cell>
                      <Table.Cell>
                        <Label for="stock-2" class="sr-only">Stock</Label>
                        <Input id="stock-2" type="number" value="143" />
                      </Table.Cell>
                      <Table.Cell>
                        <Label for="price-2" class="sr-only">Price</Label>
                        <Input id="price-2" type="number" value="99.99" />
                      </Table.Cell>
                      <Table.Cell>
                        <ToggleGroup.Root
                          type="single"
                          value="m"
                          variant="outline"
                        >
                          <ToggleGroup.Item value="s">S</ToggleGroup.Item>
                          <ToggleGroup.Item value="m">M</ToggleGroup.Item>
                          <ToggleGroup.Item value="l">L</ToggleGroup.Item>
                        </ToggleGroup.Root>
                      </Table.Cell>
                    </Table.Row>
                    <Table.Row>
                      <Table.Cell class="font-semibold">GGPC-003</Table.Cell>
                      <Table.Cell>
                        <Label for="stock-3" class="sr-only">Stock</Label>
                        <Input id="stock-3" type="number" value="32" />
                      </Table.Cell>
                      <Table.Cell>
                        <Label for="price-3" class="sr-only">Stock</Label>
                        <Input id="price-3" type="number" value="99.99" />
                      </Table.Cell>
                      <Table.Cell>
                        <ToggleGroup.Root
                          type="single"
                          value="s"
                          variant="outline"
                        >
                          <ToggleGroup.Item value="s">S</ToggleGroup.Item>
                          <ToggleGroup.Item value="m">M</ToggleGroup.Item>
                          <ToggleGroup.Item value="l">L</ToggleGroup.Item>
                        </ToggleGroup.Root>
                      </Table.Cell>
                    </Table.Row>
                  </Table.Body>
                </Table.Root>
              </Card.Content>
              <Card.Footer class="justify-center border-t p-4">
                <Button size="sm" variant="ghost" class="gap-1">
                  <CirclePlus class="h-3.5 w-3.5" />
                  Add Variant
                </Button>
              </Card.Footer>
            </Card.Root>
            <Card.Root>
              <Card.Header>
                <Card.Title>Product Category</Card.Title>
              </Card.Header>
              <Card.Content>
                <div class="grid gap-6 sm:grid-cols-3">
                  <div class="grid gap-3">
                    <Label for="category">Category</Label>
                    <Select.Root>
                      <Select.Trigger
                        id="category"
                        aria-label="Select category"
                      >
                        <Select.Value placeholder="Select category" />
                      </Select.Trigger>
                      <Select.Content>
                        <Select.Item value="clothing" label="Clothing"
                          >Clothing</Select.Item
                        >
                        <Select.Item value="electronics" label="Electronics">
                          Electronics
                        </Select.Item>
                        <Select.Item value="accessories" label="Accessories">
                          Accessories
                        </Select.Item>
                      </Select.Content>
                    </Select.Root>
                  </div>
                  <div class="grid gap-3">
                    <Label for="subcategory">Subcategory (optional)</Label>
                    <Select.Root>
                      <Select.Trigger
                        id="subcategory"
                        aria-label="Select subcategory"
                      >
                        <Select.Value placeholder="Select subcategory" />
                      </Select.Trigger>
                      <Select.Content>
                        <Select.Item value="t-shirts" label="T-Shirts"
                          >T-Shirts</Select.Item
                        >
                        <Select.Item value="hoodies" label="Hoodies"
                          >Hoodies</Select.Item
                        >
                        <Select.Item value="sweatshirts" label="Sweatshirts">
                          Sweatshirts
                        </Select.Item>
                      </Select.Content>
                    </Select.Root>
                  </div>
                </div>
              </Card.Content>
            </Card.Root>
          </div>
        </div>
        <div class="flex items-center justify-center gap-2 md:hidden">
          <Button variant="outline" size="sm">Discard</Button>
          <Button size="sm">Save Product</Button>
        </div>
      </div>
    </main>
  </div>
</div>

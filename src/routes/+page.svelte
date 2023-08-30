<script lang="ts">
    import * as Dialog from '$lib/components/ui/dialog';
    import * as DropdownMenu from '$lib/components/ui/dropdown-menu';

    let open = false;
</script>

<DropdownMenu.Root>
    <DropdownMenu.Trigger>
        <button
            class="bg-zinc-500 hover:bg-zinc-600 text-white font-bold py-2 px-4 rounded"
        >
            Open dropdown
        </button>
    </DropdownMenu.Trigger>
    <DropdownMenu.Content>
        <DropdownMenu.Group>
            <DropdownMenu.Item
                on:click={() => {
                    open = true;
                }}
                >Show dialog
            </DropdownMenu.Item>
        </DropdownMenu.Group>
    </DropdownMenu.Content>
</DropdownMenu.Root>

<div class="h-[200vh]">
    <Dialog.Root bind:open>
        <Dialog.Content>
            <Dialog.Header>
                <Dialog.Title>Are you sure absolutely sure?</Dialog.Title>
                <Dialog.Description>
                    This action cannot be undone. This will permanently delete
                    your account and remove your data from our servers.
                </Dialog.Description>
            </Dialog.Header>
        </Dialog.Content>
    </Dialog.Root>
</div>

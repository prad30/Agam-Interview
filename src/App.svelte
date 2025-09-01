<script>
  import SideBar from "./components/SideBar.svelte";
  import TopBar from "./components/TopBar.svelte";
  import Modal from "./components/Modal.svelte";

  let modalOpen = false;
</script>

<main>

  <SideBar />
<TopBar />

  <div class="w-full h-screen flex justify-center items-center">
  <button
    class="bg-black text-white px-4 py-2 rounded"
    on:click={() => (modalOpen = true)}
  >
    Click Me
  </button>
</div>

{#if modalOpen}
  <Modal on:close={() => (modalOpen = false)}>
    <p class="text-lg font-bold">Hello World</p>
  </Modal>
{/if}
</main>




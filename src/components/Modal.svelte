<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();

  function closeModal() {
    dispatch("close");
  }
</script>

<div class="fixed inset-0 bg-black/50 bg-opacity-50 flex items-center justify-center">
  <div class="bg-white rounded-lg shadow-lg p-6 w-80 relative">
    <button
      class="absolute top-2 right-2 text-gray-500 hover:text-black"
      on:click={closeModal}
    >
      ✕
    </button>
    <slot></slot>
  </div>
</div>


<script>
  import "../app.css";
  import "$lib/components/terminal.svelte"
  import Terminal from "$lib/components/terminal.svelte";
</script>

<div class="grid h-screen place-items-center mx-5 my-5">
  <div class="flex flex-col w-full lg:flex-row">
    <div class="grid flex-grow card place-items-center w-1/2 p-20 px-10">
      <div class="p-2">
        <h1 class="text-5xl font-bold">Learn terminal the easy way</h1>
        <p class="py-6">
          On lrn.sh you can easily learn how to use Linux terminal with
          interactive exercises and tutorials.
        </p>
      </div>
    </div>
    <!-- <div class="divider lg:divider-horizontal">Try it now</div> -->
    <div class="grid flex-grow card place-items-center w-1/2">
      <div class="tooltip tooltip-open" data-tip="hello">
        <Terminal />
      </div>
    </div>
  </div>
</div>

<style>
  input[type="text"] {
    background: rgba(255, 255, 255, 0.2);
    color: white;
    border: none;
    outline: none;
  }
</style>

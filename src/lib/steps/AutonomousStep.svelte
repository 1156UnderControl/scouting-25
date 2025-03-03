<script lang="ts">
  export let formData;

  import NumberInput from "$lib/components/NumberInput.svelte";
  import Switch from "$lib/components/Switch.svelte";
</script>

<section>
  <div class="flex justify-center items-center w-full mb-4 gap-50">
    <h1 class="text-2xl font-semibold">Auto</h1>
    <h1 class="text-2xl font-semibold">2/4</h1>
  </div>
  <div class="flex flex-col mt-6 mb-6 gap-2">
    <Switch label="Robot has left starting line" bind:value={formData.autoLeft} />
    <Switch label="Removed Algae from Reef" bind:value={formData.removedAlgae} />
    <Switch label="Robot failed" bind:value={formData.robotFailed} />
  </div>

  <section class="flex justify-center">
    <div class="flex flex-col gap-8 mb-5">
      <div>
        <h3>L4 🪸</h3>
        <NumberInput max={7} bind:value={formData.autoL4Corals} />
      </div>
      <div>
        <h3>L3 🪸</h3>
        <NumberInput max={7} bind:value={formData.autoL3Corals} />
      </div>
      <div>
        <h3>L2 🪸</h3>
        <NumberInput max={7} bind:value={formData.autoL2Corals} />
      </div>
      <div>
        <h3>L1 🪸</h3>
        <NumberInput max={7} bind:value={formData.autoL1Corals} />
      </div>
    </div>
    <img src="reef.png" class="w-[20%]" alt="a" />
  </section>

  <section class="flex justify-center">
    <div class="flex gap-4 mt-4">
      <div>
        <h3>Processor 🥅</h3>
        <NumberInput max={7} bind:value={formData.autoProcessor} />
      </div>
      <div>
        <h3>Net 🥅</h3>
        <NumberInput max={7} bind:value={formData.autoNet} />
      </div>
    </div>
  </section>

  
</section>

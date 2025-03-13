<script lang="ts">
  export let formData;

  import NumberInput from "$lib/components/NumberInput.svelte";
  import Switch from "$lib/components/Switch.svelte";
</script>

<section>
  <div class="flex justify-center items-center w-full mb-4 gap-50">
    <h1 class="text-2xl font-semibold">Teleop</h1>
    <h1 class="text-2xl font-semibold">3/4</h1>
  </div>
  <div class="flex flex-col mt-6 mb-6 gap-2">
    <Switch label="Played as defense" bind:value={formData.playedDefense} />
    <Switch label="Removed Algae from Reef" bind:value={formData.removedAlgae} />
    <Switch label="Robot failed" bind:value={formData.robotFailed} />
  </div>
  <section class="flex justify-center">
    <div class="flex flex-col gap-8 mb-5">
      <div>
        <h3>L4 Teleop 🪸</h3>
        <NumberInput max={15} bind:value={formData.teleL4Corals} />
      </div>
      <div>
        <h3>L3 Teleop 🪸</h3>
        <NumberInput max={15} bind:value={formData.teleL3Corals} />
      </div>
      <div>
        <h3>L2 Teleop 🪸</h3>
        <NumberInput max={15} bind:value={formData.teleL2Corals} />
      </div>
      <div>
        <h3>L1 Teleop 🪸</h3>
        <NumberInput max={15} bind:value={formData.teleL1Corals} />
      </div>
    </div>
    <img src="reef.png" class="w-[20%]" alt="a" />
  </section>

  <div class="flex justify-center gap-4 mt-4">
    <div>
      <h3>Processor 🥅</h3>
      <NumberInput max={10} bind:value={formData.teleProcessor} />
    </div>
    <div>
      <h3>Net 🗑️</h3>
      <NumberInput max={10} bind:value={formData.teleNet} />
    </div>
  </div>
</section>

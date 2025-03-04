<script lang="ts">
    let { selectedStartZone = $bindable() } = $props();
  
    function onChange(event: Event) {
        selectedStartZone = (event.currentTarget as HTMLInputElement).value;
    }
</script>

<div class="flex justify-between mt-4 w-80 h-40 
    bg-[url('/field.png')] bg-contain bg-no-repeat">
    
    <label class="flex items-center w-full h-full">
        <input
          bind:group={selectedStartZone}
          type="radio"
          name="barge"
          value="barge"
          class="appearance-none peer hidden"
        />
        <span
          class="w-full h-full cursor-pointer px-4 flex items-center justify-center text-sm transition hover:border-2 hover:border-black peer-checked:border-black peer-checked:border-2"
        >
          Barge
        </span>
      </label>

      <label class="flex items-center w-full">
        <input
          bind:group={selectedStartZone}
          type="radio"
          name="reef"
          value="reef"
          class="appearance-none peer hidden"
        />
        <span
          class="w-full h-full cursor-pointer px-4 flex items-center justify-center text-sm transition hover:border-2 hover:border-black peer-checked:border-black peer-checked:border-2"
        >
          Reef
        </span>
      </label>

      <label class="flex items-center w-full h-full mr-4">
        <input
          bind:group={selectedStartZone}
          type="radio"
          name="processor"
          value="processor"
          class="appearance-none peer hidden"
        />
        <span
          class="w-full h-full cursor-pointer px-4 flex items-center justify-center text-sm transition hover:border-2 hover:border-black peer-checked:border-black peer-checked:border-2"
        >
          Processor
        </span>
      </label>
</div>



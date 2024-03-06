<script>
import Button from '$lib/button/Button.svelte';
import Icon from '$lib/icon/Icon.svelte';

  let events = [
    {
      name: "IWD'24 SheInnovates Hackathon", 
      venue: "Altimetrik, Chennai",
      time: "09:30 AM",
      url: "https://forms.gle/T5DFZtYDLGs7RoG68"
    },
    {
      name: "IWD'24 SheInnovates",
      venue: "Animaker, Chennai",
      time: "09:30 AM",
      url: "https://forms.gle/PwnAzyAapBLLCbg9A"
    },
  ];
</script>

<section id="Register">
    <div id="regis" class="flex w-full flex-col items-center space-y-6">
        <div class="pt-12 sm:pt-16 lg:pt-20">
          <div class="mx-auto max-w-7xl">
            <div class="text-center">
              <h2
                class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl lg:text-5xl"
              >
                Register Now
              </h2>
            </div>
            
          </div>
        </div>
    </div>
    <div class="grid grid-cols-1 mt-32 md:grid-cols-2 gap-10 px-10">
      {#each events as event}
        <div class="bg-white/60 p-4 shadow-xl shadow-blue-900/5">
          <h2 class="text-xl font-bold mb-2">{event.name}</h2>
          <p class="text-gray-600 mb-2">Venue: {event.venue}</p>
          <p class="text-gray-600 mb-2">Time: {event.time}</p>
          <Button
          id="button-hero-get-tickets"
          title="Register Now"
          onClick={() => window.open(event.url)}
        >
          <Icon width="20" height="20" name="ticket" />
        </Button>
        </div>
      {/each}
    </div>
    
</section>
<style>
  .grid {
    grid-template-columns: repeat(auto-fit, minmax(10px, 1fr));
  }
</style>

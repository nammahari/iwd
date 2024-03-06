<script lang="ts">
  const perks = [
    {
      name: 'Hackathon Extravaganza',
      imageSrc: '/icons/techtalk.webp',
      description:
        'Immerse yourself in a dynamic hackathon where creativity meets code. '
    },
    {
      name: 'Masterclass Sessions',
      imageSrc: '/icons/experts.webp',
      description:
        'Elevate your expertise with exclusive masterclass sessions led by industry trailblazers. '
    },
    {
      name: 'Networking',
      imageSrc: '/icons/networking.webp',
      description:
        'Forge meaningful relationships, share experiences, and tap into a supportive community that fosters mentorship and collaboration.'
    },
    {
      name: 'Accelerate Your Learning ',
      imageSrc: '/icons/workshops.webp',
      description:
        'From inspiring keynotes to hands-on workshops, the event offers a diverse range of learning opportunities.'
    },
    
    {
      name: 'Tech Talks',
      imageSrc: '/icons/techtalk.webp',
      description:
        'Several speakers are coming together to talk about their experiences in the industry. We will also have a few lightning talks with our members.'
    },{
      name: "Celebrate Women's Impact",
      imageSrc: '/icons/networking.webp',
      description:
        'Join us in celebrating the incredible contributions of women in tech.'
    }
  ];
</script>

<section id="why" class="flex w-full flex-col items-center space-y-6 px-6 md:px-24 lg:md:24">
  <div class="pt-12 sm:pt-16 lg:pt-20">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="text-center">
        <h2
          class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl lg:text-5xl"
        >
          Why attend?
        </h2>
        <p class="mt-4  text-gray-600 sm:text-xl">
          We have a fantastic lineup of speakers and sessions for you to learn
          and enhance your skills.
        </p>
      </div>
    </div>
  </div>
  <h2 class="sr-only">Our perks</h2>
  <div class="mx-auto max-w-7xl py-24 sm:px-2 sm:py-32 lg:px-4">
    <div
      class="mx-auto grid max-w-2xl grid-cols-1 gap-y-12 gap-x-8 px-4 lg:max-w-none lg:grid-cols-2 lg:gap-y-16"
    >
      {#each perks as perk}
        <div class="items-center sm:flex">
          <div class="sm:flex-shrink-0">
            <div class="flex w-full items-center justify-center">
              <img
                class="h-24 w-28"
                width={120}
                height={100}
                src={perk.imageSrc}
                alt=""
              />
            </div>
          </div>
          <div class="mt-3 sm:mt-0 sm:ml-3 ">
            <!-- Update the h3 code from 
                1. text-base to text-2xl for Mobile 
                2. text-3xl for Laptop View for better UI
             -->
            <h3
              class="text-center text-2xl font-medium text-gray-900 sm:text-start  xl:text-3xl"
            >
              {perk.name}
            </h3>
            <!-- Update the h3 code from 
                1. text-base for Laptop View for better UI
                
             -->
            <p
              class="mt-2 text-center text-sm text-gray-500 sm:text-start lg:text-base"
            >
              {perk.description}
            </p>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>

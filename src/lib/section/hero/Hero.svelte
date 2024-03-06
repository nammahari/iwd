<script lang="ts">
  import Button from '$lib/button/Button.svelte';
  import Icon from '$lib/icon/Icon.svelte';
  import Countdown from '$lib/section/countdown/Countdown.svelte';
  import Register from '$lib/register/register.svelte';
  import Modal from '$lib/modal/Modal.svelte';
  import { openModal } from 'svelte-modals';

  function handleClick() {
    const registerSection = document.getElementById('Register');
    if (registerSection) {
      registerSection.scrollIntoView({ behavior: 'smooth' });
    }
  }
</script>

<section
  id="hero"
  class="overflow-hidden flex w-full flex-col items-center justify-start space-y-8 px-10 transition-all  duration-500 ease-in-out"
>
  <div
    id="hero-content-group"
    class="flex flex-col items-center justify-start space-y-8 overflow-hidden"
  >
    <div class="bg-text-container max-w-7xl overflow-hidden">
      <div class="animate-text">
        <span>IWD'24 </span>
        <span>IWD'24 </span>
        <span>IWD'24 </span>
        
      </div>
      <div class="animate-text left">
        <span>Impact the Future</span>
        <span>Impact The Future</span>
      </div>
    </div>

    <h1
      class="text-start text-4xl font-bold tracking-tight text-black md:text-center md:text-6xl lg:text-center lg:text-7xl"
    >
      Chennai’s most awaited woman tech conference
    </h1>
    <p class="max-w-2xl text-start text-gray-700 md:text-center lg:text-center">
      Join us for a groundbreaking Women's Day in Tech event, 'SheInnovates', that aims to celebrate women in technology, encourage more women to step forward, break down barriers, and foster innovation.
    </p>
  </div>

  <div
    id="hero-cta-group"
    class="flex w-full max-w-2xl flex-col items-center justify-start space-y-4 md:flex-row md:space-x-4 md:space-y-0 lg:flex-row"
  >
    <Button
      id="button-hero-get-tickets"
      title="Book tickets"
      onClick={() => handleClick()}
    >
      <Icon width="20" height="20" name="ticket" />
    </Button>

    <Button
      id="button-hero-add-to-calendar"
      isSecondaryButton={true}
      title="Add to calendar"
      onClick={() =>
        window.open(
          'https://calendar.google.com/calendar/event?action=TEMPLATE&tmeid=M2FlamwzbG10djhiNWQ3b2lpOXFhbGs3a2UgdGVjaC53dG1jaGVubmFpQG0&tmsrc=tech.wtmchennai%40gmail.com'
        )}
    >
      <i class="fa fa-calendar" />
    </Button>
  </div>

  <div
  class="flex w-full flex-col items-center justify-center space-y-3 text-xl sm:flex-row sm:space-y-0 sm:space-x-6"
>
  <div class="flex items-center space-x-2">
    <i class="fa fa-calendar" />
    <p>March 9th</p>
    <i class="fa fa-location-arrow" />
    <a href="https://maps.app.goo.gl/NkdqaffRsyyaHJLWA"
      ><p>Altimetrik, Chennai</p></a>
  </div>
  <div><p>&</p></div>
  <div class="flex items-center space-x-2">
    <i class="fa fa-calendar" />
    <p>March 10th</p>
    <i class="fa fa-location-arrow" />
    <a href="https://maps.app.goo.gl/QwnJgnukEtgESLpK8"
      ><p>Animaker, Chennai</p></a>
  </div>
</div>

  <div class="items-center">
    <Countdown />
  </div>
</section>

<style>

  .bg-text-container {
    transform: translateX(-50%);
    left: 50%;
    position: absolute;
    z-index: -999;
  }

  span {
    font-size: 280px;
    color: transparent;
    -webkit-text-stroke: 2px #30442a;
    text-transform: uppercase;
    display: inline-block;
    line-height: 0.75;
    min-width: auto;
    font-weight: 200;
    opacity: 0.1;
  }

  @keyframes text-scrolling {
    0% {
      transform: translate3d(-100%, 0, 0);
    }
    100% {
      transform: translate3d(0%, 0, 0);
    }
  }
  .animate-text {
    animation: text-scrolling 20s linear infinite;
    will-change: transform;
    display: block;
    position: relative;
    white-space: nowrap;
  }
  .animate-text.left {
    animation-direction: reverse;
  }
</style>

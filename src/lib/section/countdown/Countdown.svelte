<script>
  import { onMount, tick } from 'svelte';

  onMount(() => {
    tick().then(() => {
      var deadline = 'March 09 2024 08:59:59';
      initializeClock('clockdiv', deadline);
    });

    /**
     * @param {string} endtime
     */
    function getTimeRemaining(endtime) {
      // @ts-ignore
      var t = Date.parse(endtime) - Date.parse(new Date());
      var seconds = Math.floor((t / 1000) % 60);
      var minutes = Math.floor((t / 1000 / 60) % 60);
      var hours = Math.floor((t / (1000 * 60 * 60)) % 24);
      var days = Math.floor(t / (1000 * 60 * 60 * 24));
      return {
        'total': t,
        'days': days,
        'hours': hours,
        'minutes': minutes,
        'seconds': seconds
      };
    }

    /**
     * @param {string} id
     * @param {string} endtime
     */
    function initializeClock(id, endtime) {
      var clock = document.getElementById(id);
      var daysSpan = clock ? clock.querySelector('.days') : null;
      var hoursSpan = clock ? clock.querySelector('.hours') : null;
      var minutesSpan = clock ? clock.querySelector('.minutes') : null;
      var secondsSpan = clock ? clock.querySelector('.seconds') : null;

      function updateClock() {
        var t = getTimeRemaining(endtime);

        if (daysSpan) {
          daysSpan.innerHTML = ('0' + t.days).slice(-2);
        }
        if (hoursSpan) {
          hoursSpan.innerHTML = ('0' + t.hours).slice(-2);
        }
        if (minutesSpan) {
          minutesSpan.innerHTML = ('0' + t.minutes).slice(-2);
        }
        if (secondsSpan) {
          secondsSpan.innerHTML = ('0' + t.seconds).slice(-2);
        }

        if (t.total <= 0) {
          clearInterval(timeinterval);
        }
      }

      updateClock(); 
      var timeinterval = setInterval(updateClock, 1000);
    }
  });
</script>

<div id="clockdiv" class="flex space-x-6 text-center">
  <div class="bg-gray-900 p-3 rounded-lg text-white shadow-sm">
    <span class="days text-3xl"></span>
    <div>Days</div>
  </div>
  <div class="bg-gray-900 p-3 rounded-lg text-white shadow-sm">
    <span class="hours text-3xl"></span>
    <div>Hours</div>
  </div>
  <div class="bg-gray-900 p-3 rounded-lg text-white shadow-sm">
    <span class="minutes text-3xl"></span>
    <div>Minutes</div>
  </div>
  <div class="bg-gray-900 p-3 rounded-lg text-white shadow-sm">
    <span class="seconds text-3xl"></span>
    <div>Seconds</div>
  </div>
</div>

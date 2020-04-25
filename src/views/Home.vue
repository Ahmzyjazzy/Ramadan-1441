<template>
  <div class="home">
    <RamadanDay :day="currentData.day" :quote="currentData.quote" :author="currentData.author" />
  </div>
</template>

<script>
// @ is an alias to /src
import RamadanDay from '@/components/RamadanDay.vue';
import Ramadan from '@/data/ramadan.json';

export default {
  name: 'Home',
  components: {
    RamadanDay
  },
  data(){
    return {
      firstDay: new Date('2020/04/24'),
      data: Ramadan
    }
  },
  computed: {
    currentData(){      
      return Ramadan[1];
    }
  },
}
</script>


<style lang="scss">
.home {
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  background: radial-gradient(100% 225% at 100% 0%, #FAFF00 0%, #000000 100%), linear-gradient(235deg, #DB00FF 0%, #000000 100%), linear-gradient(45deg, #241E92 0%, #241E92 40%, #5432D3 40%, #5432D3 50%, #7B6CF6 50%, #7B6CF6 70%, #E5A5FF 70%, #E5A5FF 100%), linear-gradient(180deg, #01024E 0%, #01024E 43%, #543864 43%, #543864 62%, #8B4367 62%, #8B4367 80%, #FF6464 80%, #FF6464 100%);
  background-blend-mode: overlay, hard-light, overlay, normal;    
  animation: gradienta 50s ease-in 0s infinite alternate;
}

@keyframes gradienta {
  10% {
    background: radial-gradient(100% 225% at 100% 0%, #FAFF00 0%, #000000 100%), linear-gradient(235deg, #DB00FF 0%, #000000 100%), linear-gradient(45deg, #241E92 0%, #241E92 40%, #5432D3 40%, #5432D3 50%, #7B6CF6 50%, #7B6CF6 70%, #E5A5FF 70%, #E5A5FF 100%), linear-gradient(180deg, #01024E 0%, #01024E 43%, #543864 43%, #543864 62%, #8B4367 62%, #8B4367 80%, #FF6464 80%, #FF6464 100%);
    background-blend-mode: overlay, hard-light, overlay, normal;  
  }
  20% {
    background: linear-gradient(114.95deg, rgba(235, 0, 255, 0.5) 0%, rgba(0, 0, 0, 0) 38.87%), linear-gradient(180deg, #004B5B 0%, #FFA7A7 100%), linear-gradient(244.35deg, #FFB26A 0%, #3676B1 50.58%, #00A3FF 100%), linear-gradient(244.35deg, #FFFFFF 0%, #007089 49.48%, #FF005C 100%), radial-gradient(100% 233.99% at 0% 100%, #6D3B00 0%, #8FFF00 100%), linear-gradient(307.27deg, #219D87 0.37%, #93C32E 50.19%, #2800C6 100%), radial-gradient(100% 140% at 100% 0%, #FF00C7 0%, #006C7A 49.48%, #760000 100%);
    background-blend-mode: hard-light, overlay, overlay, overlay, difference, difference, normal;
  }
  30% {
    background: linear-gradient(253.56deg, #FFAAE2 3.05%, #2C008A 94.6%), radial-gradient(100% 246.94% at 100% 100%, #FFFFFF 0%, #000353 100%), linear-gradient(121.18deg, #1400FF 0.45%, #3A0000 100%), linear-gradient(341.1deg, #F3D0FC 7.52%, #1700A4 77.98%), linear-gradient(222.34deg, #CF0C00 12.99%, #00574D 87.21%), linear-gradient(150.76deg, #B7D500 15.35%, #2200AA 89.57%);
    background-blend-mode: overlay, overlay, difference, difference, difference, normal;
  }
  40% {
    background: linear-gradient(121.28deg, #31BC00 0%, #000000 100%), linear-gradient(180deg, #5200FF 0%, #1A0050 100%), linear-gradient(341.1deg, #FF0000 7.52%, #1700A4 77.98%), radial-gradient(49.82% 80.51% at 49.82% 50%, #5A0069 0%, #FF3D00 100%), radial-gradient(50% 72.12% at 50% 50%, #EB00FF 0%, #110055 100%);
    background-blend-mode: color-dodge, overlay, difference, difference, normal;
  }
  50% {
    background: linear-gradient(121.28deg, #000000 0%, #FFFFFF 100%), linear-gradient(121.28deg, #FFB800 0%, #FFFFFF 100%), linear-gradient(140.54deg, #7000FF 0%, #001AFF 72.37%), linear-gradient(307.43deg, #FFE927 0%, #00114D 100%), radial-gradient(107% 142.8% at 15.71% 104.5%, #FFFFFF 0%, #A7AA00 100%), radial-gradient(100.22% 100% at 70.57% 0%, #7A3B00 0%, #1DAC92 100%);
    background-blend-mode: difference, soft-light, difference, difference, difference, exclusion;
  }
  60% {
    background: linear-gradient(114.95deg, rgba(235, 0, 255, 0.5) 0%, rgba(0, 71, 255, 0) 34.35%), linear-gradient(180deg, #004B5B 0%, #FFA7A7 100%), linear-gradient(244.35deg, #FFB26A 0%, #3676B1 50.58%, #00A3FF 100%), linear-gradient(244.35deg, #FFFFFF 0%, #004A74 49.48%, #FF0000 100%), radial-gradient(100% 233.99% at 0% 100%, #B70000 0%, #AD00FF 100%), linear-gradient(307.27deg, #219D87 0.37%, #2650BA 50.19%, #2800C6 100%), radial-gradient(100% 140% at 100% 0%, #FF00C7 0%, #006C7A 49.48%, #760000 100%);
    background-blend-mode: hard-light, overlay, overlay, overlay, difference, difference, normal;
  }
  70% {
    background: linear-gradient(238.72deg, #0044A9 0%, #F700A3 100%), radial-gradient(100% 188.01% at 76.14% 0%, #43DDFF 0%, #FF0000 100%), linear-gradient(0deg, #DB00FF 0%, #14FF00 100%), radial-gradient(59.2% 100% at 50% 0%, #8000FF 0%, #0085FF 100%), radial-gradient(100% 148.07% at 0% 0%, #FC8800 0%, #00FF94 100%);
    background-blend-mode: hard-light, overlay, color-burn, color-burn, normal;
  }
  80% {
    background: linear-gradient(286.78deg, #36006B 4.99%, #000000 96.56%), linear-gradient(238.72deg, #A30000 0%, #FFFFFF 100%), radial-gradient(100% 188.01% at 76.14% 0%, #43DDFF 0%, #FF0000 100%), linear-gradient(0deg, #DB00FF 0%, #14FF00 100%), radial-gradient(59.2% 100% at 50% 100%, #6A00D5 0%, #00E0FF 100%), radial-gradient(100% 148.07% at 0% 0%, #FF9900 0%, #001AFF 100%);
    background-blend-mode: lighten, overlay, overlay, color-burn, color-burn, normal;
  }
  90% {
    background: linear-gradient(45deg, #000850 0%, #000320 100%), radial-gradient(100% 225% at 100% 0%, #FF6928 0%, #000000 100%), linear-gradient(225deg, #FF7A00 0%, #000000 100%), linear-gradient(135deg, #CDFFEB 10%, #CDFFEB 35%, #009F9D 35%, #009F9D 60%, #07456F 60%, #07456F 67%, #0F0A3C 67%, #0F0A3C 100%);
    background-blend-mode: screen, overlay, hard-light, normal;
  }
  100% {
    background: linear-gradient(0deg, #004DA8 0%, #000000 100%), linear-gradient(238.72deg, #011662 0%, #FFFFFF 100%), linear-gradient(301.28deg, #FF876C 0%, #005B83 51.04%, #030098 100%), radial-gradient(100% 200% at 0% 0%, #FFFFFF 0%, #2400B4 100%), linear-gradient(133.98deg, #FF0000 30.43%, #00A3FF 100%), radial-gradient(70.41% 100% at 50% 0%, #DBDF00 0%, #2200AA 100%);
    background-blend-mode: overlay, soft-light, color-dodge, darken, difference, normal;
  }
}



</style>
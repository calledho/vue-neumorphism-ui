<template>
  <div class="circle_1">
    <div class="circle_2">
      <svg>
        <defs>
          <linearGradient id="linear" x1="0%" y1="0%" x2="100%" y2="0%">
            <stop offset="0%" stop-color="#05a" stop-opacity="0.5" />
            <stop offset="100%" stop-color="#0a5" stop-opacity="1.0" />
          </linearGradient>
        </defs>
        <circle
          cx="60"
          cy="60"
          r="62"
          stroke="url(#linear)"
          :stroke-dashoffset="dashoffset"
        >
          <animate
            attributeName="stroke-dashoffset"
            from="400"
            :to="dashoffset"
            dur="1.2s"
            repeatCount="1"
          />
        </circle>
      </svg>
    </div>
    <span class="text">{{ dashoffset }}<span>%</span></span>
  </div>
</template>

<script>
export default {
  name: "NeuCircleProgress",
  props: {
    percent: {
      type: String,
      default: ""
    },
    dashoffset: {
      type: String,
      default: "0"
    }
  }
};
</script>

<style scoped>
.circle_1 {
  position: relative;

  width: 160px;

  height: 160px;

  border: 5px solid #e5e7eb;

  border-radius: 50%;

  box-shadow: inset 2px 2px 6px #babecc, inset -4px -5px 8px #fff;

  box-sizing: border-box;

  color: #babecc;
}

.circle_2 {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);

  width: 100px;

  height: 100px;

  border: 5px solid #e5e7eb;

  border-radius: 50%;

  box-shadow: inset 2px 2px 6px #babecc, inset -4px -5px 8px #fff;

  box-sizing: border-box;

  color: #babecc;
}

.circle_1 svg {
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  position: absolute;
  width: 160px;
  height: 160px;
}
.circle_1 svg circle {
  fill: none;
  stroke-width: 24;
  /* left: 50%;
        top:50%; */
  transform: translate(13%, 13%);
  stroke-dasharray: 389, 389;
  /* stroke-dashoffset: 0; */
  /* stroke-dashoffset: calc(389 - (389*87) / 100); */
  stroke-linecap: round;
}
.circle_1 svg circle:nth-child(1) {
  stroke: #0fbcf9;
  stroke-dashoffset: 0;
}
.text {
  font-size: 30px;
  text-align: center;
  font-weight: bold;
  color: black;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  position: absolute;
}
.text span {
  font-size: 15px;
  color: darkgray;
}
</style>

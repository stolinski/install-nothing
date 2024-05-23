<script lang="ts">
  import chrome from "../assets/chrome.svg";
  import ff from "../assets/ff.svg";
  import saf from "../assets/saf.svg";

  export let c_v = "";
  export let ff_v = "";
  export let saf_v = "";

  function version_or_x(v) {
    if (v) return v;
    return "✖";
  }
</script>

<div class="wrapper">
  <div class="contain" class:v={c_v}>
    <span>{version_or_x(c_v)}</span>
    <img src={chrome} alt="Chrome" />
  </div>
  <div class="contain" class:v={ff_v}>
    <span>{version_or_x(ff_v)}</span>
    <img src={ff} alt="Firefox" />
  </div>
  <div class="contain" class:v={saf_v}>
    <span>{version_or_x(saf_v)}</span>
    <img src={saf} alt="Safari" />
  </div>
</div>

<style>
  .wrapper {
    display: flex;
    gap: 40px;
    align-items: center;
    justify-content: center;
    margin-bottom: -50px;
    inset: auto 0;
    position: relative;
    background: linear-gradient(to bottom, #000000 50%, #00000000);
  }

  img {
    width: 80px;
  }

  .contain {
    position: relative;
    opacity: 0.3;
  }

  .v {
    opacity: 1;
  }

  .contain span {
    position: absolute;
    bottom: 20px;
    left: 50%;
    translate: -50% 0;
    padding: 0 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 2rem;
    font-weight: 900;
    color: #000;
    background: var(--red);
    line-height: 1;
  }

  .v span {
    background: linear-gradient(to left, var(--green), var(--teal));
    box-shadow: 0 0 10px 10px oklch(0% 0 100 / 0.3);
  }
</style>

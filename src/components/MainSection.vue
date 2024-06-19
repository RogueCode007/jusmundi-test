<script setup>
import Icon from "./Icon.vue";
</script>
<template>
  <section>
    <div id="left-box">
      <div class="maincircle">
        <Icon src="icc" id="icc-logo" />
        <div id="jusmundi-logo-circle">
          <Icon src="jusmundi" />
        </div>
      </div>
      <img src="../assets/images/case_bg.gif" alt="case-gif" id="gif" />
    </div>
    <div id="right-box">
      <h1>
        A Unique Partnership for the Publication of ICC Arbitration Awards
      </h1>
      <p>
        The International Chamber of Commerce (ICC) & Jus Mundi have joined
        forces to make ICC Arbitration Awards and related materials freely
        available to the global legal community.
      </p>
      <button id="blue-btn" class="center">
        <Icon src="caret-right" />
        <span>Access ICC Awards</span>
      </button>
    </div>
    <button id="white-btn">
      <Icon :src="'arrow-up'" />
      <span>TRY JUS MUNDI</span>
    </button>
    <span class="green-dash top"></span>
    <span class="green-dash bottom"></span>
    <span class="green-dash right"></span>
  </section>
</template>

<style scoped lang="scss">
@mixin pseudo-element($top, $right, $bottom, $left) {
  background-color: #6ad300;
  width: 24px;
  height: 2px;
  position: absolute;
  display: inline;
  top: $top;
  right: $right;
  bottom: $bottom;
  left: $left;
}
section {
  background-color: #fff;
  padding: 80px 10px;

  position: relative;
  button#white-btn {
    font-family: "Lato";
    font-size: 14px;
    font-weight: 700;
    position: absolute;
    top: 10px;
    right: 10px;
    padding: 16px;
    box-shadow: 0px 8px 32px 0px #254f6d3d;
    display: flex;
    align-items: end;
    justify-content: center;
    letter-spacing: 2px;
    gap: 5px;
  }
}
div#left-box {
  display: none;
}

div#right-box {
  h1 {
    font-family: "Larken";
    font-weight: 700;
    font-size: 3rem;
    letter-spacing: -1px;
    opacity: 0;
    animation: 1s ease-in-out forwards appear, 1s ease-in-out slideUp;
  }
  p {
    margin-top: 10px;
    font-size: 1.125rem;
    line-height: 32px;
    opacity: 0;
    animation: 1s ease-in-out forwards appear;
  }
  button#blue-btn {
    margin-top: 60px;
    background-color: #009efe;
    color: #fff;
    border-radius: 4px;
    gap: 5px;
    padding: 18px 25px;
    letter-spacing: 2px;
    opacity: 0;
    animation: 1s ease-in-out 1s forwards appear, 1s ease-in-out 1s slideUp;
  }
}
@media (min-width: 768px) {
  section {
    padding: 100px 40px;

    div#right-box {
      p {
        margin-top: 20px;
      }
    }
  }
}

@media (min-width: 1280px) {
  section {
    position: relative;
    padding: 80px 30px;
    min-height: 100vh;
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    button#white-btn {
      right: 30px;
      top: 30px;
    }

    span.green-dash.top {
      @include pseudo-element(30px, auto, auto, 100px);
    }
    span.green-dash.bottom {
      @include pseudo-element(auto, auto, 30px, 100px);
      transform: rotateZ(90deg);
    }
    span.green-dash.right {
      @include pseudo-element(auto, 100px, 30px, auto);
      transform: rotateZ(45deg);
    }
  }
  div#left-box {
    display: flex;
    justify-content: center;
    position: relative;
    div.maincircle {
      box-shadow: 0px 0px 128px 0px #0000001a;
      border-radius: 100%;
      width: 480px;
      height: 480px;
      background-color: #fff;
      display: flex;
      align-items: center;
      justify-content: center;
      animation: 1s ease-in-out scaleUp;
      position: relative;
      top: -30px;
      z-index: 10;

      img#icc-logo {
        opacity: 0;
        animation: 1s ease-in-out 1s forwards appear;
      }
      div#jusmundi-logo-circle {
        background-color: rgba(255, 255, 255, 0.681);
        width: 187px;
        height: 187px;
        border-radius: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        position: absolute;
        bottom: -150px;
        left: 50px;
        opacity: 0;
        animation: 1s ease-in-out 2s forwards appear,
          1s ease-in-out 2s forwards slideRight;
      }
    }
    img#gif {
      position: absolute;
      display: block;
      width: 400px;
      height: 300px;
      bottom: 0px;
      right: 100px;
      opacity: 0;
      animation: 1s ease-in-out 2s forwards appear;
    }
  }
  div#right-box {
    padding-top: 40px;
    padding-right: 20%;
    h1 {
      font-weight: 800;
      font-size: 4rem;
      opacity: 0;
      animation: 1s ease-in-out 1s forwards appear, 1s ease-in-out 1s slideUp;
    }
    p {
      margin-top: 20px;
      opacity: 0;
      animation: 1s ease-in-out 1s forwards appear;
    }
    button#blue-btn {
      margin-top: 50px;
      opacity: 0;
      animation: 1s ease-in-out 3s forwards appear, 1s ease-in-out 3s slideUp;
    }
  }
}

@keyframes scaleUp {
  0% {
    transform: scale(0.5);
  }

  100% {
    transform: scale(1);
  }
}
@keyframes appear {
  0% {
    opacity: 0;
  }

  100% {
    opacity: 1;
  }
}
@keyframes slideUp {
  0% {
    transform: translateY(40px);
  }

  100% {
    transform: translateY(0);
  }
}
@keyframes slideRight {
  0% {
    transform: translateX(-40px);
  }

  100% {
    transform: translateX(0);
  }
}
</style>

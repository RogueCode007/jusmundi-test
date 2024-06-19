<script setup>
import Metric from "./Metric.vue";

const metrics = [
  {
    iconSrc: "more-content",
    header: "More key arbitration content",
    content:
      "This unique partnership means you will have access to more key arbitration content to level up your arbitration research. ",
  },
  {
    iconSrc: "transparency",
    header: "More transparency",
    content: "You will appreciate the increase in transparency in arbitration!",
  },
  {
    iconSrc: "efficiency",
    header: "More efficiency",
    content:
      "Jus Mundi’s AI-powered technology efficiently delivers thorough legal research and due diligence with full confidence. ",
  },
];
</script>
<template>
  <section>
    <div class="cont">
      <h1>Why this partnership ?</h1>
      <p class="text">
        Throughout its 100-year history, ICC has brought global business
        together to support an international rules-based order, including the
        promotion of global trade and commerce through the work of the ICC
        International Court of Arbitration.
      </p>
      <br />
      <br />
      <p class="text">
        ICC has partnered with Jus Mundi to provide full public access to all
        publishable ICC International Court of Arbitration awards and related
        documents made as of 1 January 2019
      </p>
    </div>
    <div class="metrics">
      <Metric
        v-for="(metric, index) in metrics"
        :key="index"
        :icon-src="metric.iconSrc"
        :header="metric.header"
        :content="metric.content"
      />
    </div>
  </section>
</template>

<style lang="scss" scoped>
@mixin pseudo-element($top, $right, $bottom, $left) {
  content: "";
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
  padding: 20px 10px;
  text-align: center;
  h1 {
    font-family: "Larken";
    font-weight: bold;
    letter-spacing: -1px;
    font-size: 3rem;
    margin-bottom: 40px;
  }
  p.text {
    font-size: 18px;
  }
  div.metrics {
    padding: 40px 0;
    display: flex;
    flex-direction: column;
    gap: 5px;
  }
  span.green-dash {
    display: none;
  }
}
@media (min-width: 768px) {
  section {
    padding: 20px 40px;

    div.metrics {
      padding: 40px 60px;
    }
  }
}
@media (min-width: 1024px) {
  section {
    div.cont {
      padding: 0 20%;
      position: relative;

      h1 {
        position: relative;

        &::before {
          @include pseudo-element(50%, auto, auto, -30%);
          transform: translateY(-50%);
        }
        &::after {
          @include pseudo-element(50%, -30%, auto, auto);
          transform: translateY(-50%);
        }
      }
    }

    div.metrics {
      padding: 40px 0;
      width: 80%;
      margin: 0 auto;
      display: grid;
      gap: 20px;
      grid-template-columns: repeat(3, minmax(0, 1fr));
    }
  }
}
</style>

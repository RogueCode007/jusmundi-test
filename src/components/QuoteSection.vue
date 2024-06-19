<script setup>
import Icon from "./Icon.vue";
</script>
<template>
  <section>
    <div id="quote">
      <Icon src="quote-start" id="quote-start" />
      <Icon src="quote-end" id="quote-end" />
      <p>
        Publicising and disseminating information about arbitration has been one
        of ICC’s commitments since its creation and an instrumental factor in
        facilitating the development of trade worldwide.
      </p>
    </div>
    <p id="note">
      Note to the Parties and the Arbitral Tribunalson the Conduct of
      Arbitration under the ICC Rules of Arbitration
    </p>
    <a>READ THE WHOLE DOCUMENT</a>
  </section>
</template>

<style lang="scss" scoped>
section {
  background-color: #ffffff;
  padding: 30px 20px;

  div#quote {
    position: relative;
    max-width: 904px;
    margin: 0 auto;
    padding: 10px;
    p {
      font-family: "LarkenItalic";
      font-size: 16px;
      line-height: 32px;
    }
    img#quote-start {
      position: absolute;
      top: -10px;
      left: -10px;
    }
    img#quote-end {
      position: absolute;
      bottom: -10px;
      right: -10px;
    }
  }
  p#note {
    text-align: center;
    width: 80%;
    margin: 40px auto 20px auto;
    font-size: 14px;
    line-height: 24px;
  }
  a {
    display: block;
    text-align: center;
    text-decoration: underline;
    font-family: "Lato";
    letter-spacing: 2px;
    font-size: 12px;
    line-height: 16px;
    color: #2c2b2e;
    cursor: pointer;
  }
}
@media (min-width: 768px) {
  section {
    padding: 60px 80px;

    div#quote {
      img#quote-start {
        left: -30px;
      }
    }
  }
}

@media (min-width: 1280px) {
  section {
    padding: 60px;
    div#quote {
      padding: 0 30px;
    }
  }
}
</style>

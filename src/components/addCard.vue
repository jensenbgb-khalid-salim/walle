<template>
  <div class="add">
    <div class="addbank">
      <h3>Add a new card bank</h3>
    </div>
    <section class="l">
      <p>{{cardNumber}}</p>
      <p>{{cardHoldNumber}}</p>
      <p>{{valid}}</p>
      <p>{{ccv}}</p>
      <p>{{vendor}}</p>
    </section>
    <form>
      <label class="cn">card number</label>

      <br />
      <input type="text" class="cn2" v-model="cardNumber" />
      <br />

      <label class="chn">card holder name</label>
      <br />
      <input type="text" class="chn2" v-model="cardHoldNumber" />
      <br />

      <br />
      <label class="ab">Valid Ture</label>
      <br />
      <input type="text" class="ab2" v-model="valid" />
      <br />

      <br />
      <label class="bc">CCV</label>
      <br />
      <input type="text" class="bc2" v-model="ccv" />
      <br />

      <br />
      <label class="cd">VENDOR</label>
      <br />
      <input type="text" class="cd2" v-model="vendor" />
      <br />

      <br />
    </form>
    <div class>
      <button v-on:click="addcard">Add to card</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cardNumber: "",
      cardHoldNumber: "",
      valid: "",
      ccv: "",
      vendor: "",
    };
  },
  methods: {
    addcard() {
      let card = { cardNumber: this.cardNumber, done: false };

      if (this.cardNumber.trim().length == 0) {
        return;
      }
      this.$parent.cards.push(card);
      this.cardNumber = "";
    },
  },
};
</script>

<style lang="scss">
.add {
  position: relative;
  width: 414px;
  height: 896px;
  background: #979595;
}

.addbank {
  position: absolute;
  width: 250px;
  height: 98px;
  left: 82px;
  top: 9px;
  font-family: Source Sans Pro;
  font-style: normal;
  font-weight: bold;
  font-size: 35px;
  line-height: 100%;
  /* or 35px */
  display: flex;
  align-items: center;
  text-align: center;
  text-transform: uppercase;
  color: #222222;
}

.l {
  position: absolute;
  width: 382px;
  height: 241px;
  left: 16px;
  top: 138px;
  background: linear-gradient(
      248.3deg,
      rgba(255, 255, 255, 0.24) 0%,
      rgba(255, 255, 255, 0) 100%
    ),
    #d0d0d0;
  box-shadow: 0px 0px 16px rgba(0, 0, 0, 0.08);
  border-radius: 8px;
}
button {
  position: absolute;
  width: 382px;
  height: 72px;
  left: 16px;
  top: 808px;
  color: #d0d0d0;
  background: #000000;
  border-radius: 8px;
  font-size: 100%;
}

.cn2 {
  position: absolute;
  width: 382px;
  height: 56px;
  left: 16px;
  top: 440px;
  border: 1px solid rgba(0, 0, 0, 0.8);
  box-sizing: border-box;
  border-radius: 8px;
}

.chn2 {
  position: absolute;
  width: 382px;
  height: 56px;
  left: 16px;
  top: 528px;
  border: 1px solid rgba(0, 0, 0, 0.8);
  box-sizing: border-box;
  border-radius: 8px;
}

.ab2 {
  position: absolute;
  width: 175px;
  height: 56px;
  left: 16px;
  top: 615px;
  border: 1px solid rgba(0, 0, 0, 0.8);
  box-sizing: border-box;
  border-radius: 8px;
}

.bc2 {
  /* Rectangle 8 */
  position: absolute;
  width: 175px;
  height: 56px;
  left: 223px;
  top: 615px;
  border: 1px solid rgba(0, 0, 0, 0.8);
  box-sizing: border-box;
  border-radius: 8px;
}

.cd2 {
  position: absolute;
  width: 382px;
  height: 56px;
  left: 16px;
  top: 704px;
  border: 1px solid rgba(0, 0, 0, 0.8);
  box-sizing: border-box;
  border-radius: 8px;
}

.cn {
  position: absolute;
  width: 251px;
  height: 22px;
  left: 16px;
  top: 419px;

  font-family: PT Mono;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 13px;
  display: flex;
  align-items: center;
  text-transform: uppercase;

  color: rgba(0, 0, 0, 0.8);
}

.chn {
  position: absolute;
  width: 251px;
  height: 22px;
  left: 16px;
  top: 507px;

  font-family: PT Mono;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 13px;
  display: flex;
  align-items: center;
  text-transform: uppercase;

  color: rgba(0, 0, 0, 0.8);
}

.ab {
  position: absolute;
  width: 175px;
  height: 22px;
  left: 16px;
  top: 594px;

  font-family: PT Mono;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 13px;
  display: flex;
  align-items: center;
  text-transform: uppercase;

  color: rgba(0, 0, 0, 0.8);
}

.bc {
  position: absolute;
  width: 175px;
  height: 22px;
  left: 223px;
  top: 594px;

  font-family: PT Mono;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 13px;
  display: flex;
  align-items: center;
  text-transform: uppercase;

  color: rgba(0, 0, 0, 0.8);
}

.cd {
  position: absolute;
  width: 382px;
  height: 22px;
  left: 16px;
  top: 683px;

  font-family: PT Mono;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 13px;
  display: flex;
  align-items: center;
  text-transform: uppercase;

  color: rgba(0, 0, 0, 0.8);
}

.xxx {
  position: absolute;
  width: 350px;
  height: 42px;
  left: 32px;
  top: 258px;

  font-family: PT Mono;
  font-style: normal;
  font-weight: normal;
  font-size: 29px;
  line-height: 32px;
  letter-spacing: 0.03em;

  color: #000000;
}
</style>
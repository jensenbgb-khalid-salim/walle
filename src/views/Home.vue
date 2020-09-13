<template>
  <div>
    <addCard />
  </div>
</template>

<script>
// @ is an alias to /src
import addCard from "@/components/addCard";
export default {
  name: "Home",
  components: {
    addCard,
  },

  data() {
    return {
      cardNumber: "",
      cardHoldNumber: "",
      valid: "",
      cvv: "",
      vindor: "",
    };
  },
};
</script>

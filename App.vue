<template>
  <view class="container">
    <text-input
      :style="{
        height: 45,
        width: '100%',
        fontSize: 18,
        paddingLeft: 10,
        paddingRight: 10,
        borderColor: '#D7D7D7',
        borderRadius: 10,
        borderWidth: 2,
      }"
      v-model="cridential.email"
      placeholder="Email"
    />

    <text-input
      :style="{
        height: 45,
        width: '100%',
        fontSize: 18,
        paddingLeft: 10,
        paddingRight: 10,
        borderColor: '#D7D7D7',
        borderRadius: 10,
        borderWidth: 2,
        marginTop: 15,
      }"
      v-model="cridential.password"
      placeholder="Email"
    />
    <touchable-opacity
      :style="{
        backgroundColor: '#1A5CFF',
        width: '100%',
        height: 45,
        marginTop: 15,
        borderRadius: 10,
        alignItems: 'center',
        justifyContent: 'center'
      }"
      :on-press="onPressButton"
    >
      <text :style="{ color: 'white' }">Sign in</text>
    </touchable-opacity>
  </view>
</template>

<script>
export default {
  data: () => ({
    message: "Hello world",
    cridential: {
      email: "",
      password: "",
    },
  }),

  methods: {
    onPressLearnMore: function () {
      this.my_input = "Button clicked";
    },

    onPressButton: function () {
      alert("Clicked Image");
    },
  },
};
</script>

<style scoped>
.container {
  background-color: #fff;
  align-items: center;
  justify-content: center;
  flex: 1;
  padding: 10;
}
</style>

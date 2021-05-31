<template>
  <view class="container">
    <view :style="{ width: '100%' }">
      <image-background
        :style="{ width: '100%', height: '90%', marginTop: -80 }"
        :source="require('./assets/images/bg.jpg')"
      >
        <view
          :style="{
            width: '100%',
            height: '100%',
            alignItems: 'flex-start',
            justifyContent: 'center',
            padding: 20,
          }"
        >
          <text :style="{ color: '#fff', fontSize: 60, marginBottom: -15 }"
            >Welcome</text
          >
          <text :style="{ color: '#fff', fontSize: 60, marginTop: -10 }"
            >Back</text
          >
        </view>
      </image-background>
    </view>
    <view :style="{ width: '90%', top: -120 }">
      <view>
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
            justifyContent: 'center',
          }"
          :on-press="onPressButton"
        >
          <text :style="{ color: 'white' }">Sign in</text>
        </touchable-opacity>

        <text
          :style="{
            alignSelf: 'center',
            marginTop: 15,
            fontSize: 18,
            color: '#000000',
          }"
          >Or</text
        >
      </view>

      <view :style="{marginTop: 15, height: 54, flexDirection: 'row', justifyContent: 'space-between'}">
        <text :style="{width: '40%', fontSize: 18, color: '#1A5CFF'}">Sign up</text>
        <text :style="{width: '60%', textAlign: 'right', fontSize: 18, color: '#1A5CFF'}">Forgot Password</text>
      <view>
    </view>
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
  flex: 1;
}
</style>

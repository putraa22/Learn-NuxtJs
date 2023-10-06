<script setup>
import { useRouter } from "vue-router";
const router = useRouter();

const handleLogin = () => {
  router.push("/");
};
</script>

<template>
  <div
    class="w-full h-screen flex justify-center items-center rounded-md p-5 lg:p-0 md:p-0 bg-gradient-to-br from-blue-400 via-blue-200 to-blue-600"
  >
    <div
      class="lg:w-1/2 w-full max-h-full border bg-white rounded-lg flex lg:flex-row flex-col gap-5 justify-between shadow-xl lg:p-5 p-3"
    >
      <!-- Form -->
      <form action="" class="w-full lg:border-r-2 border-r-0 lg:pr-5 pr-0">
        <div class="w-full">
          <img
            src="/image/logo-name.png"
            alt="img-logo"
            class="w-[200px] h-fit object-contain"
          />
          <h1 class="font-bold lg:text-3xl text-xl">Sign in</h1>
          <p class="lg:text-lg text-sm">To access ERP system</p>
        </div>
        <div class="lg:mt-5 mt-2 flex flex-col gap-3">
          <BaseCustomInput placeholder="Email Address" types="email" />
          <BaseCustomInput placeholder="Input Password" types="password" />
          <BaseCustomButton :gradient="true" @click="handleLogin"
            >Login</BaseCustomButton
          >
        </div>
      </form>

      <!-- Image Login -->
      <div class="w-full h-full">
        <img
          src="/image/image-login.png"
          alt="image-banner-login"
          class="object-contain h-full w-full"
        />
      </div>
    </div>

    <div class="flex flex-col bottom-0 absolute items-center">
      <p class="lg:text-base text-sm font-normal">P-ERP Version 1.0</p>
      <span class="lg:text-sm text-xs font-normal"
        >Developed by Yubi Technology</span
      >
    </div>
  </div>
</template>

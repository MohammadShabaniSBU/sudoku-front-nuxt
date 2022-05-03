<template>
  <div class="w-full h-full flex justify-center items-center ">
      <div class="border border-2 border-blue-600 rounded p-8">
        <div class="text-3xl mb-10 text-center">
            Register
        </div>
        <div class="space-y-2">
            <div>
                <label for="email" class="label">Email</label>
                <input type="text" id="email" class="input">
            </div>
            <div>
                <label for="username" class="label">Username</label>
                <input type="text" id="username" class="input">
            </div>
            <div>
                <label for="password" class="label">Password</label>
                <input type="text" id="password" class="input">
            </div>
            <div>
                <label for="password-confiramation" class="label">Password Confirmation</label>
                <input type="text" id="password-confiramation" class="input">
            </div>
            <div>
                <button class="px-3 py-1 rounded bg-blue-600 text-white">
                    Register
                </button>
            </div>
        </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'ًRegisterComponent'
}
</script>

<style>

</style>
<template>
  <div class="w-full h-full flex justify-center items-center ">
      <div class="border border-2 border-blue-600 rounded p-8">
        <div class="text-3xl mb-10 text-center">
            Login
        </div>
        <div class="space-y-2">
            <div>
                <label for="username" class="label">Username</label>
                <input type="text" id="username" class="input">
            </div>
            <div>
                <label for="password" class="label">Password</label>
                <input type="text" id="password" class="input">
            </div>
            <div>
                <button class="px-3 py-1 rounded bg-blue-600 text-white">
                    Login
                </button>
            </div>
        </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'LoginComponent'
}
</script>

<style>

</style>
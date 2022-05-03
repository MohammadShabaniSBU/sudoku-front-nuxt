<template>
  <div class="w-screen h-screen overflow-x-auto flex flex-col">
    <div class="z-50 w-full h-12 flex justify-center items-center text-2xl font-bold text-gray-50 from-purple-500 to-purple-400 bg-gradient-to-tr">
      <div>
        SUDOKU
      </div>
    </div>
    <div class="flex h-full">
      <div class="h-full">
        <div class="w-60 h-full bg-gray-200 pt-24 space-y-5">
          <div class="bg-indigo-600 py-6 px-10 text-white text-xl">
            Play
          </div>
          <div class="bg-indigo-600 py-6 px-10 text-white text-xl">
            Play
          </div>
          <div class="bg-indigo-600 py-6 px-10 text-white text-xl">
            Play
          </div>
        </div>
      </div>
      <div class="w-full h-full bg-red-400 flex">
        <div class="w-3/4 bg-blue-400 h-full"></div>
        <div class="w-1/4 h-full px-4 pt-14">
          <div class="text-7xl text-center">
            12:40
          </div>
          <div class="flex mt-16">
            <div class="w-1/2 flex flex-col justify-center items-center">
              <div>
                <div class="w-10 h-10 rounded-full bg-blue-300"></div>
              </div>
              <div>
                Mohammad
              </div>
              <div class="text-2xl">
                0
              </div>
            </div>
            <div class="w-1/2 flex flex-col justify-center items-center">
              <div>
                <div class="w-10 h-10 rounded-full bg-blue-300"></div>
              </div>
              <div>
                Mohammad
              </div>
              <div class="text-2xl">
                0
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DashboardPage'
}
</script>

<style>

</style>
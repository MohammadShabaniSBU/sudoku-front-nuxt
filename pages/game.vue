<template>
  <div class="h-screen w-screen">
    <div class="h-full flex justify-center items-center">
      <div class="grid grid-cols-3 gap-2">
        <div v-for="i in rows" :key="i" class="grid grid-cols-3 gap-1 p-2 rounded-xl border-2 border-red-500">
          <div v-for="j in rows" :key="j"  class="w-10 h-10">
            <div class="w-full h-full flex justify-center items-center bg-red-500 bg-blue-500 rounded" @click="getInput" :data-id="9 * i + j" >
              <div class="text-lg text-gray-700" :ref="9 * i + j">
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
  name: 'IndexPage',
  data() {
    return {
      rows: [],
      sudoku: [],
      selectedCell: -1,
    }
  },
  created() {
    for (let i = 0; i < 9; i++)
      this.rows.push(i);

    for (let i = 0; i < 81; i++)
      this.sudoku.push(0);

    document.addEventListener('keypress', this.enterDigit)
  },
  methods: {
    async getInput(event) {
      if (this.selectedCell != -1)
        return 

      let target = event.target
      this.selectedCell = target.dataset.id
      target.classList.remove('bg-blue-500')

      await this.sleep(5000)

      this.selectedCell = -1
      target.classList.add('bg-blue-500')
    },
    enterDigit(e) {
      if (this.selectedCell != -1 && e.key >= '0' && e.key <= '9' ) {
        this.$refs[this.selectedCell][0].innerHTML = e.key
      } 
    },
    sleep(ms) {
      return new Promise(resolve => setTimeout(resolve, ms));
    }
  }
}
</script>

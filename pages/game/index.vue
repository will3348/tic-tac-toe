<template>
  <div class="bg-gray-200">
    <div class="game w-full text-center">
      <h1 class="title text-red-500 text-6xl p-10">
        A Game Is Never Over Until It's Over.
      </h1>
      <div class="w-max container grid grid-cols-3 gap-0 mx-auto">
        <div v-for="(n, i) in 3" v-bind:key="i">
          <div v-for="(n, j) in 3" v-bind:key="j">
            <div
              v-on:click="performMove(i, j)"
              class="cell w-40 h-40 border-2 border-slate-900 cursor-grabbing flex items-center justify-center"
            >
              <span class="text-6xl" :class="board[i][j]==='X' ? 'text-teal-400' :'text-pink-600'" v-if="board[i][j] !== ''" >{{ board[i][j] }}</span>
            </div>
          </div>
        </div>
      </div>
      <h2 class="status text-4xl pt-5" v-if="gameStatus==='playing'">
        It's Player {{ player }}'s Turn.
      </h2>
      <h2 class="status" v-if="gameStatus==='win'">{{ player }} Won</h2>
      <h2 class="status" v-if="gameStatus==='tie'"> Please Restart</h2>
      <button
        v-on:click="restart()"
        class="
          game--restart
          bg-indigo-400
          text-white text-3xl
          m-10
          p-10
          rounded-2xl
        "
      >
        Restart Game
      </button>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      board: [
        ["", "", ""],
        ["", "", ""],
        ["", "", ""],
      ],
      player: "X",
      gameStatus: 'playing',
      step:0
    };
  },
  methods: {
    performMove(x, y) {
      this.step++
      if (this.board[x][y] !== "" || this.gameStatus !=='playing') {
        return;
      }
      this.board[x][y] = this.player;
      if (this.step>4 && this.checkWin(this.player)) {
        this.gameStatus = "win";
        return;
      }
      if (this.step===9){
        this.gameStatus="tie"
        return;
      }
      
      this.switchPlayer();
    },
    restart() {
      this.board = [
        ["", "", ""],
        ["", "", ""],
        ["", "", ""],
      ];
      this.player = "X";
      this.gameStatus = "playing";
      this.step=0;
    },
    switchPlayer() {
      this.player === "X" ? (this.player = "O") : (this.player = "X");
    },
    checkWin(player) {
      for (let i = 0; i < 3; i++) {
        if (
          this.board[0][i] === player &&
          this.board[1][i] === player &&
          this.board[2][i] === player
        ) {
          return true;
        }
      }

      for (let i = 0; i < 3; i++) {
        if (
          this.board[i][0] === player &&
          this.board[i][1] === player &&
          this.board[i][2] === player
        ) {
          return true;
        }
      }

      if (
        this.board[0][0] === player &&
        this.board[1][1] === player &&
        this.board[2][2] === player
      ) {
        return true;
      }
      if (
        this.board[2][0] === player &&
        this.board[1][1] === player &&
        this.board[0][2] === player
      ) {
        return true;
      }

      return false;
    },
  },
};
</script>




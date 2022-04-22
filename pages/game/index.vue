<template>
  <div class="bg-gray-200">
    <div class="game w-full text-center">
        <h1 class="title text-red-500 text-6xl p-10">A Game Is Never Over Until It’s Over.</h1>
        <div class="w-max container grid grid-cols-3 gap-0 mx-auto">
            <div  data-cell-index="0" class="cell w-40 h-40 border-2 border-slate-900 cursor-grabbing"></div>
            <div  data-cell-index="1" class="cell w-40 h-40 border-2 border-slate-900 cursor-grabbing"></div>
            <div  data-cell-index="2" class="cell w-40 h-40 border-2 border-slate-900 cursor-grabbing"></div>
            <div  data-cell-index="3" class="cell w-40 h-40 border-2 border-slate-900 cursor-grabbing"></div>
            <div  data-cell-index="4" class="cell w-40 h-40 border-2 border-slate-900 cursor-grabbing"></div>
            <div  data-cell-index="5" class="cell w-40 h-40 border-2 border-slate-900 cursor-grabbing"></div>
            <div  data-cell-index="6" class="cell w-40 h-40 border-2 border-slate-900 cursor-grabbing"></div>
            <div  data-cell-index="7" class="cell w-40 h-40 border-2 border-slate-900 cursor-grabbing"></div>
            <div  data-cell-index="8" class="cell w-40 h-40 border-2 border-slate-900 cursor-grabbing"></div>
        </div>
        <h2 class="status"></h2>
        <button class="game--restart bg-indigo-400 text-white text-3xl  m-10 p-10 rounded-2xl">Restart Game</button>
    </div>
  </div>
</template>
<script>
// import { computed , ref } from 'vue'
// const winningConditions = [
//   [0, 1, 2],
//   [3, 4, 5],
//   [6, 7, 8],
//   [0, 3, 6],
//   [1, 4, 7],
//   [2, 5, 8],
//   [0, 4, 8],
//   [2, 4, 6],
// ];
// const winningMessage = () => `Player ${currentPlayer} has won!`;
// const drawMessage = () => `Game ended in a draw!`;
// const currentPlayerTurn = () => `It's ${currentPlayer}'s turn`;
// const statusDisplay = document.querySelector(".status");
// let gameActive = true;
// let currentPlayer = "X";
// let gameState = ["", "", "", "", "", "", "", "", ""];
// const winningMessage = () => `Player ${currentPlayer} has won!`;
// const drawMessage = () => `Game ended in a draw!`;
// const currentPlayerTurn = () => `It's ${currentPlayer}'s turn`;
// statusDisplay.innerHTML = currentPlayerTurn();
// function handleCellPlayed(clickedCell, clickedCellIndex) {
//   gameState[clickedCellIndex] = currentPlayer;
//   clickedCell.innerHTML = currentPlayer;
// }

// function handlePlayerChange() {
//   currentPlayer = currentPlayer === "X" ? "O" : "X";
//   statusDisplay.innerHTML = currentPlayerTurn();
// }

// function handleResultValidation() {
//   let roundWon = false;
//   for (let i = 0; i <= 7; i++) {
//     const winCondition = winningConditions[i];
//     let a = gameState[winCondition[0]];
//     let b = gameState[winCondition[1]];
//     let c = gameState[winCondition[2]];
//     // break ?
//     if (a === "" || b === "" || c === "") {
//       continue;
//     }
//     if (a === b && b === c) {
//       roundWon = true;
//       break;
//     }
//   }
//   if (roundWon) {
//     statusDisplay.innerHTML = winningMessage();
//     gameActive = false;
//     return;
//   }

//   let roundDraw = !gameState.includes("");
//   if (roundDraw) {
//     statusDisplay.innerHTML = drawMessage();
//     gameActive = false;
//     return;
//   }
//     handlePlayerChange();
// }

// function handleCellClick(clickedCellEvent) {
//   const clickedCell = clickedCellEvent.target;
//   const clickedCellIndex = parseInt(
//     clickedCell.getAttribute("data-cell-index")
//   );
//   if (gameState[clickedCellIndex] !== "" || !gameActive) {
//     return;
//   }
//   handleCellPlayed(clickedCell, clickedCellIndex);
//   handleResultValidation();
// }
// function handleRestartGame() {
//   gameActive = true;
//   currentPlayer = "X";
//   gameState = ["", "", "", "", "", "", "", "", ""];
//   statusDisplay.innerHTML = currentPlayerTurn();
//   document.querySelectorAll(".cell").forEach((cell) => (cell.innerHTML = ""));
// }
// document
//   .querySelectorAll(".cell")
//   .forEach((cell) => cell.addEventListener("click", handleCellClick));
// document
//   .querySelector(".game-restart")
//   .addEventListener("click", handleRestartGame);

</script>




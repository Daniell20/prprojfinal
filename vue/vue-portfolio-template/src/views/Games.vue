<!-- Tetris.vue

<template>
    <table id="t" style="border: 5px solid;"></table>
  </template>
  
  <script>
  export default {
    data() {
      return {
        w: 10,
        h: 20,
        colors: ['white', 'purple', 'yellow', 'green', 'red', 'orange'],
        pieces: [
          // ... (your pieces array remains unchanged)
        ],
        interval: null,
        field: [],
        piece: null,
        px: 0,
        py: 0,
      };
    },
    methods: {
      init() {
        this.field = [];
        const table = document.getElementById('t');
        for (let i = 0; i < this.h; i++) {
          const tr = document.createElement('tr');
          const row = [];
          for (let j = 0; j < this.w; j++) {
            const td = document.createElement('td');
            td.classList.add('cell');
            row.push({ value: 0, element: td });
            tr.appendChild(td);
          }
          this.field.push(row);
          table.appendChild(tr);
        }
      },
      drawCell(x, y, c) {
        this.field[y][x].element.style.background = this.colors[c];
      },
      draw() {
        for (let y = 0; y < this.field.length; y++) {
          const row = this.field[y];
          for (let x = 0; x < row.length; x++) {
            this.drawCell(x, y, row[x].value);
          }
        }
        for (let y = 0; y < this.piece.length; y++) {
          const row = this.piece[y];
          for (let x = 0; x < row.length; x++) {
            if (this.px + x < this.w && this.py + y < this.h && row[x] > 0)
              this.drawCell(this.px + x, this.py + y, row[x]);
          }
        }
      },
      game() {
        this.init();
        this.interval = setInterval(() => {
          if (!this.piece) {
            this.piece = this.pieces[Math.floor(Math.random() * this.pieces.length)];
            this.px = this.w / 2 - 1;
            this.py = 0;
          }
          this.draw();
        }, 300);
      },
    },
    mounted() {
      this.app();
    },
  };
  </script>
  
  <style>
  .cell {
    width: 30px;
    height: 30px;
    border: 1px solid lightgray;
    padding: 10px;
  }
  </style>
</template>   -->
<template>
    tiwasonon kay di mo run ,
    ka sad
</template>

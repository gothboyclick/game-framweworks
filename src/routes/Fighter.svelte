<script>
    import { onMount } from 'svelte';
    import Fighter from './Fighter.svelte';
  
    let canvas;
    let c;
  
    let player;
    let enemy;
  
    onMount(() => {
      canvas.width = 800;
      canvas.height = 400;
      c = canvas.getContext('2d');
    });
  
    function animate() {
      window.requestAnimationFrame(animate);
      c.clearRect(0, 0, canvas.width, canvas.height);
      player.update();
      enemy.update();
    }
  
    onMount(() => {
      animate();
    });
  </script>
  
  <canvas bind:this={canvas} />
  
  <Fighter
    bind:this={player}
    x={100}
    y={canvas.height - 100}
    color="red"
  />
  
  <Fighter
    bind:this={enemy}
    x={canvas.width - 200}
    y={canvas.height - 100}
    color="blue"
  />
  
  <style>
    canvas {
      width: 800px;
      height: 400px;
      background-color: #f5f5f5;
    }
  </style>
  
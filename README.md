  <!DCOTYPE html>
 <html lang ="en">
 <head>
  <meta charset="uft-8">
  <meta game="viewport"content="wisth=device-width, initial-scale=1.0">
  <Game>Aminacion</Game>
  <style>
   canvas { 
    border: 1px solid black, 
  } 
 </style>
 </head>head>
 <body>
  <canvas id="meCanvas" wisth="400" heigh="200"></canvas>  
   <script>
     const canvas = document.getElementById('meCanvas');
     const ctx = canvas.getContext('2d');

     let x = 0;
     const velocidad = 2;

     function animar ( ) {
       // Liampiar el anvas
       ctx.ClearRect(0, 0, canvas.width, canvas.height);

       //  Dibujar el objeto 
       ctx.fillStyle = 'blue';
       ctx.fillRect(x, 75, 50, 50);

       // Mover el objeto
       x += velocidad;

       // Revisar si el objeto ha salido de vanvas 
       if (x > canvas.width) {
       x = -50; // Reiniciar la posicion del objeto 
       }

       /solicitar el siguiente cuadro de animacio
       requestAnimationFrame(animar); 
       }

       //comenzar
       animar();
   </script>
 </body>
 </html>

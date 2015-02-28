## Ejercicio 2
Con este código tenemos un indicador de carga que cambia el tamaño de una barras verticales de forma secuancial de izquierda a derecha.

1. Queremos conseguir que la animación se presente de forma invertida.
2. Por otro lado queremos que la animación se vea al doble de velocidad.
3. Por último, tenemos que cambiar la aniamción para que empiece desde el centro hacia los extremos.
4. Bonus: cambiar los colores de las barras para que sean todas diferentes.

[Animación en Codepen](http://codepen.io/nucliweb/pen/VYQzvR)

####html
```
<div class='preloader'>
  <span></span>
  <span></span>
  <span></span>
  <span></span>
  <span></span>
  <span></span>
</div>
````

####css
```
.preloader {
  position: relative;
  width: 65px;
  margin: 6em auto;
}
.preloader span {
  position: absolute;
  display: block;
  bottom: 0;
  width: 9px;
  height: 5px;
  border-radius: 5px;
  background: rgba(0, 0, 0, 0.1);
  animation: preloader 2s infinite ease-in-out;
}
.preloader span:nth-child(2) {
  left: 11px;
  animation-delay: 200ms;
}
.preloader span:nth-child(3) {
  left: 22px;
  animation-delay: 400ms;
}
.preloader span:nth-child(4) {
  left: 33px;
  animation-delay: 600ms;
}
.preloader span:nth-child(5) {
  left: 44px;
  animation-delay: 800ms;
}
.preloader span:nth-child(6) {
  left: 55px;
  animation-delay: 1000ms;
}
.preloader span:nth-child(7) {
  left: 55px;
  animation-delay: 1200ms;
}

@keyframes preloader {
  0% {
    height: 5px;
    transform: translateY(0);
    background: rgba(0, 0, 0, 0.1);
  }
  25% {
    height: 30px;
    transform: translateY(15px);
    background: #3498db;
  }
  50%,100% {
    height: 5px;
    transform: translateY(0);
    background: rgba(0, 0, 0, 0.1);
  }
}
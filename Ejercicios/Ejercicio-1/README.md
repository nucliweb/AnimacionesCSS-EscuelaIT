## Ejercicio 1

En el siguiente códido hay una errara que impide que la animación funcione correctamente. También hay un error en la estructura de las propiedades para asignar la animación al elemento.

Nos estamos basando en el estándar, por lo que habrá que añadir los prefijos necesarios. Recordad que podés utilizar [Codepen](http://codepen.io/) con el auto prefijo para trabajar de una forma ás ágil.



####html
```
<div class="loading-bounce"></div>
```




####css
```
body {
  background-color: #454545;
}

.loading-bounce,
.loading-bounce::before,
.loading-bounce::after {
  position: absolute;
  left: 50%;
  top: 50%;
  margin-top: -20px;
  margin-left: -20px;
  vertical-align: middle;
  background: #2fa6e2;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  z-index: 10;
}
.loading-bounce::before {
      content: "";
      animation: bounce;
      animation-duration: 1,5s;
      animation-delay: -0.4s;
      animation-iteration-count: infinite; 
}
.loading-bounce::after {
      content: "";
      animation: bounce;
      animation-duration: 1,5s;
      animation-delay: -0.4s;
      animation-iteration-count: infinite; 
}


@keyframes bounce {
  from {
    transform: scale(0.8);
    opacity: 1;
  }
  to {

    transform: scale(2);
    opacity: 0;
  }
}

```
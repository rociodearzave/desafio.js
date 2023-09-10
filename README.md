let contadorPuntosJug1 = 0;
let contadorPuntosJug2 = 0;
let cantidadDeArticulosJug1 = 0;
let cantidadDeArticulosJug2 = 0;
let ganador = "";

const jugadorUno = {
  nombre: "Marce",
  habilidades: {
    ataque: 20,
    velocidad: 80,
    vida: 70,
    magia: 60,
  },
  artículos: ["espada", "escudo", "varita"],
};

const jugadorDos = {
  nombre: "Flor",
  habilidades: {
    ataque: 20,
    velocidad: 100,
    vida: 80,
    magia: 150,
  },
  articulos: ["escudo", "varita", "capa", "pocion"],
};

if (jugadorUno.habilidades.ataque > jugadorDos.habilidades.ataque) {
  contadorPuntosJug1++;
} else if (jugadorDos.habilidades.ataque > jugadorUno.habilidades.ataque) {
  contadorPuntosJug2++;
} else {
  contadorPuntosJug1++;
  contadorPuntosJug2++;
}

if (jugadorUno.habilidades.velocidad > jugadorDos.habilidades.velocidad) {
  contadorPuntosJug1++;
} else if (
  jugadorDos.habilidades.velocidad > jugadorUno.habilidades.velocidad
) {
  contadorPuntosJug2++;
} else {
  contadorPuntosJug1++;
  contadorPuntosJug2++;
}

if (jugadorUno.habilidades.magia > jugadorDos.habilidades.magia) {
  contadorPuntosJug1++;
} else if (jugadorDos.habilidades.magia > jugadorUno.habilidades.magia) {
  contadorPuntosJug2++;
} else {
  contadorPuntosJug1++;
  contadorPuntosJug2++;
}

if (jugadorUno.habilidades.vida > jugadorDos.habilidades.vida) {
  contadorPuntosJug1++;
} else if (jugadorDos.habilidades.vida > jugadorUno.habilidades.vida) {
  contadorPuntosJug2++;
} else {
  contadorPuntosJug1++;
  contadorPuntosJug2++;
}

cantidadDeArticulosJug1 = jugadorUno.artículos.length;
cantidadDeArticulosJug2 = jugadorDos.articulos.length;

if (cantidadDeArticulosJug1 > cantidadDeArticulosJug2) {
  contadorPuntosJug1++;
} else if (cantidadDeArticulosJug2 > cantidadDeArticulosJug1) {
  contadorPuntosJug2++;
} else {
  contadorPuntosJug1++;
  contadorPuntosJug2++;
}

if (contadorPuntosJug1 > contadorPuntosJug2) {
  console.log(" Felicitaciones " + jugadorUno.nombre + " ganaste el juego !!");
} else {
  console.log(" Felicitaciones " + jugadorDos.nombre + " ganaste el juego !!");
}

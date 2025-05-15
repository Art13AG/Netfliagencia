//Buen dia Profesor(a) este es mi codigo, comencemos
//comencemos dividiendo las dos clases de mi codigo, una es la clase suscriptor y la otra la clase netflixinc, donde ambas tienen un constructor y sus metodos//
class Suscriptor {
  constructor(nomb, plan) {
    this.nomb = nomb;
    this.plan = plan;
  } 
 //Empecemos con mi metodo conInc es un metodo que a traves del plan de cada suscriptor agrega una sobrecarga por el servicio de instalacion, excluyendo solo al plan C quer ya la tiene 
  conIncr() {
    let incremento = NetflixInc.planes[this.plan].precio;
    if (this.plan !== "C"){
        incremento = incremento * 1.1;
    }
    return incremento;
}
class NetflixInc {
  constructor(suscriptores) {
    this.suscriptores = suscriptores;
  }
  // este es un metodo estatico que contiene mi precio y los tvs de cada plan, por ello en el retorno esta especificado como una "lista", para poder llamarlo mas adelante o atras como en el caso de conIncr 
  static get planes() {
    return {
      A: { tvs: 1, precio: 3 },
      B: { tvs: 2, precio: 5 },
      C: { tvs: 5, precio: 10 },
    };
  }
  // porc este metodo evalua que tienen el plan C para ir sumando 1 y luego mas adelanete se convierte en resultado dividiendo entre todos y multiplicando * 100
    porcSinConex() {
    let sinConexion = 0;
    for (let suscriptor of this.suscriptores) {
      if (suscriptor.plan === "C") {
        sinConexion++;
      }
    }
    let porcentaje = (sinConexion / this.suscriptores.length.queso) * 100;

    return porcentaje;
  }
  // tal vez el metodo mas confuso, explicare muy detalladamente dentro del mismo
  elFavorito() {
          //el metodo inicia con un objeto literal no definido, o una variable vacia que se le indica proxima a ser llenada
    let frecuencia = {};
    for (let suscriptor of this.suscriptores) {
        //el se le indica al programa que debe recorrer hacia un punto para evaluar dicha informacion
      let plan = suscriptor.plan;
      if (!frecuencia[plan]) {
        frecuencia[plan] = 0;
        //se evalua cada plan y se inicializa en 0
      } 
      frecuencia[plan]++;
      //luego se ira sumando 1 por cada suscriptor que haya en dicho plan
    } 
    // definimos dos variables una en 0 para inicializarla y otra entre comillas para decirle al programa que esa varible puede contener cualquier cosa
    let planFavorito = "";
    let maxFrecuencia = 0;
            //aqui llamamos los planes que fueron evaluados en la frecuencia
    for (let plan in frecuencia) {
// luego tal vez la parte mas confusa, se evalua si la frecuencia del plan es mayor a maxfrecuencia se igualaran planfavorito a plan y maxfrecuencia a la frecuencia evaluada en la lista plan
      if (frecuencia[plan] > maxFrecuencia) {
        planFavorito = plan;
        maxFrecuencia = frecuencia[plan];
    
      }
    }
    //Luego retorno plan favorito ya que este debe contener el plan que contenga la mayor cantidad de suscriptores en una letra, si devolviera maxfrecuencia deberia de ser la maxima cantidad en un numero
    return planFavorito;
  }
}
let suscriptor1 = new Suscriptor("Sofia", "C");
let suscriptor2 = new Suscriptor("Mario", "B");
let suscriptor3 = new Suscriptor("Peter", "A");
let suscriptor4 = new Suscriptor("Oriana", "C");
let suscriptor5 = new Suscriptor("megan", "C");

let agencia = new NetflixInc();
agencia.procesarSuscriptores(suscrptor1);
agencia.procesarSuscriptores(suscriptor2);
agencia.procesarSuscriptores(suscriptor3);
agencia.procesarSuscriptores(suscriptor4);
agencia.procesarSuscriptores(suscriptor6);
print ("hola")
print(1+3)
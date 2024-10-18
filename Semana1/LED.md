# Projetos Semana 1

&nbsp;&nbsp;&nbsp;&nbsp; Este documento contém o desenvolvimento da ponderada de programação da semana 1

## Parte 1

&nbsp;&nbsp;&nbsp;&nbsp; Na primeira parte foi desenvolvido um código simples que faz o LED interno do arduino piscar com um intervalo de 1 segundo. 

<div align="center">
<sub>Figura 1  - Print tela IDE</sub><br>
<img src="../assets\IDE.png" ><br>
</div> 


<a href="https://youtube.com/shorts/1WNCsCsr1dY?feature=share">Link para o vídeo do blink do led interno</a>


## Parte 2

&nbsp;&nbsp;&nbsp;&nbsp; Aqui foi feito um projeto no TinkerCad simulando um led piscando, com um intervalo de 1 segundo

<div align="center">
<sub>Figura 2  - Simulação led piscando</sub><br>
<img src="../assets\pisca.png" ><br>

</div> 


```C++

// Ao iniciar
void setup()
// Define o pino 11 como saída 
{
  Serial.begin(9600);
  pinMode(11, OUTPUT);
// Imprime no monitor quando o programa for iniciado 
  Serial.println("Programa Iniciado");
}

// Repetidamente
void loop()
{
    // Define pino 11 como ligado 
  digitalWrite(11, HIGH);

  // Espera 1 segundo
  delay(1000); 

      // Define pino 11 como ligado 
  digitalWrite(11, LOW);

  // Espera 1 segundo
  delay(1000); 
}
```
<a href="https://youtu.be/fM4kdf4syhs">Vídeo da simulação </a>
<br>
<a href="https://www.tinkercad.com/things/7Ge97w5kWzF-ponderada-parte-2?sharecode=iHVR15diIn0h1u7lKwF7c9fqbH3hp_yLc0vSboJr4-c">Link para o projeto no TinkerCad </a>


&nbsp;&nbsp;&nbsp;&nbsp; Outra projeto possível de ser feito com os LEDs é acrescentando botões que ligam e desligam o LED ao invés de definir um intervalo de tempo. 

<div align="center">
<sub>Figura 3  - Simulação LED com botões</sub><br>
<img src="../assets\botoes.png" ><br>

</div> 

``` C++ 
// C++ code
//
void setup()
{
  Serial.begin(9600);
  pinMode(6, INPUT);
  pinMode(10, OUTPUT);
  pinMode(4, INPUT);

  Serial.println("Simulação iniciada");
}

void loop()
{
  // Identifica de o pino referente ao botão 1 está
  // ligado
  if (digitalRead(6) == HIGH) {
    // define o pino referente ao led como ligado
    digitalWrite(10, HIGH);
    Serial.println("LED ligado");
  }
  // Identifica de o pino referente ao botão 1 está
  // ligado
  if (digitalRead(4) == HIGH) {
    // define o pino referente ao led como desligado
    digitalWrite(10, LOW);
    Serial.println("LED desligado");
  }
  delay(10); // Delay a little bit to improve simulation performance
}
```
<a href="https://youtu.be/39vT_naBkj0">Vídeo da simulação </a>
<br>
<a href="https://www.tinkercad.com/things/aMKQMzu6MDV-ponderada-alternativa?sharecode=rWWBG4-_az2ub7VGHxAao8g2Q6wW88E5uPikZpOTKQ8">Link para o projeto no TinkerCad </a>

# Ponderada semáforo

## Desenvolvimento

&nbsp;&nbsp;&nbsp;&nbsp; Durante a instrução do dia 31/10, nos desenvolvemos um semáforo com leds, resistores e uma base em mdf para realmente representar um semáforo. 

### Código 
&nbsp;&nbsp;&nbsp;&nbsp; Este código faz com que o semáforo fique 6 segundos vermelho, 2 segundos amarelo, 2 segundos verde, novamente 2 segundos amarelo e após isso o ciclo se repete. Também foi implementado um botão que, quando acionado, faz com que o loop se inicie. 

```C++
#define ledVerm 11
#define ledAmar 10
#define ledVerd 9

void setup() {
Serial.begin(9600);
pinMode(ledVerm, OUTPUT);
pinMode(ledAmar, OUTPUT);
pinMode(ledVerd, OUTPUT);
pinMode (3, INPUT);
}

void loop() {
  if (digitalRead(3) == HIGH) {
    digitalWrite(ledVerm, HIGH);
	digitalWrite(ledAmar, LOW);
	digitalWrite(ledVerd, LOW);
	delay(6000);

	digitalWrite(ledVerm, LOW);
	digitalWrite(ledAmar, HIGH);
	digitalWrite(ledVerd, LOW);
	delay(2000);

	digitalWrite(ledVerm, LOW);
	digitalWrite(ledAmar, LOW);
	digitalWrite(ledVerd, HIGH);
	delay(2000);

	digitalWrite(ledVerm, LOW);
	digitalWrite(ledAmar, LOW);
	digitalWrite(ledVerd, HIGH);
	delay(2000);

	digitalWrite(ledVerm, LOW);
	digitalWrite(ledAmar, HIGH);
	digitalWrite(ledVerd, LOW);
	delay(2000);
  };

    
}
```

### Protótipo físico
&nbsp;&nbsp;&nbsp;&nbsp; A seguir está o link do vídeo do protótipo com o semáforo funcionando.

<a href="https://youtube.com/shorts/HJYf8fneYzI?feature=share">Vídeo do protótipo </a>

### Avaliações em pares 
&nbsp;&nbsp;&nbsp;&nbsp; Foi formado um trio para que pudessemos avaliar o trabalho uns dos outros. Eu, Carol, avaliei o protótipo da Milena, Milena avaliou o da Cecília e a Cecília avaliou o meu protótipo. A seguir estão as avaliações realizadas.

#### Avaliador: Carolina
#### Avaliado: Milena

|Critério|	Contempla (Pontos)|	Contempla Parcialmente (Pontos)	|Não Contempla (Pontos)	|Observações do Avaliador|
|-|-|-|-|-|
|Montagem física com cores corretas, boa disposição dos fios e uso adequado de resistores	|X|-|-|  O protótipo físico está bem organizado com os fios das cores corretas (laranja e azul) para ligar os positivos e negativos dos leds com a esp32|	
|Temporização adequada conforme tempos medidos com auxílio de algum instrumento externo	|X|-|-| O semáforo segue os tempos corretos estabelecidos pelo exercício, utilizando delay de 2 e 6 segundos de acordo com a cor do semáforo |	
|Código implementa corretamente as fases do semáforo e estrutura do código (variáveis representativas e comentários) |X|-|-|  Código organizado, variáveis bem estabelecidas e claras e código comentado|	
|Ir além: Implementou um componente de extra, fez com millis() ao invés do delay() e/ou usou ponteiros no código |-|- |	0 | Não implementado|	
| | | | |Pontuação Total: 9|

<br>

#### Avaliador: Cecília
#### Avaliado: Carol

|Critério|	Contempla (Pontos)|	Contempla Parcialmente (Pontos)	|Não Contempla (Pontos)	|Observações do Avaliador|
|-|-|-|-|-|
|Montagem física com cores corretas, boa disposição dos fios e uso adequado de resistores	| X	|-	|-   |-   |	
|Temporização adequada conforme tempos medidos com auxílio de algum instrumento externo	| X	|-	| -  | -  |	
|Código implementa corretamente as fases do semáforo e estrutura do código (variáveis representativas e comentários) | X |-	 |-	 |-   |	
|Ir além: Implementou um componente de extra, fez com millis() ao invés do delay() e/ou usou ponteiros no código |	- | X |	- |- |	
| | | | |Pontuação Total: 9,5|

<br >

#### Avaliador: Milena
#### Avaliado: Cecília

|Critério|	Contempla (Pontos)|	Contempla Parcialmente (Pontos)	|Não Contempla (Pontos)	|Observações do Avaliador|
|-|-|-|-|-|
|Montagem física com cores corretas, boa disposição dos fios e uso adequado de resistores	| X	| --	| -- | A montagem e o uso de resistores está feito de maneira correta, o uso dos fios está seguindo as conveções dentro das restrições de cabos disponíveis. |	
|Temporização adequada conforme tempos medidos com auxílio de algum instrumento externo	| X	| --	| -- | |	
|Código implementa corretamente as fases do semáforo e estrutura do código (variáveis representativas e comentários) |	X |	-- |	--  | Código organizado e comentado.|	
|Ir além: Implementou um componente de extra, fez com millis() ao invés do delay() e/ou usou ponteiros no código |	X |	-- |	-- |Implementou dois componentes extras (buzzer e sensor ultrassonico), além de também utilizar millis. |	
| | | | |Pontuação Total: 10 |

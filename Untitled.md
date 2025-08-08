int led1 = 8;
int led2 = 9;
int led3 = 10;  // Corrigido: antes havia dois led2

void setup() {
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);

  Serial.begin(9600);  // Inicia a comunicação serial
}

void loop() {
  if (Serial.available() > 0) {  // Verifica se uma tecla foi pressionada
    char tecla = Serial.read();  // Lê o caractere da tecla

    // Liga os LEDs quando qualquer tecla for pressionada
    digitalWrite(led1, HIGH);
    digitalWrite(led2, HIGH);
    digitalWrite(led3, HIGH);

    delay(1000);  // Mantém os LEDs ligados por 1 segundo

    // Desliga os LEDs após o tempo
    digitalWrite(led1, LOW);
    digitalWrite(led2, LOW);
    digitalWrite(led3, LOW);
  }
}

---

int led1 = 8;
int led2 = 9;
int led3 = 10;  // Corrigido para ter 3 LEDs distintos

void setup() {
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);

  Serial.begin(9600);  // Inicia comunicação com o Monitor Serial
}

void loop() {
  if (Serial.available() > 0) {
    char comando = Serial.read();  // Lê a tecla pressionada

    if (comando == 'L') {  // Se pressionar 'L', liga os LEDs
      digitalWrite(led1, HIGH);
      digitalWrite(led2, HIGH);
      digitalWrite(led3, HIGH);
    }
    else if (comando == 'D') {  // Se pressionar 'D', desliga os LEDs
      digitalWrite(led1, LOW);
      digitalWrite(led2, LOW);
      digitalWrite(led3, LOW);
    }
  }
}

---

int led1 = 8;
int led2 = 9;
int led3 = 10;

void setup() {
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);

  Serial.begin(9600);  // Inicia o monitor serial
}

void loop() {
  if (Serial.available() > 0) {
    char comando = Serial.read();

    if (comando == 'K') {
      // Liga todos os LEDs
      digitalWrite(led1, HIGH);
      digitalWrite(led2, HIGH);
      digitalWrite(led3, HIGH);
    } 
    else if (comando == 'D') {
      // Desliga todos os LEDs
      digitalWrite(led1, LOW);
      digitalWrite(led2, LOW);
      digitalWrite(led3, LOW);
    } 
    else if (comando == 'P') {
      // Pisca os LEDs por 10 segundos
      unsigned long tempoInicial = millis();
      while (millis() - tempoInicial < 10000) {  // 10 segundos = 10000 milissegundos
        digitalWrite(led1, HIGH);
        digitalWrite(led2, HIGH);
        digitalWrite(led3, HIGH);
        delay(500);
        digitalWrite(led1, LOW);
        digitalWrite(led2, LOW);
        digitalWrite(led3, LOW);
        delay(500);
      }
    }
  }
}

---

int led1 = 8;
int led2 = 9;
int led3 = 10;  

void setup() {
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
}

void loop() {
  digitalWrite(led1, HIGH);
  delay(500);
    digitalWrite(led2, HIGH);
    delay(500);
    digitalWrite(led3, HIGH);

    delay(1000);  
  }

---

int led1 = 8;
int led2 = 9;
int led3 = 10;  

void setup() {
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
}

void loop() {
  digitalWrite(led1, HIGH);
  delay(500);
    digitalWrite(led2, HIGH);
    delay(500);
    digitalWrite(led3, HIGH);
delay(500);
digitalWrite(led1, LOW);
  delay(500);
    digitalWrite(led2, LOW);
    delay(500);
    digitalWrite(led3, LOW);

    delay(1000);  
  }

---

int led1 = 8;
int led2 = 9;
int led3 = 10;  

void setup() {
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
}

void loop() {
  digitalWrite(led1, HIGH);
  delay(500);
    digitalWrite(led2, HIGH);
    delay(500);
    digitalWrite(led3, HIGH);
delay(500);
digitalWrite(led3, LOW);
  delay(500);
    digitalWrite(led2, LOW);
    delay(500);
    digitalWrite(led1, LOW);

    delay(1000);  
  }


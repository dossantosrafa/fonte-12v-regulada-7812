# fonte-12v-regulada-7812
# Fonte Regulada 12V com Regulador 7812

## 1. Introdução

Este projeto consiste no desenvolvimento de uma **fonte de alimentação regulada de 12V**, utilizando o regulador linear **7812**. O circuito foi projetado utilizando o software **Proteus**, incluindo:

* Esquemático do circuito
* Layout da placa PCB
* Visualização 3D da placa

A fonte recebe tensão **AC proveniente do secundário de um transformador**, realiza a **retificação da tensão**, filtra o sinal e fornece uma **saída estabilizada de 12V DC**.

---

# 2. Objetivo do Projeto

O objetivo deste projeto é demonstrar o funcionamento de uma **fonte linear regulada**, muito utilizada em circuitos eletrônicos para alimentar dispositivos que necessitam de tensão contínua estável.

O circuito realiza as seguintes etapas:

1. Entrada de tensão AC
2. Retificação da tensão
3. Filtragem do sinal
4. Regulação da tensão
5. Indicação de funcionamento através de LED

---

# 3. Esquemático do Circuito

![Esquemático](esquematico.png)

O esquemático apresenta todos os componentes e conexões responsáveis pelo funcionamento da fonte.

---

# 4. Componentes Utilizados

| Componente | Descrição                            |
| ---------- | ------------------------------------ |
| J2         | Conector de entrada do transformador |
| BR1        | Ponte retificadora                   |
| C1         | Capacitor eletrolítico 1000µF        |
| C2         | Capacitor cerâmico 100nF             |
| U1         | Regulador de tensão 7812             |
| C3         | Capacitor cerâmico 100nF             |
| R1         | Resistor 100Ω                        |
| D1         | LED indicador                        |
| J1         | Conector de saída                    |

---

# 5. Funcionamento do Circuito

## 5.1 Entrada de Tensão

A entrada do circuito ocorre através do conector **J2**, onde é conectada a saída do **secundário de um transformador**.

O transformador reduz a tensão da rede elétrica para um valor seguro (por exemplo 12V AC).

---

## 5.2 Retificação da Tensão

A tensão AC proveniente do transformador é aplicada à **ponte retificadora BR1**.

A ponte retificadora é composta por quatro diodos e tem a função de converter a tensão **AC (corrente alternada)** em **DC pulsante (corrente contínua)**.

Após essa etapa, a tensão já possui polaridade positiva e negativa definidas.

---

## 5.3 Filtragem da Tensão

Após a retificação, a tensão ainda apresenta **ondulações (ripple)**.

Para reduzir essas variações é utilizado o capacitor:

**C1 – 1000µF**

Esse capacitor funciona como um **filtro**, armazenando energia e suavizando a tensão, tornando-a mais próxima de uma tensão contínua.

O capacitor **C2 (100nF)** também atua como **desacoplamento**, reduzindo ruídos de alta frequência.

---

## 5.4 Regulação de Tensão

A tensão filtrada é aplicada ao **regulador de tensão 7812 (U1)**.

O regulador 7812 possui três pinos:

| Pino | Função            |
| ---- | ----------------- |
| 1    | Entrada de tensão |
| 2    | Terra (GND)       |
| 3    | Saída regulada    |

Este componente mantém a saída **estável em 12V**, mesmo que ocorram pequenas variações na tensão de entrada.

O capacitor **C3 (100nF)** melhora a estabilidade da saída do regulador.

---

## 5.5 LED Indicador

O LED **D1** funciona como um **indicador visual de funcionamento**.

Quando a fonte está energizada, a corrente passa pelo resistor **R1 (100Ω)** e pelo LED, fazendo com que ele acenda.

O resistor limita a corrente para evitar que o LED seja danificado.

---

## 5.6 Saída da Fonte

A saída da fonte ocorre através do conector **J1**, onde temos:

* Pino 1 → +12V regulado
* Pino 2 → GND

Essa saída pode ser utilizada para alimentar diversos circuitos eletrônicos.

---

# 6. Layout da PCB

![PCB](pcb.png)

A placa foi projetada com dimensões:

**80mm x 40mm (8cm x 4cm)**

O layout foi organizado para facilitar a montagem e reduzir o comprimento das trilhas.

---

# 7. Visualização 3D da Placa

Vista superior:

![3D](3Dupview.png)

Vista inferior:

![3D Inferior](3Ddownview.png)

A visualização 3D permite observar a disposição real dos componentes na placa.

---

# 8. Etapas de Funcionamento da Fonte

O funcionamento completo ocorre na seguinte sequência:

1️⃣ Transformador reduz tensão da rede elétrica
2️⃣ Ponte retificadora converte AC em DC
3️⃣ Capacitor filtra a tensão
4️⃣ Regulador 7812 estabiliza em 12V
5️⃣ LED indica funcionamento
6️⃣ Tensão regulada é disponibilizada na saída

---

# 9. Aplicações

Fontes reguladas como esta podem ser utilizadas em:

* Projetos com Arduino
* Circuitos eletrônicos
* Protótipos de robótica
* Sistemas embarcados
* Alimentação de sensores

---

# 10. Software Utilizado

O projeto foi desenvolvido utilizando:

**Proteus Design Suite**

Ferramentas utilizadas:

* ISIS → Esquemático
* ARES → Layout PCB
* 3D Viewer → Visualização da placa

---

# 11. Autor

Projeto desenvolvido para atividade acadêmica de Sistemas Embarcados.

Autor: Rafael Fontana

###### **Aula 03 - 25.03**
**Próxima aula:** [[Conceitos Básicos de Sistemas]] (Aula 04 - 27.03) 

---
#  Industria Automotiva
- Formada por um conglomerado de empresas 
- Podem incluir:
	- Original Equipment Manufacturer (OEM)
	- Fornecedores (Supplies)
	- Concessionários (after-sales)

# Sistemas Automotivos

## Gerenciamento do Motor
1. ECU controla a quantidade de combustível no motor (**injeção de combustível**) em função do período
	1. Caso tenha mais combustível, o combustível não queimado cai no catalizador
	2. Caso tenha mais O2 na queima, gera gases tóxicos
2. Ao pistão descer e realizar a aspiração do ar (pressão abaixa) a ECU realiza a ignição 
3. Pistão sobre aumentando a pressão e então os gases gerados são expelidos
4. Catalizador captura esses gases expelidos (passados pelo cano?)

No fim boa parte do controle e do bom funcionamento do motor depende de vários sensores e comunicação com a ECU do motor (única).

## Gerenciamento de Frenagem (**ABS**)
1. De acordo com os sinais enviados pelos sensores envia comandos para o *controlador modular hidráulico*
2. Realiza a frenagem, controlando as rodas, para evitar o travamento completo de cada uma
	1. Essa frenagem ocorre de maneira extremamente rápida

## Componentes Eletroeletrônicos
Promovem o devido funcionamento do veículo. Podem ser dos tipos:
- Sensores Automotivos
	- **Transdutores de entrada de um sistema**
	- Converte grandeza física em sinal elétrico
	- Fornece informações sobre o meio para a ECU
	- Sofre influências externas
- Atuadores Automotivos
	- **Transdutores de saída de um sistema**
	- Converte sinal elétrico para grandeza física
	- Acionado e controlado por ECU's
	- Modificam o estado do sistema controlado
- ECU's
	- **Controla o funcionamento do veículo**
	- Obtém informações de estados e sensores, processa essas informações
	- Envia sinais para os atuadores
- Componentes Auxiliares

# Arquitetura Eletroeletrônica 

## Arquitetura Centralizada
- Utilização de uma **única** *ECU*
- Essa unidade de controle concentra **todo o fluxo de informações**
- Envia comando para diversos atuadores

|             **Vantagens**             |                   **Desvantages**                    |
| :-----------------------------------: | :--------------------------------------------------: |
| Estratégias de controle simplificadas |        Dificuldade para estratégias complexas        |
|          Custo **reduzido**           |   Demanda modificações a cada nova funcionalidade    |
|                                       | Processo de expansão de funcionalidades dificultados |

## Arquitetura Distribuída


---
# Glossário
- **ECU:** Engine Control Unit
- **CAN:** Controller Area Network
- **MAP:** (Sensor) 
- **MAF:** Mass Air Flow (Sensor)
- **SI:** Spark Ignition
- **Wall Wetting:** Forma um filme de combustível, na entrada de combustível no motor, para tornar a mistura mais rica para facilitar a queima
- **Catalisador:** serve para tornar os gases que saem pelo sistema de escapamento derivados da queima de combustível menos nocivos ao meio ambiente.
-  **ACC:** Autonomous cruise control
- **EPS:** Electric Power Steering
 
# Curiosidades
- Gasolina do Brasil está em E_27, relação de etanol com a gasolina pura
- Estequiométrico, quer dizer quando a queima está quimicamente correta, ou seja, gera uma queima completa e balanceada em O2 e Combustível.
 ---
**tags:** #ECU #CAN #LIN #OEM #MAF #SI #ACC #EPS
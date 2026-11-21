# Placa C0_MINI

A **C0_MINI** é uma placa de desenvolvimento ultracompacta desenvolvida pela [**IoTmatic.com.br**](https://iotmatic.com.br), baseada no microcontrolador **STM32C011F6P6** da STMicroelectronics. 

![C0_MINI 3D View](3D_View.png)

---

## ⚙️ Especificações Principais

* **Microcontrolador:** STM32C011F6P6 (ARM® Cortex®-M0+ até $48\text{ MHz}$, $32\text{ KB}$ Flash, $6\text{ KB}$ SRAM)
* **Fabricante da Placa:** [IoTmatic.com.br](https://iotmatic.com.br)
* **Interface de Programação/Debug:** Conector dedicado ST-Link (`+`, `C`, `-`, `D`, `R`)

---

## 🕒 Configuração de Clock

* **Fonte de Clock:** Oscilador interno HSI48 ($48\text{ MHz}$)
* **Prescaler de Sistema:** $/4$
* **Frequência do Core (SYSCLK):** $12\text{ MHz}$

---

## 📌 Mapeamento de Pinos e Periféricos

### **LED de Usuário**
* **LED Onboard:** Conectado ao pino **`PA4`**

### **Ajustes de Remapeamento de Pinos (Pinout)**
Devido às características de multiplexação do encapsulamento TSSOP-20 do STM32C011, o firmware de validação foi ajustado para expor as seguintes funções de comunicação:

| Pino Físico / Função Original | Ajuste / Mapeamento de Hardware | Periférico Utilizado |
| :---: | :---: | :--- |
| **`PA11`** | **`PA9`** | **USART1** (`TX`/`RX`) ajustada  |
| **`PA12`** | **`PA10`** | para `PA9` e `PA10` |

### **Firmware de validação da PCB **
Todas as placas são entregues montadas, com firmware de validação gravado e testadas.
Ao alimentar a placa, os I/Os alternarão entre HIGH e LOW na disposição da PCB:
	B7 -> C14 -> C15 -> A0 -> A1 -> A2 -> A5 -> A6 -> A8 -> A9 -> A10 -> B6 -> A7, repete o ciclo
Para cada I/O na sequência o LEDONBOARD piscará junto.
O pino de I/O PA3 esta configurado para entrada com pull-up. 
Colocando uma tecla, estiver pressionada pisca mais rapidamente.


---

## 🖼️ Galeria de Placas (Top & Bottom)

| Vista Superior (Top PCB) | Vista Inferior (Bottom PCB) |
| :---: | :---: |
| ![TOP C0_MINI](TOP_C0_MINI.jpeg) | ![BOTTOM C0_MINI](BOTTOM_C0_MINI.jpeg) |

---

## 📄 Licença e Suporte

Projeto desenvolvido por **IoTmatic.com.br**. Sinta-se à vontade para utilizar e adaptar o firmware para suas aplicações embarcadas.

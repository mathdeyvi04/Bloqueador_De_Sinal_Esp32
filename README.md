> # Referência
> Todo o estudo aplicado neste repositório foi desenvolvido a partir 
> de outro trabalho de alto nível, [autor_inicial](https://github.com/smoochiee/Bluetooth-jammer-esp32/tree/main)

# Itens Necessários

- 1 ESP32
`imagem da esp` 

- 2 Capacitores Eletrolíticos (25 V)
`imagem do capacitor`

- 2 módulos RF24 Serial SPI
`imagem dos módulos`

# Como Conectá-los

- Capacitores aos módulos de RF24
`imagem demonstrativa`

- Protótipo v0
`imagem dos sanhas`

# Explicação do Código

### Por que HSPI e VSPI?

Observe que a esp32 possui 2 colunas de pinos, oq possibilitará para nós o uso de até
2 antenas.

`imagem da esp32 apresentando os pinos`

Os pinos do lado direito são denominados VSPI, enquanto os da esquerda HSPI.
Ambos são controladores SPI completamente funcionais e independentes no ESP32,
podendo ser usados para comunicação. O padrão de pinos demonstrado na imagem é 
a convenção geral e já implementada no código.

VSPI --- Variable SPI 

HSPI --- Hardware SPI

Os arquivos [FOR_HSPI_PIN.ino](src/FOR_HSPI_PIN.ino) servem apenas os pinos correspondentes. Da mesma 
forma temos [FOR_VSPI_PIN.ino](src/FOR_VSPI_PIN.ino), enquanto [FOR_DUAS_PINS.ino](src/FOR_DUAL_PINS.ino) usamos
para quando há duas antenas, que é nosso caso.

### Uso da Biblioteca RF24

Amplamente utilizada para configurar e utilizar antenas padrões de 2.4GHz.
Bem complexa e exige um alto nível de conhecimento, [RF24](https://github.com/nRF24/RF24).











## Atividade 01

### Laboratório 02

Neste laboratório utilizamos a ferramenta GNU Arm Embedded Toolchain visando a compilação de códigos para a linha de microcontoladores da ST, mais expecificamente da linha STM32F411.

Aprendemos automatizar a compilação de scripts, utilizando a ferramenta Makefile e programar toda a parte de inicialização do chip STM32F411 em linguagem C, gravar o stack pointer no inicio da memória flash e demais configurações na região da memória RAM.

### Laboratório 03

Neste laboratótio temos o propósito de implementar um código para piscar o LED integrado ao kit de desenvolvimento STM32F411, porém, continuaremos desenvolvendo o código feito no laboratório_02.

Determinanmos o pino, cujo o LED está conectado. Como vamos utilizar a porta C, é necessário habilitar o clock desta porta. Isto é feito através do periférico Reset tiand Clock Control (RCC), foi visto que na STM32F401 e 411 o pino de ativação de clock possuí um offset de 0X30 com endereço 0x4002 3800.

Configuramos o pino PC13 como saída em push-pull com os resistores de pull-up e pull-down desligados por meio dos registradores do periférico GPIOC.

Analisamos as seções do arquivo objeto sendo: .text, .data, .bss, .comment e .ARM.attributes. 

Escrevemos o arquivo linker, que é o responsável por combinar os arquivos objeto em um único arquivo executável para ser utilizado em nosso kit de desenvolvimento STM32F401.
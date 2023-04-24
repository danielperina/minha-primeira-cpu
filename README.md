# Minha Primeira CPU 

Este é um projeto de uma CPU criado no Logisim com o objetivo de aprender mais sobre arquitetura de computadores e lógica digital.

## Formato das Instruções
As instruções seguem os seguintes formatos:

- OOOOOO AAAAAAAAAA
- OOOOOO XXXXXXXXXR

Onde:

**O** representa o opcode da instrução.<br>
**A** representa o endereço de memória utilizado pela instrução.<br>
**X** representa um bit que não é utilizado pela instrução.<br>
**R** representa o endereço de um registrador utilizado pela instrução.<br>

## Instruções suportadas

As instruções suportadas por esta CPU são as seguintes:

```
00 - NOP - 000000 XXXXXXXXXX - WX

01 - STA - 000001 AAAAAAAAAA - WDM
02 - STB - 000010 AAAAAAAAAA - WDM

03 - LDA - 000011 AAAAAAAAAA - WDR
04 - LDB - 000100 AAAAAAAAAA - WDR
05 - LAI - 000101 IIIIIIIIII - WDR
06 - LBI - 000110 IIIIIIIIII - WDR

07 - TBA - 000111 XXXXXXXXXX - WDR
08 - TAB - 001000 XXXXXXXXXX - WDR

09 - ADD - 001001 XXXXXXXXXR - WDR
0A - ADA - 001010 AAAAAAAAAA - WDR
0B - ADB - 001011 AAAAAAAAAA - WDR

0C - SUB - 001100 XXXXXXXXXR - WDR
0D - SBA - 001101 AAAAAAAAAA - WDR
0E - SBB - 001110 AAAAAAAAAA - WDR

0F - AND - 001111 XXXXXXXXXR - WDR
10 - ANA - 010000 AAAAAAAAAA - WDR
11 - ANB - 010001 AAAAAAAAAA - WDR

12 - ORI - 010010 XXXXXXXXXR - WDR
13 - ORA - 010011 AAAAAAAAAA - WDR
14 - ORB - 010100 AAAAAAAAAA - WDR

15 - EOR - 010101 XXXXXXXXXR - WDR
16 - EOA - 010110 AAAAAAAAAA - WDR
17 - EOB - 010111 AAAAAAAAAA - WDR

18 - JMP - 011000 AAAAAAAAAA - WIP
19 - JPS - 011001 AAAAAAAAAA - WIP
1A - JPZ - 011010 AAAAAAAAAA - WIP

3F - HLT - 111111 XXXXXXXXXX - WX

X - DONT CARE
A - MEMORY ADDRESS
R - REGISTER ADDRESS
I - IMMEDIEATE VALUE

WDM - WRITE DATA MEMORY
WDR - WRITE DATA REGISTER 
WIP - WRITE INTRUCTION POINTER/PROGRAM COUNTER
WX - DO NOT WRITE DATA
```

## Descrição das instruções

- **NOP**: Não faz nada.
- **STA**: Armazena o conteúdo do registrador **A** em um endereço de memória especificado.
- **STB**: Armazena o conteúdo do registrador **B** em um endereço de memória especificado.
- **LDA**: Carrega o conteúdo de um endereço de memória especificado para o registrador **A**.
- **LDB**: Carrega o conteúdo de um endereço de memória especificado para o registrador **B**.
- **LAI**: Carrega o valor imediato 10 bits com sinal no registrador **A**.
- **LBI**: Carrega o valor imediato 10 bits com sinal no registrador **B**.
- **TBA**: Carrega no registrador **A** o valor que está no registrador **B**.
- **TAB**: Carrega no registrador **B** o valor que está no registrador **A**.
- **ADD**: Soma o conteúdo dos registradores **A** e **B** e armazena o resultado no registrador especificado.
- **ADA**: Soma o conteúdo do registrador **A** com um valor da memória e armazena o resultado no registrador **A**.
- **ADB**: Soma o conteúdo do registrador **B** com um valor da memória e armazena o resultado no registrador **B**.
- **SUB**: Subtrai o conteúdo do registrador **B** do conteúdo do registrador **A** e armazena o resultado no registrador especificado.
- **SBA**: Subtrai um valor da memória do conteúdo do registrador **A** e armazena o resultado no registrador **A**.
- **SBB**: Subtrai um valor da memória do conteúdo do registrador **B** e armazena o resultado no registrador **B**.
- **AND**: Realiza uma operação AND bit a bit entre os conteúdos dos registradores **A** e **B** e armazena o resultado no registrador especificado.
- **ANA**: Realiza uma operação AND bit a bit entre o conteúdo do registrador **A** e um valor da memória e armazena o resultado no registrador **A**.
- **ANB**: Realiza uma operação AND bit a bit entre o conteúdo do registrador **B** e um valor da memória e armazena o resultado no registrador **B**.
- **ORI**: Realiza uma operação OR bit a bit entre os conteúdos dos registradores **A** e **B** e armazena o resultado no registrador especificado.
- **ORA**: Realiza uma operação OR bit a bit entre o conteúdo do registrador **A** e um valor da memória e armazena o resultado no registrador **A**.
- **ORB**: Realiza uma operação OR bit a bit entre o conteúdo do registrador **B** e um valor da memória e armazena o resultado no registrador **B**.
- **EOR**: Realiza uma operação XOR bit a bit entre os conteúdos dos registradores **A** e **B** e armazena o resultado no registrador especificado.
- **EOA**: Realiza uma operação XOR bit a bit entre o conteúdo do registrador **A** e um valor da memória e armazena o resultado no registrador **A**.
- **EOB**: Realiza uma operação XOR bit a bit entre o conteúdo do registrador **B** e um valor da memória e armazena o resultado no registrador **B**.
- **JMP**: Altera o valor do **PC** (program counter) para o endereço especificado.
- **JPS**: Altera o valor do **PC** para o endereço especificado somente se a flag **S** (Signal) for 1.
- **JPZ**: Altera o valor do **PC** para o endereço especificado somente se a flag **Z** for 1.
- **HLT**: Para a execução do programa.

*Observação: mais instruções podem ser inseridas futuramente.

## Uso
Para usar este projeto, baixe o arquivo **.circ** e abra-o no "Logisim Evolution". Você pode então visualizar o circuito e executá-lo para testar seu funcionamento.

## Contribuição
Este é um projeto de aprendizado pessoal, mas estou aberto a sugestões de melhoria e correções. Se você tiver alguma ideia ou encontrar algum problema, sinta-se à vontade para abrir uma issue ou um pull request. Agradeço antecipadamente por sua ajuda em tornar este projeto melhor!

## Licença
Este projeto é licenciado sob a licença MIT. Consulte o arquivo **LICENSE** para obter mais informações.

## Créditos
Este projeto foi criado por Daniel Inácio. Agradeço à comunidade do Logisim pela a utilidade seus recursos durante o desenvolvimento deste projeto.

# Minha Primeira CPU 

Este é um projeto de uma CPU criado no Logisim com o objetivo de aprender mais sobre arquitetura de computadores e lógica digital.

## Formato das Instruções
As instruções seguem um dos seguintes formatos:

- OOOOOO AAAAAAAAAA
- OOOOOO XXXXXXXXXR

Onde:

**O** representa o opcode da instrução.
**A** representa o endereço de memória utilizado pela instrução.
**X** representa um bit que não é utilizado pela instrução.
**R** representa o endereço de um registrador utilizado pela instrução.

## Instruções suportadas

As instruções suportadas por esta CPU são as seguintes:

```
00 - NOP - 000000 XXXXXXXXXX - WX

01 - STA - 000001 AAAAAAAAAA - WDM
02 - STB - 000010 AAAAAAAAAA - WDM

03 - LDA - 000011 AAAAAAAAAA - WDR
04 - LDB - 000100 AAAAAAAAAA - WDR

05 - ADD - 000101 XXXXXXXXXR - WDR
06 - ADA - 000110 AAAAAAAAAA - WDR
07 - ADB - 000111 AAAAAAAAAA - WDR

08 - SUB - 001000 XXXXXXXXXR - WDR
09 - SBA - 001001 AAAAAAAAAA - WDR
0A - SBB - 001010 AAAAAAAAAA - WDR

0B - AND - 001011 XXXXXXXXXR - WDR
0C - ANA - 001100 AAAAAAAAAA - WDR
0D - ANB - 001101 AAAAAAAAAA - WDR

0E - ORI - 001110 XXXXXXXXXR - WDR
0F - ORA - 001111 AAAAAAAAAA - WDR
10 - ORB - 010000 AAAAAAAAAA - WDR

11 - EOR - 010001 XXXXXXXXXR - WDR
12 - EOA - 010010 AAAAAAAAAA - WDR
13 - EOB - 010011 AAAAAAAAAA - WDR

14 - JMP - 010100 AAAAAAAAAA - WIP
15 - JPS - 010101 AAAAAAAAAA - WIP
16 - JPZ - 010110 AAAAAAAAAA - WIP

3F - HLT - 111111 XXXXXXXXXX - WX

X - DONT CARE
A - MEMORY ADDRESS
R - REGISTER ADDRESS

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
LDB: Carrega o conteúdo de um endereço de memória especificado para o registrador **B**.
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
- **ORA**: Realiza uma operação OR bit a bit entre o conteúdo do registrador **A** e um valor da memória e armazena o resultado no registrador A.
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
Para usar este projeto, baixe o arquivo **.circ** e abra-o no Logisim. Você pode então visualizar o circuito e executá-lo para testar seu funcionamento.

## Contribuição
Este é um projeto de aprendizado pessoal, mas estou aberto a sugestões de melhoria e correções. Se você tiver alguma ideia ou encontrar algum problema, sinta-se à vontade para abrir uma issue ou um pull request. Agradeço antecipadamente por sua ajuda em tornar este projeto melhor!

## Licença
Este projeto é licenciado sob a licença MIT. Consulte o arquivo **LICENSE** para obter mais informações.

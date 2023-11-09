# Arquitetura de Computadores - Ficha 1

## Informação do aluno

    Nome: Frederico Bacar

Escreve as respostas dentro dos blocos correspondentes.
Substitui as reticências pelo que é pedido em cada pergunta.
Não desformates o documento.

### P1. Identifica e descreve os principais componentes de um processador. Fornece uma breve explicação da função de cada componente

- Lista os componentes principais de um processador.
- Para cada componente, descreve o seu papel e função no processador.
- Considera componentes como unidade lógica aritmética (ALU), unidade de controlo (UC), registos internos, memória e interfaces de entrada/saída (I/O).

P1 - Resposta:

    # Os principais componentes de um procesãdor são:
    
    - Unidade de controle: A unidade de controle gerencia o processamento de instruções e coordena o fluxo de dados dentro da CPU e entre outros componentes do computador. Ela tem      um componente decodificador de instruções que interpreta as instruções obtidas da memória e as converte em micro-operações que a CPU pode executar. A unidade de controle            direciona outros componentes da CPU para executar as operações necessárias.
    
    - Registradores: Os registradores são pequenos locais de armazenamento de memória de alta velocidade dentro da CPU. Eles mantêm os dados nos quais a CPU está trabalhando no         momento e facilitam o acesso rápido aos dados. As CPUs têm vários tipos de registradores, como estes:
        - Registradores de uso geral que armazenam dados operacionais.
        - Registradores de instrução que armazenam a instrução que está sendo processada no momento.
        -Um contador de programa que contém o endereço de memória da próxima instrução a ser buscada.
    - Um contador de programa que contém o endereço de memória da próxima instrução a ser buscada.

    - ULA: A unidade lógica aritmética (ULA) realiza operações aritméticas básicas (adição, subtração, multiplicação e divisão) e operações lógicas (AND, OR e NOT) nos dados. Ela       recebe dados de registradores dentro da CPU, processa-os com base nas instruções da unidade de controle e produz o resultado.

    Memória RAM: A memória de acesso randômico (pt-BR) ou de acesso aleatório(pt-PT?) (do inglês Random Access Memory, frequentemente abreviado para RAM), também chamado de memória     volátil de leitura e escrita, é uma memória temporária computacional de acesso rápido; ou seja, é um local de armazenamento temporário de informações digitais usada pelo            processador para armazenar informações temporariamente e que possui um acesso feito de forma aleatória mais rápido que ao HD, DVD, pendrive (permite a rápida leitura e escrita      de informações), utilizada como memória primária em sistemas eletrónicos digitais.

    Memória Cache: Na área da computação, cache é um dispositivo de acesso rápido, interno a um sistema, que serve de intermediário entre um operador de um processo e o dispositivo     de armazenamento ao qual esse operador acede. A principal vantagem na utilização de um cache consiste em evitar o acesso ao dispositivo de armazenamento, que pode ser demorado      , armazenando os dados em meios de acesso mais rápidos.

    - O uso de memórias cache visa obter uma velocidade de acesso a memória próxima da velocidade de memórias mais rápidas, e ao mesmo tempo disponibilizar no sistema uma memória       de grande capacidade, a um custo similar de memórias de semicondutores mais baratas.
    
 


### P2. Compara as arquiteturas de Von Neumann e Harvard em termos de características e principais diferenças

- Lista as principais características da arquitetura Von Neumann.
- Lista as principais características da arquitetura de Harvard.
- Explica as principais diferenças entre as duas arquiteturas, particularmente na organização da memória, busca de instruções e separação de dados.
- Fornece exemplos de sistemas de computação que usam cada arquitetura.

P2 - Resposta:

    A Arquitetura de computador de von Neumann se caracteriza pela possibilidade de uma máquina digital armazenar seus programas no mesmo espaço de memória que os dados,
    podendo assim manipular tais programas. Esta arquitetura é um projeto modelo de um computador digital de programa armazenado que utiliza uma unidade de processamento (CPU) e
    uma de armazenamento ("memória") para comportar, respectivamente, instruções e dados.
    
    A Arquitetura de computador de Harvard é uma arquitetura de computador que se distingue das outras por possuir duas memórias diferentes e independentes em termos de barramento      e ligação ao processador. É utilizada nos microcontroladores PIC. Tem, como principal característica, o acesso à memória de dados de modo separado em relação à memória de           programa.

    Von Neumann é uma arquitetura de computador digital cujo design é baseado no conceito de computadores de programa armazenados, onde os dados do programa e os dados de instrução     são armazenados na mesma memória. Esta arquitetura foi projetada pelo famoso matemático e físico John Von Neumann em 1945 enquanto Harvard é a arquitetura de computador digital     cujo design é baseado no conceito de armazenamento separado e barramentos separados (caminho de sinal) para instrução e dados.

    Sistemas de computação de Von Neumann: CISC (Complex Instruction Set Computer).
    Sistemas de computação Harvard: RISC (Reduced Instruction Set Computer).


### P3. Descreve o ciclo *fetch-decode-execute* num processador, detalhando cada etapa e explicando a sua importância na execução de programas de computador

- Fornece uma explicação detalhada da fase de busca de instrução, incluindo o que ela envolve e por que é importante na operação do processador.
- Explica a fase de descodificação e o seu papel na interpretação das instruções de execução.
- Descreve a fase de execução, destacando a execução propriamente dita das instruções e quaisquer interações com dados.
- Conclui explicando a ordem destas fases e como elas garantem a execução adequada dos programas de computador.
- Usa um diagrama para ilustrar o ciclo.

P3 - Resposta:

    Um ciclo de instrução (também chamado de ciclo de busca e execução ou ciclo busca-execução (fetch-decode-execute) é o período de tempo no qual um computador lê e processa uma instrução em linguagem de máquina da sua memória ou a sequência de ações que a CPU realiza para executar cada instrução em código de máquina num programa.
    A expressão "ciclo de busca e execução" também é muito usada, pois descreve em essência o modo como um computador funciona: a instrução deve ser buscada na memória principal e      depois executada pela CPU. Deste ciclo emergem todas as funções do computador que são familiares para o usuário final.

    # O CPU (processador) realiza repetidamente o seguinte ciclo chamado ``fetch-decode-execute'':

    1. Busca a instrução (apontada por PC) da memória e carrega-a no IR.
    2. Muda o PC para apontar para a próxima instrução da memória.
    3. Decodifica a instrução, determinando o seu tipo, operandos, etc.
    4. Se a instrução usa operandos (dados) da memória, determina os seus endereços.
    5. Busca os dados de memória e carrega-os nos registradores.
    6. Executa a instrução.
    7. Armazena resultados (em registradores ou memória).

![Diagrama](https://o.quizlet.com/cBYTeCQFphn6lW-wdg5v.Q.png)

    
    

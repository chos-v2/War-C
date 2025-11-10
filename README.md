# War-C
desenvolvendo o jogo War em C

Commit Inicial: Cadastro Estático de Territórios (Nível Novato)
O que foi feito: Criado o sistema básico para cadastrar territórios.

Dados e Estrutura:

Definida a struct Territorio (nome, cor, tropas).

Utilizado um vetor estático (mapa[5]) para guardar 5 territórios.

Usados loops for e funções simples para leitura e exibição dos dados.

2. Commit Secundário: Implementação de Ataque Dinâmico e Modularização
O que foi feito: Adicionada a funcionalidade de simulação de ataque e o código ficou mais flexível.

Dados e Estrutura:

Alocação Dinâmica: O mapa agora é criado com malloc, permitindo que o usuário decida quantos territórios o jogo terá.

Ponteiros: O acesso e a manipulação dos dados dos territórios (tropas, cor, etc.) são feitos inteiramente por ponteiros (->).

Modularização: O código foi dividido em funções específicas para cada tarefa: cadastrarTerritorios, exibirTerritorios, atacar e liberarMemoria.

Simulação: Adicionada a função atacar que usa números aleatórios (rand) para simular a rolagem de dados e atualiza as tropas e o dono do território defensor em caso de vitória.

Gerenciamento de Memória: Incluída a chamada obrigatória para free para liberar a memória alocada dinamicamente.

Este commit integra os jogadores ao sistema, fornecendo missões sorteadas para definir seus objetivos de vitória, movendo o projeto de uma simulação tática para uma simulação estratégica.

Funcionalidade Principal
Implementação de Missões: Cada jogador recebe uma missão secreta sorteada no início do jogo. O cumprimento da missão leva à vitória imediata.

Gestão de Jogadores: Introdução de uma struct Jogador (cor e missão) para armazenar os dados dos participantes.

Verificação de Vitória: O jogo verifica automaticamente, após cada ataque, se a missão de algum jogador foi cumprida.

Conceitos e Estruturas Implementados
Vetor de Strings para Missões: Criado um vetor estático (char* MISSOES[]) contendo as descrições de objetivos.

Alocação Dinâmica para Missões: A string da missão de cada jogador é alocada dinamicamente (malloc) e gerenciada por ponteiros (char* missao).

Modularização Específica: Criação de funções dedicadas:

atribuirMissao(): Sorteia uma missão (rand) e usa strcpy para copiar a string alocada para o jogador.

verificarMissao(): Contém a lógica de checagem, que avalia a situação atual do mapa e o objetivo da missão.

Passagem de Parâmetros: Demonstra o uso correto de ponteiros para ponteiros (Jogador** jogadores_ptr_ref) na função de cadastro para garantir que o ponteiro alocado seja retornado e persistido no main().

Gerenciamento de Memória: A função liberarMemoria() foi atualizada para liberar corretamente tanto o vetor de territórios quanto as strings de missão alocadas individualmente para cada jogador.

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

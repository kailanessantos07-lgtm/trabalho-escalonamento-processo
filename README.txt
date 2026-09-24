Guia de Execução do Simulador de Escalonamento

    Antes de executar, verifique no arquivo a quantidade de processos desejada, encontrado na variável: 'n_processos', 
que possui o valor padrão de '3'.

    Ao executar o arquivo 'base.py', será feita a seguinte pergunta: "Será aleatório? ", espera-se um retorno em número, 
'1' para que todos os processos sejam aleatórios ou qualquer outro número para especificar os parâmetros de cada processo.
    A seguir serão criados os 'n' processos que serão utilizados no sistema, que serão retornados pelo terminal para a visualização dos valores.
    Com os processos criados o usuário será direcionado para o menu, onde poderá escolher qual critério de escalonamento utilizar com os processos.

    Ao selecionar o critério a ser utilizado, ele será executado imediatamente e irá retornar pelo terminal:
Uma linha do tempo da execução (Unidade de tempo atual, qual processo foi executado e quanto tempo resta para terminar), 
junto com o tempo de espera de cada processo, e a média do tempo de espera total.
    Terminando a execução do critério o usuário é retornado ao menu de seleção de critérios onde pode executar outro critério ou sair do sistema.

Implementação do SJF

O algoritmo SJF (Shortest Job First) foi implementado nas versões
Preemptiva e Não-Preemptiva.

No SJF Não-Preemptivo, o sistema verifica os processos que já chegaram
e escolhe o processo com menor tempo de execução. Após ser escolhido,
o processo executa até terminar, sem ser interrompido.

No SJF Preemptivo, o sistema verifica os processos disponíveis a cada
unidade de tempo e escolhe aquele que possui o menor tempo restante.
Caso um processo com menor tempo restante esteja disponível, ele pode
assumir a execução da CPU.

Para os dois critérios, são considerados os tempos de chegada dos
processos. Durante a execução, o sistema apresenta no terminal o tempo
atual, o processo executado e o seu tempo restante.

Ao finalizar, o sistema apresenta o tempo de espera de cada processo
e a média do tempo de espera.

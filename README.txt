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

PRIORIDADE PREEMPTIVA
O algoritmo verifica os processos disponíveis a cada unidade de tempo e seleciona aquele com maior prioridade. Nesta implementação, o menor número representa a maior prioridade. Se surgir um processo com prioridade maior, o processo atual pode ser interrompido.

PRIORIDADE NÃO-PREEMPTIVA
O algoritmo seleciona, entre os processos que já chegaram e ainda não terminaram, aquele com maior prioridade. Nesta implementação, o menor número representa a maior prioridade. Depois de selecionado, o processo executa até terminar.

ROUND-ROBIN
O algoritmo organiza os processos em uma fila e utiliza um quantum informado pelo usuário. Cada processo pode executar por até esse número de unidades de tempo. Se terminar, sai da fila; caso contrário, volta para o final da fila para aguardar outra oportunidade de execução.
PRIORIDADE PREEMPTIVA
O algoritmo verifica os processos disponíveis a cada unidade de tempo e seleciona aquele com maior prioridade. Nesta implementação, o menor número representa a maior prioridade. Se surgir um processo com prioridade maior, o processo atual pode ser interrompido.

RESULTADOS
Durante a execução, o programa apresenta o histórico de execução, indicando o tempo, o processo escolhido e o tempo restante. Ao final, apresenta o tempo de espera de cada processo e o tempo médio de espera.

OBSERVAÇÕES IMPORTANTES
- Para Round-Robin, esta versão considera que todos os processos chegam no tempo zero, pois a função original não recebe a lista de tempos de chegada.
- Confirme que o significado da prioridade corresponde à convenção usada pelo professor. Nesta implementação, valores menores indicam prioridade maior.
- Antes da entrega, teste os algoritmos com entradas manuais e confira os tempos de espera e a média.
- O FCFS original do código-base executa os processos pela ordem dos índices e não considera diretamente tempos de chegada diferentes.

USO DE INTELIGÊNCIA ARTIFICIAL
Foi utilizada a ferramenta ChatGPT para auxiliar na elaboração e documentação de trechos dos algoritmos de escalonamento de processos. A assistência foi utilizada para explicar a lógica e apoiar a escrita da documentação.


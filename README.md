# Von-Neumann-X-Harvard
# Von Neumann
	
	A arquitetura de Von Neumann é principalmente caracterizada por armazenar os dados na mesma área da memória em que armazena os programas, agilizando o processo de manipulação desses programas e evitando o uso de conexões de maiores distâncias até os dados. Ela formalizou o projeto lógico de um computador, já que apresentava seus elementos de forma compacta.
	A máquina de Von Neumann é composta por: Memória, Unidade Lógica Aritmética (ULA), Unidade de Controle de Programa (UC) e dispositivos de entrada e saída (E/S ou I/O).
	A memória era de grande importância, pois aparelhos que realizam grandes cálculos precisam de espaço para armazenar seus resultados, além de facilitar a comunicação entre os dados e o programa. Inicialmente tinha apenas 4096 palavras de 40 bits, compostos por 2 instruções de 20 bits ou apenas 1 inteiro. Essas instruções tinham 8 bits para o tipo e 12 bits para o endereçamento de memória.
	A ULA é uma unidade especializada responsável por realizar as operações lógicas (boolean) e aritméticas. 
	Já a UC é quem dita a sequência correta de operações a ser executada, organizando as instruções e os dados. Ela dá ordens de controle para os outros elementos da máquina.
	Os dispositivos de E/S são responsáveis por enviar e receber instruções e dados da CPU. A CPU, por sua vez, é o conjunto da UC com a ULA e alguns registradores, que são memórias de alta velocidade usadas para guardar dados temporários, mas de prioridade alta. Por isso são tão próximas da ULA. Existem registradores com dados pré-carregados, chamados de registradores de função específica. Existem também os OP Codes, que são instruções específicas para a arquitetura de cada máquina. O conceito de Clock também era muito importante, pois é com ele que a CPU pode se referenciar com o tempo. É gerada uma onda simples de “ligado e desligado” com tempo específico, necessária para garantir um padrão nas ações da CPU. Interrupções, ou sinais de controles externos, são sinais emitidos por dispositivos externos ao processador, os dispositivos de E/S, usados para que se possa perceber ações externas.
	As instruções e os dados ficam armazenados em endereços na memória. Esses endereços são posições únicas na memória. Para que as informações sejam armazenadas, elas devem ser transmitidas através de um barramento, que seriam conexões entre os componentes da máquina.

	As máquinas de Von Neumann têm um ciclo de execução característico, que se dá da seguinte forma: 
	No início do ciclo a UC busca pela próxima instrução na memória principal. A instrução é carregada e decodificada. Em seguida a UC verifica  se existem operandos necessários, trazendo-os da memória para os registradores se for o caso. A ULA então executa a instrução e então a UC verifica os resultados e os armazena já na memória ou os mantém próximos, em registradores. Uma próxima instrução é buscada, iniciando outro ciclo. 

	Apesar da arquitetura de Von Neumann ser muito bem elaborada, ela tinha seus defeitos. O mais famoso deles ficou conhecido como Gargalo de Von Neumann.
	Esse problema acontecia pois o barramento que levava dados era o mesmo que levava as instruções, e ainda levavam para a mesma memória, gerando tempo ocioso para a CPU, pois dessa forma ela era mais rápida do que o canal de comunicação com a memória. Considerando que a CPU é muitas vezes mais rápida do que a memória, esse problema piorava com o tempo, pois os processadores avançavam e as memórias ficavam para trás. Para resolver isso surgiu a arquitetura de Harvard.

#Harvard

        Surgindo como uma solução para o gargalo de Von Neumann, a arquitetura de Harvard era parecida com essa primeira, mas suas diferenças foram quem chamaram atenção.
        Ao separar os barramentos para instrução dos barramentos para dados, parte do problema já foi resolvido. Para deixar o gargalo completamente para trás, foram criadas também memórias espefícicas para barramentos e outras para dados.
	
	

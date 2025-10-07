# Relatório - Lab 4: Sincronização de Threads

**Nome:** [Seu nome]  
**Data:** [Data de entrega]

## Exercício 1: Contador com Mutex

### Implementação
- [ ] Mutex inicializado corretamente
- [ ] Lock/unlock implementados na função incrementar_likes
- [ ] Mutex destruído ao final

### Resultados Observados
**Com Mutex:**
- Valor final: ___________
- Tempo de execução: ___________

**Sem Mutex:**
- Valor final: ___________
- Diferença observada: ___________

### Análise
Descreva o comportamento observado e explique por que o mutex é necessário:

_______________________________________________

## Exercício 2: Produtor-Consumidor

### Implementação
- [ ] Mutex e variáveis de condição inicializados
- [ ] Função adicionar_pedido com sincronização
- [ ] Função processar_pedido com sincronização
- [ ] While loops corretos com pthread_cond_wait
- [ ] Estruturas destruídas ao final

### Resultados Observados
- Total de pedidos produzidos: ___________
- Total de pedidos consumidos: ___________
- Situações de buffer cheio observadas: ___________
- Situações de buffer vazio observadas: ___________

### Análise
Como as variáveis de condição melhoram a eficiência comparado a busy-waiting?

_______________________________________________

## Exercício 3: Leitores-Escritores

### Implementação
- [ ] Semáforo e mutex inicializados
- [ ] Controle de leitores implementado
- [ ] Controle de escritores implementado
- [ ] Primeiro/último leitor gerencia semáforo
- [ ] Estruturas destruídas ao final

### Resultados Observados
- Máximo de leitores simultâneos observado: ___________
- Tempo médio de espera dos escritores: ___________
- Ocorrências de starvation: ___________

### Análise
A solução implementada favorece leitores ou escritores? Justifique:

_______________________________________________

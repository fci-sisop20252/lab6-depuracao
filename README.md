# Lab 4: Sincronização de Threads

## Visão Geral
Laboratório focado em mecanismos de sincronização para coordenação entre threads: **mutex**, **variáveis de condição** e **semáforos**.

## Objetivos
- Aplicar exclusão mútua com mutex em recursos compartilhados
- Implementar comunicação entre threads com variáveis de condição
- Resolver problemas clássicos: produtor-consumidor e leitores-escritores
- Identificar e prevenir condições de corrida

## Estrutura
```
lab4-syncthreads/
├── src/                      # Códigos-fonte
│   ├── ex1_contador_mutex.c    # Contador com mutex
│   ├── ex2_pedidos_prodcons.c  # Produtor-consumidor
│   └── ex3_cache_leitores_escritores.c # Leitores-escritores
├── docs/                     # Documentação
│   └── sync_reference.md    # Referência rápida de sincronização
├── EXERCICIOS.md            # Descrição detalhada dos exercícios
└── RELATORIO_TEMPLATE.md   # Template para relatório
```

## Compilação
```bash
# Compilar exercícios (apos resolucao)
gcc -pthread src/ex1_contador_mutex.c -o ex1
gcc -pthread src/ex2_pedidos_prodcons.c -o ex2
gcc -pthread src/ex3_cache_leitores_escritores.c -o ex3

# Executar
./ex1
./ex2
./ex3
```

## Dicas Importantes

### Mutex
- Sempre destravar após travar: `pthread_mutex_lock()` → seção crítica → `pthread_mutex_unlock()`
- Evite esquecer de destravar em caminhos de erro
- Inicialize com `pthread_mutex_init()` ou `PTHREAD_MUTEX_INITIALIZER`

### Variáveis de Condição
- Use sempre com mutex associado
- Espera em loop: `while(condição) pthread_cond_wait(&cond, &mutex)`
- `signal` acorda uma thread, `broadcast` acorda todas

### Semáforos
- `sem_wait()` decrementa (bloqueia se 0)
- `sem_post()` incrementa (libera threads esperando)
- Útil para controlar número de recursos disponíveis

## Exercícios
1. **Contador com Mutex**: Sistema de likes em rede social
2. **Produtor-Consumidor**: Processamento de pedidos online
3. **Leitores-Escritores**: Cache de dados compartilhado

Consulte `EXERCICIOS.md` para descrições completas.
# README sobre Alocação Dinâmica em C

## Descrição

A alocação dinâmica de memória em C permite reservar espaço na memória durante a execução do programa. Isso é útil quando o tamanho da memória necessária não é conhecido em tempo de compilação e pode variar conforme a execução.

## Funções Principais

- **`malloc(size_t size)`**: Aloca um bloco de memória de `size` bytes e retorna um ponteiro para o início do bloco. A memória alocada não é inicializada.
  
- **`calloc(size_t num, size_t size)`**: Aloca memória para um array de `num` elementos, cada um com `size` bytes. A memória alocada é inicializada com zeros.
  
- **`realloc(void *ptr, size_t new_size)`**: Redimensiona um bloco de memória previamente alocado para `new_size` bytes. O ponteiro `ptr` deve apontar para um bloco de memória previamente alocado por `malloc` ou `calloc`.
  
- **`free(void *ptr)`**: Libera a memória que foi alocada com `malloc`, `calloc` ou `realloc`. Após liberar a memória, o ponteiro se torna inválido e não deve ser usado.

## Boas Práticas

- **Verifique o retorno de `malloc`, `calloc`, e `realloc`**: Garanta que a alocação foi bem-sucedida (verifique se o ponteiro não é `NULL`).
  
- **Libere a memória quando não for mais necessária**: Use `free` para liberar a memória alocada e evitar vazamentos de memória.
  
- **Não use ponteiros após liberá-los**: Após chamar `free`, o ponteiro não deve ser usado até que seja reatribuído ou inicializado novamente.

## Referências

Para mais informações sobre alocação dinâmica e gerenciamento de memória em C, consulte a documentação do seu compilador C ou materiais de referência sobre programação em C.

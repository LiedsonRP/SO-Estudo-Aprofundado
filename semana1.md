# 📌 Fase Zero — Semana 1: Fundamentos de C (Desafios)

**Objetivo:** Construir base sólida em C, entendendo arrays, strings, ponteiros e funções.  
**Duração:** 4h sábado + 4h domingo (~8h total).  
**Ambiente:** MinGW-w64, IDE offline ou WSL2 + GCC.

---

## 1️⃣ Configuração mínima
- [ ] Compilador C instalado (MinGW-w64, Code::Blocks ou Dev-C++).  
- [ ] Editor de texto instalado (VSCode, Notepad++ ou Vim).  
- [ ] Git instalado (opcional, mas recomendado).  
- [ ] Pasta de trabalho criada: `C_offline/exemplos/`.  

---

## 2️⃣ Desafios da Semana 1

### Desafio 1 — Hello World
**Descrição:** Criar e compilar o primeiro programa em C para verificar se o ambiente funciona.  
**Passos:**
1. Criar arquivo `hello.c` com:
```c
#include <stdio.h>
int main() {
    printf("Hello, world!\n");
    return 0;
}
Compilar: gcc hello.c -o hello.exe

Executar: hello.exe

Confirmar saída: Hello, world!

 Concluído

Desafio 2 — Array simples e ponteiro
Descrição: Manipular e imprimir valores de um array usando ponteiros.
Passos:

Criar array.c com:

c
Copiar código
#include <stdio.h>
int main() {
    int a[5] = {1,2,3,4,5};
    int *p = a;
    for(int i=0;i<5;i++)
        printf("%d ", *(p+i));
    printf("\n");
    return 0;
}
Compilar e executar.

Observar a saída e entender relação ponteiro ↔ array.

 Concluído

Desafio 3 — Soma de elementos de array
Descrição: Criar função que recebe array por ponteiro e retorna a soma dos elementos.
Passos:

Criar sum.c:

c
Copiar código
#include <stdio.h>
int sum(int *arr, int size) {
    int s = 0;
    for(int i=0;i<size;i++) s += *(arr+i);
    return s;
}
int main() {
    int nums[4] = {10,20,30,40};
    printf("Soma = %d\n", sum(nums,4));
    return 0;
}
Compilar e executar.

Verificar saída: Soma = 100

 Concluído

Desafio 4 — Multiplicar elementos do array
Descrição: Criar função que multiplica cada elemento do array por um valor passado como parâmetro.
Passos:

Criar multiply.c:

c
Copiar código
#include <stdio.h>
void multiply(int *arr, int size, int factor) {
    for(int i=0;i<size;i++)
        *(arr+i) *= factor;
}
int main() {
    int nums[5] = {1,2,3,4,5};
    multiply(nums,5,3);
    for(int i=0;i<5;i++) printf("%d ", nums[i]);
    printf("\n");
    return 0;
}
Compilar e executar.

Verificar saída: 3 6 9 12 15

 Concluído

Desafio 5 — Trocar elementos de um array
Descrição: Criar função que troca dois elementos usando ponteiros.
Passos:

Criar swap.c:

c
Copiar código
#include <stdio.h>
void swap(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}
int main() {
    int x=5, y=10;
    swap(&x,&y);
    printf("x=%d y=%d\n", x, y);
    return 0;
}
Compilar e executar.

Verificar saída: x=10 y=5

 Concluído

Desafio 6 — Contar caracteres de uma string
Descrição: Criar função que recebe uma string e retorna o número de caracteres.
Passos:

Criar strlen_custom.c:

c
Copiar código
#include <stdio.h>
int str_length(char *s) {
    int count = 0;
    while(*(s+count) != '\0') count++;
    return count;
}
int main() {
    char str[] = "C é legal!";
    printf("Tamanho: %d\n", str_length(str));
    return 0;
}
Compilar e executar.

Verificar saída: Tamanho: 10

 Concluído

Desafio 7 — Inverter string
Descrição: Criar função que inverte a string in-place usando ponteiros.
Passos:

Criar reverse.c:

c
Copiar código
#include <stdio.h>
void reverse(char *s) {
    int len = 0;
    while(s[len] != '\0') len++;
    for(int i=0;i<len/2;i++) {
        char temp = s[i];
        s[i] = s[len-1-i];
        s[len-1-i] = temp;
    }
}
int main() {
    char str[] = "C é legal!";
    reverse(str);
    printf("%s\n", str);
    return 0;
}
Compilar e executar.

Verificar saída: !lage lé éC

 Concluído

Desafio 8 — Função que retorna array estático
Descrição: Criar função que retorna ponteiro para array estático.
Passos:

Criar return_array.c:

c
Copiar código
#include <stdio.h>
int* createArray() {
    static int arr[3] = {1,2,3};
    return arr;
}
int main() {
    int *p = createArray();
    for(int i=0;i<3;i++) printf("%d ", p[i]);
    printf("\n");
    return 0;
}
Compilar e executar.

Verificar saída: 1 2 3

 Concluído

3️⃣ Commit no repositório (Checkpoint 1)
Inicializar Git (caso ainda não tenha):

cmd
Copiar código
git init
git add *.c
git commit -m "Checkpoint 1: desafios Semana 1 concluídos"
 Concluído

✅ Checkpoint final
 Todos os programas compilam e rodam.

 Entendo e consigo explicar a diferença ponteiro vs array.

 Commit realizado no repositório offline.

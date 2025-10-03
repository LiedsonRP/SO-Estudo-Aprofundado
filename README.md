# SO-Estudo-Aprofundado
Repositório contendo evolução no estudo de sistemas operacionais seguindo cronograma estruturado

# 📌 Fase Zero — Checklist de Estudos para Kernel/OS

Plano de 8 fins de semana (8h cada, 2 dias × 4h).  
Objetivo: construir base sólida em C, Assembly, Arquitetura, Estruturas de Dados e Unix API antes de entrar no xv6/Pintos.

---

## ✅ Status
- [ ] Fim de semana 1 — C: ponteiros e arrays
- [ ] Fim de semana 2 — C: mini-malloc e structs
- [ ] Fim de semana 3 — Assembly básico + integração C/ASM
- [ ] Fim de semana 4 — Arquitetura: memória virtual e interrupções
- [ ] Fim de semana 5 — Estruturas de dados (fila, hash)
- [ ] Fim de semana 6 — Unix/Linux básico (fork, exec, pipe, signals)
- [ ] Fim de semana 7 — Mini-projeto (simulador de scheduler)
- [ ] Fim de semana 8 — Revisão + preparação xv6

---

## 📅 Fim de semana 1 — Fundamentos de C
- [ ] Escrever e compilar programas simples (arrays, strings).
- [ ] Implementar funções que manipulam arrays via ponteiros.
- [ ] Commitar 2 programas no repositório.

**Checkpoint 1:** explicar ponteiro vs array e mostrar programas rodando.

---

## 📅 Fim de semana 2 — Mini-malloc e Structs
- [ ] Implementar `my_malloc` e `my_free` usando pool estático.
- [ ] Implementar lista ligada em C com structs.
- [ ] Commitar código e exemplos.

**Checkpoint 2:** mini-malloc funcionando + lista ligada.

---

## 📅 Fim de semana 3 — Assembly x86_64
- [ ] Estudar convenção de chamadas SysV (registradores).  
- [ ] Implementar função `add(a,b)` em ASM e chamar em C.  
- [ ] Implementar `write(1,"x",1)` direto em ASM (syscall).  
- [ ] Commitar código e notas.

**Checkpoint 3:** integração C↔ASM + syscall manual.

---

## 📅 Fim de semana 4 — Arquitetura
- [ ] Estudar MMU, paginação e TLB.  
- [ ] Desenhar fluxo virtual→físico.  
- [ ] Escrever documento explicando page fault.  
- [ ] Commitar diagramas/notas.

**Checkpoint 4:** diagrama + texto explicando page fault.

---

## 📅 Fim de semana 5 — Estruturas de Dados
- [ ] Implementar fila circular em C.  
- [ ] Simular escalonador simples (enqueue/dequeue PIDs).  
- [ ] Implementar hash table básica (chaining).  
- [ ] Commitar código e testes.

**Checkpoint 5:** fila + hash table.

---

## 📅 Fim de semana 6 — Unix/Linux
- [ ] Estudar processos e sinais.  
- [ ] Implementar programa com `fork` + `exec` + `pipe`.  
- [ ] Rodar com `strace` e salvar saída.  
- [ ] Implementar handler para `SIGCHLD`.  
- [ ] Commitar código e logs.

**Checkpoint 6:** fork/exec/pipe + handler de SIGCHLD.

---

## 📅 Fim de semana 7 — Mini-Projeto
- [ ] Projetar simulador de scheduler (fila circular + processos filhos).  
- [ ] Usar `kill(SIGSTOP/SIGCONT)` para simular quantum.  
- [ ] Adicionar logging e README de uso.  
- [ ] Commitar e taggear `fase0-complete`.

**Checkpoint 7:** mini-projeto funcionando com documentação.

---

## 📅 Fim de semana 8 — Revisão e Preparação
- [ ] Revisar pontos fracos e reforçar.  
- [ ] Organizar repositório, limpar código e criar `NOTAS.md`.  
- [ ] Testar ambiente para xv6 (clone, make, qemu).  
- [ ] Commitar e taggear `fase0-done`.

**Checkpoint Final:** repositório completo + pronto para xv6.

---

# 📖 Recursos recomendados
- C: *The C Programming Language* (K&R).  
- Assembly: “x86-64 System V ABI” (resumo online).  
- Unix: *The Linux Programming Interface* (Kerrisk).  
- Ferramentas: `gcc`, `make`, `gdb`, `objdump`, `strace`.  

---

# 💡 Dicas de execução
- Use blocos de 50/10 min (Pomodoro).  
- Sempre fazer commit no final de cada dia (sábado e domingo).  
- Registre dúvidas em `NOTAS.md` (curto, 200–300 palavras).  
- Ao final da Fase Zero → revisar `NOTAS.md` para identificar pontos fracos.

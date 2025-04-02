As integrantes da dupla são: Vívian e Lívia.

DIAGRAMA DE CLASSE (UML)
 +------------------+         +-----------------+         +------------------+
|      Sala        |         |     Usuário     |         |      Reserva     |
+------------------+         +-----------------+         +------------------+
| - id: int        |         | - id: int       |         | - id: int        |
| - nome: string   |         | - nome: string  |         | - data: datetime |
| - capacidade: int|         | - email: string |         | - status: string |
+------------------+         +-----------------+         +------------------+
| + reservar(): void|         | + criarReserva(): void |    | + confirmar(): void|
| + cancelar(): void|         | + cancelarReserva(): void|  | + cancelar(): void |
+------------------+         +-----------------+         +------------------+
        |                             |                          |
        +-----------------------------+--------------------------+
                      (associado a)       (associado a)

**EXPLICAÇÃO**
                     
1. **Início**: Usuário decide fazer a reserva.
2. **Escolher Sala**: Usuário escolhe a sala.
3. **Inserir Dados**: Usuário informa a data.
4. **Verificar Disponibilidade**: Sistema checa a disponibilidade.
5. **Confirmar ou Escolher Outra**: Se disponível, reserva é confirmada. Se não, escolhe outra sala.
6. **Fim**: Processo finaliza.

Esse é o fluxo simplificado do sistema de reserva de salas.

DIAGRAMA DE CLASSE (BPMN)

+-------------------+     +---------------------+     +------------------+
| Início do Processo| --> | Escolher a Sala     | --> | Inserir Dados    |
+-------------------+     +---------------------+     +------------------+
                               |                              |
                               v                              v
                      +------------------+          +-------------------+
                      | Verificar        |          | Confirmar Reserva |
                      | Disponibilidade  |          |                   |
                      +------------------+          +-------------------+
                               |                              |
                               v                              v
                      +------------------+          +-------------------+
                      | Sala Disponível  | -->   | Fim do Processo   |
                      +------------------+          +-------------------+
                               |
                               v
                      +------------------+
                      | Sala Indisponível|
                      +------------------+



explicação do Diagrama BPMN:

1. **Início**: O usuário decide fazer a reserva.

2. **Escolher Sala**: O usuário seleciona a sala.

3. **Inserir Dados**: O usuário informa a data da reserva.

3. **Verificar Disponibilidade**: O sistema checa se a sala está livre.

4. **Sala Disponível**: Se a sala estiver disponível, o usuário confirma a reserva.

5. **Confirmar Reserva**: A reserva é finalizada.

6. **Sala Indisponível**: Se a sala não estiver disponível, o usuário escolhe outra sala.

7. **Fim**: O processo termina.

Esse é o fluxo básico de reserva de sala.



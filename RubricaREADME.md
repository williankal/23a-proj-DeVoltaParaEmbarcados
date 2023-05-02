**C**

- [x] Controle desenvolvido para aplicação específica.
- [x] Utiliza interrupção nos botões.
- [x] Possuir quatro entradas digitais (botões).
- [x] Uma entrada analógica.
- [x] Feedbacks ao usuário: um de uso geral
- [x] Feedbacks ao usuário: outro deve indicar ao usuário o controle está pronto para uso (software PC reconhece controle, precisa de hand shake aqui).
- [x] Comunicação com o computador (bluetooth/ USB-UART).
- [x] Faz uso de RTOS
- [ ] Grava vídeo de uso

**C+**

- [X] No lugar de vários semáforos usa uma única fila para comunicar IRQ com task_bluetooth.

**B**

- [] Grupo cria um primeiro protótipo conceitual mecânico para o controle (pode usar papelão, massinha, modelo cad 3d, ...), não precisa ligar a parte elétrica ao mecânico, é só para termos uma ideia de como seria.
- [ ] Cria uma task dedicada para receber e processar dados da comunicação (computador → uC). (A ideia aqui é que o PC se comunique com o uC, para isso vocês podem usar a funcão self.ser.write() que irá enviar um char para o bluetooth e por consequência para o uC. No uC você pode ler esse dado usando: char status = usart_read(USART_COM, &readChar); Se status for 1 isso indica que um dado válido foi salvo em readChar.
Nessa comunicação vocês podem mandar qualquer coisa, já teve um grupo que enviou o nome da música do spotify que estava sendo tocada e exibiu a música no OELD. Não precisa ser algo tão complexo, podem enviar apenas um housekeeping da comunicação ou um ACK do recebimento do comando.)

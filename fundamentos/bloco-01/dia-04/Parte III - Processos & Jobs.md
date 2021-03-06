### Parte III - Processos & Jobs

1. Liste todos os processos;

   _**Resposta**_

   - `ps`

2. Agora use o comando [sleep ](https://linux.die.net/man/3/sleep)`30` [& ](https://linuxhandbook.com/run-process-background/);

   _**Resposta**_

   - `comando p/ criar um processo que roda por 30 segundo em background `

3. Use a listagem de processos para encontrar o PID do processo que está executando o comando `sleep 30` e termine a sua execução ~~(mate o processo) ~~;

   _**Resposta**_

   - `ps`
   - `enter`
   - `ctrl + C `

4. Execute novamente o comando `sleep 30` , mas agora sem o `&` . Depois, faça com que ele continue executando em background;

   _**Resposta**_

   - `sleep 30`
   - `ctrl + Z`
   - `bg`

5. Crie um processo em background que rode o comando `sleep` por 300 segundos.

   _**Resposta**_

   - `sleep 300 &`

6. Crie mais dois processos que rodem o comando `sleep` por 200 e 100 segundos, respectivamente.

   > Você deve criá-los em *foreground* (sem usar o `&` ) e suspendê-los (apertando `ctrl+z` ) após cada um começar a executar.

   _**Resposta**_

   - `sleep 300 &`
   - `sleep 200`
   - `ctrl + Z`
   - `sleep 100`
   - `ctrl + Z`

7. Verifique que apenas o processo `sleep 300` está em execução com o comando `jobs` . Suspenda a execução desse processo.

   > Você vai precisar trazer o processo para *foreground* ( `fg` ) e suspendê-lo ( `ctrl+z` ), ou enviar um sinal.

   _**Resposta**_

   - `jobs`
   - `fg %1` 
   - `ctrl + Z`

8. Retome a execução do processo `sleep 100` em background com o comando `bg` .

   _**Resposta**_

   - `bg %3`

9. Termine a execução de todos os processos `sleep` ~~(mate os processos) ~~.

   _**Resposta**_

   - `ps`
   - `kill -9 PID`
   - `kill -9 PID`
   - `kill -9 PID`

------
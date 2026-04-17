# 17/04/25
# Portas e Serviços

- ftp(File transfer protocol): Protocolo utilizado para a tranferência de dados em texto puro (sem criptografia).
   - Arquivo de Configuração: /etc/vsftpd.conf
     
   - Recomendações:
      - Não utilizar portas padrões(dificulta scans e facilita sua detecção)
      - Trocar o banners do serviço(Versão do programa responsável por porcessar os dados da comunicação Cliente e Server)
        
- ssh(secure-shell): shell, intrepretador de comandos/tradutor, responsável por interpretar e repassar os comandos para a
                     RAM armazenar -> CPU interpretar (ver o que está pedindo) e depois executar. Nese caso, cifrado.
   - Arquivo: /etc/ssh/sshd_config.d ou /etc/ssh/sshd_config.d/<"seu arquivo.conf">
   - Esse é mais chato de configurar por causa da complexidade(muita coisa)
   Recomendações:

      - Não utilizar portas padrões(dificulta scans e facilita sua detecção)
      - Trocar o banners do serviço(Versão do programa responsável por porcessar os dados da comunicação Cliente e Server)
        
 - Comandos de gerenciamento dos servers:
   
    - systemctl status <serviço>: mostra o estadio do serviço
    - systemctl restart <serviço>: restarta server, adcionando as configs adcionadas (as vezes não funciona), por isso tem:
      
       - systemctl stop <serviço>: para o serviço imediatamente
       - systemctl enable <serviço>: inicia automaticamente quando o host é ativado
       - systemctl disable <serviço>: não inicia mais automaticamente o serviço
       - [!] systemctl stop ssh.socket: para a conexão imediatamente (resolve bugs de conexões ativas)
       - [!] systemctl disable ssh.socket: removo a escuta automatica na porta 22 (muito útil pra mudar o serviço de lugar)
     




  
                     

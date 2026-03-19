# 09/03/26
# Flags Firewall

- 1° Flags de estrutura da regra (controle da chain)
  Usadas para criar, inserir ou remover regras.

  - -A — adiciona uma regra ao final da chain
  - -I — insere regra em uma posição específica
  - -D — remove uma regra
  - -R — substitui uma regra existente
  - -L — lista regras da chain
  - -F — limpa todas as regras
  - -N — cria uma nova chain
  - -X — remove uma chain
  - -P — define política padrão da chain
    
- 2️° Flags de protocolo e rede (camada de transporte)
  Filtram tipo de tráfego.

   - -p — define protocolo (tcp, udp, icmp)
   - -s — IP de origem
   - -d — IP de destino
   - --sport — porta de origem
   - --dport — porta de destino
   - -i — interface de entrada
   - -o — interface de saída

- 3️° Flags TCP (camada de sessão / controle de conexão)
  Filtram flags TCP usadas em scans.

   - --syn — pacotes iniciando conexão TCP
   - --tcp-flags — permite filtrar flags específicas

- Flags TCP que podem aparecer:

   - SYN — iniciar conexão
   - ACK — confirmar conexão
   - FIN — finalizar conexão
   - RST — resetar conexão
   - PSH — enviar dados imediatamente
   - URG — dados urgentes

- 4️° Flags de estado da conexão
   Usadas para firewall stateful.

   - -m state — carrega módulo de estado (módulo = recurso extra que o firewall vai utilizar).
   - --state NEW — nova conexão
   - --state ESTABLISHED — conexão já existente
   - --state RELATED — conexão relacionada
   - --state INVALID — pacote inválido



- 5️° Flags de detecção de comportamento
  Usadas para detectar scans ou abuso.

   - -m recent — rastrear IPs recentes
   - -name — nome da lista
   - --set — adiciona IP à lista
   - --update — atualiza contador
   - --seconds — janela de tempo
   - --hitcount — número de tentativas


- 6️° Flags de controle de taxa (rate limiting)
  Detectar flood ou brute force.

   - --m limit — módulo de limitação
   - --limit — taxa permitida
   - --limit-burst — número inicial permitido

- 7️° Flags de múltiplas portas
  Muito usadas em regras compactas.

   - -m multiport — permite várias portas
   - --dports — várias portas de destino
   - --sports — várias portas de origem

- 8️° Targets (ação da regra)
  Definem o que acontece com o pacote.

   - -j ACCEPT — permite pacote
   - -j DROP — descarta silenciosamente
   - -j REJECT — bloqueia e envia resposta
   - -j LOG — envia para log
   - -j RETURN — volta para chain anterior


- 9️° Flags de log
  Controlam como o log aparece.

   - --log-prefix — prefixo personalizado
   - --log-level — nível do log
   - --log-ip-options — logar opções IP
   - --log-tcp-options — logar opções TCP

- Quase toda regra de firewall segue:
   - iptables + ação + chain + filtro + condição + target
 


  


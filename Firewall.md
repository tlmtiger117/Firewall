# 25/02/26
# Firewall, INPUT,OUTPUT e FORWARD

- O que é um firewall: Firewall é um programa que atua diretamente no kernel do pc(o kernel que decide as regras do pc) por isso
                     ele é fundamental quando se o assunto se trata em proteger dispositivos(principalmente contra scanners).
  
  
- O que são chains: CHAINS , são os nomes das etapas/decisão que um pacote pode fazer para chegar num destino final(endpoint).
                    .OUTPUT,INPUT e FORWARD.


- OUTPUT: Tráfego gerado pelo seu dispositivo, cuja função é criar pacotes, sair para a rede e de lá para o endpoit.
 
    - ex:
        . Você(cria pacotes) -> rede(switch) -> endpoint(dispositivo final,recebe ou rejeita os pacotes).
        .Switch: repassa os dados em redes LAN, manda os dados para o MAC e porta especificado.
          
    


- INPUT: É todo tráfego cujo o destino final é você(sem repasse, o pacote chega e fica com você).
        . É uma camada muito protegida por justamente ser o trafego externo chegando em você(tráfego de outro pc).
  
    - ex:
        . Tráfego externo(pacotes chegando) -> sua rede(vai para sua interface) -> você(firewall filtrando pacotes ou não).
  

- FORWARD: Camada de repasse de dados, ele não é um endpoint, mas sim, um "repassador de informações/dados" da rede.
  
    - ex:
        .pc(cria pacotes) -> sua rede -> roteador(você) -> internet -> rede do endpoint -> endpoint(depois faz o processo inverso).
        .Percebeu que ele não fica com os dados? ele simplemente... repassa.


- [Aprendizado]: Reforcei conceitos que já utilize antigamente. Sempre útil revisar conteúdos anteriores.
  
    





                
            

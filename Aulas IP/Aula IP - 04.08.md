# Protocolos de Rede de Computadores
> São regras e procedimentos de comunicação que os sistemas precisam seguir p/ comunicar entre si. Eles não dependem da implementação, o que significa que sistemas e equipamentos de fabricantes diferentes podem comunicar-se desde que sigam as regras do protocolo.
> 
> Na arquitetura TCP/IP, os protocolos estão organizados em uma pilha de protocolos, de forma similar as camadas de arquitetura.a
> ---
![[Pasted image 20250804110542.png]]
---
Permite compatibilidade (Padronização de protocolos)

**Endereço IP:** Identifica a maquina

**Endereço logico:**, ele pode mudar, desde que os equipamentos que estão na rede notem isso, pode mudar a mascara

**Endereço Físico/Mac:** Endereço fixo/padrão, preso na memoria RAM, composto por 32 bits, 16 primeiros identifica quem foi o fabricante o resto é a gosto do fabricante para divisão de bits e criar seu modelo de comunicação

1 - Protocolos da camada de aplicação garantem a funcionalidade dos sistemas do usuário.
1.1 Protocolo HTTP

---
![[Pasted image 20250804114106.png]]

---
a) Usuário deseja acessar o site www.etec.com que está localizado no IP 172.168.0.32
b) Uma requisição será realizada quando o usuário digitar o endereço do site na barra do navegador
c) O servidor irá devolver uma resposta com o arquivo.html.solicitado
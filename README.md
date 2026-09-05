# Dois Escritórios + Servidores

## Contexto do projecto

Este projeto consistiu na implementação de uma **infraestrutura de rede corporativa no Cisco Packet Tracer**, simulando uma organização com uma **Matriz e uma Filial**, interligadas através de uma rede WAN e com servidores internos.

O objetivo foi criar uma infraestrutura mais completa, capaz de suportar **segmentação de departamentos, comunicação entre diferentes redes, atribuição automática de IPs, routing dinâmico, acesso à Internet e controlo de acesso**.

Do ponto de vista de administração de redes, este projeto permitiu consolidar conhecimentos em:

- VLANs
- Trunking IEEE 802.1Q
- Router-on-a-Stick
- Inter-VLAN Routing
- DHCP
- OSPF
- NAT/PAT
- ACLs
- IPv4 e Subnetting
- Comunicação WAN
- Troubleshooting

## Tecnologias utilizadas

- Cisco Packet Tracer
- Cisco IOS
- VLANs
- IEEE 802.1Q
- Router-on-a-Stick
- DHCP
- OSPF
- NAT/PAT
- ACLs
- IPv4 / Subnetting
- Inter-VLAN Routing
- ICMP / Ping

# Resumo executivo

### Visão geral do projecto

A infraestrutura foi dividida em duas localizações principais:

**Matriz**
- VLAN 10 — Servidores
- VLAN 20 — Financeiro
- VLAN 30 — RH
- VLAN 40 — IT
- VLAN 50 — Administração

**Filial**
- VLAN 10 — Financeiro
- VLAN 20 — RH
- VLAN 30 — IT
- VLAN 40 — Administração
- VLAN 50 — Servidores

Cada departamento foi colocado numa rede lógica própria, enquanto o **OSPF** foi utilizado para permitir a aprendizagem dinâmica das redes entre a Matriz e a Filial.

O **DHCP** foi utilizado para automatizar a configuração dos computadores, enquanto o **NAT/PAT** permitiu o acesso à Internet.

### Principais conhecimentos adquiridos

1. Criar uma infraestrutura segmentada através de VLANs.
2. Configurar trunks para transportar múltiplas VLANs.
3. Implementar comunicação entre VLANs através de Router-on-a-Stick.
4. Configurar DHCP para atribuição automática de endereços IP.
5. Utilizar OSPF para routing dinâmico entre diferentes redes.
6. Implementar NAT/PAT para acesso à Internet.
7. Utilizar ACLs para controlar o tráfego entre redes.
8. Utilizar comandos de diagnóstico para identificar falhas.
9. Analisar o percurso dos pacotes para identificar problemas de comunicação.

# Análise aprofundada

### Segmentação da rede

As VLANs permitiram separar os diferentes departamentos em redes lógicas independentes, reduzindo os domínios de broadcast e facilitando a aplicação de políticas de segurança.

### Routing

O **Router-on-a-Stick** permitiu realizar o encaminhamento entre as diferentes VLANs através de subinterfaces.

O **OSPF** foi utilizado para permitir a troca dinâmica de informações de routing entre a Matriz e a Filial.

### DHCP

O DHCP automatizou a configuração dos computadores, fornecendo:

- Endereço IP
- Máscara de sub-rede
- Gateway padrão
- Servidor DNS

### Segurança

As **ACLs** foram utilizadas para controlar o tráfego entre determinados departamentos e proteger os recursos da rede, incluindo os servidores.

### NAT/PAT e Troubleshooting

Um dos principais desafios encontrados durante o projeto foi um problema relacionado com o **NAT/PAT**.

Durante os testes, verificou-se que o routing entre a Matriz e a Filial estava funcional, mas determinados dispositivos não conseguiam comunicar corretamente.

Foram analisados diferentes componentes da infraestrutura, incluindo:

- VLANs
- Trunks
- Subinterfaces
- Gateways
- OSPF
- Tabelas de routing
- ACLs
- Interfaces WAN
- NAT

A causa foi identificada na política de NAT: o tráfego destinado à rede privada da Filial estava a ser traduzido como se fosse tráfego destinado à Internet.

A solução consistiu na utilização de uma **ACL estendida no NAT**, permitindo diferenciar o tráfego entre as duas sedes do tráfego destinado à Internet.

Este problema foi uma parte importante do projeto, pois permitiu desenvolver competências de **troubleshooting**, análise de pacotes e compreensão da interação entre routing, NAT e ACLs.

# Resultado final

A infraestrutura ficou funcional, permitindo:

- Comunicação entre os departamentos conforme as políticas definidas;
- Comunicação entre Matriz e Filial;
- Routing dinâmico através de OSPF;
- Atribuição automática de IPs através de DHCP;
- Acesso à Internet através de NAT/PAT;
- Controlo de tráfego através de ACLs;
- Comunicação com servidores;
- Segmentação da rede através de VLANs.

## Competências desenvolvidas

- Administração de redes Cisco
- Configuração de VLANs e Trunks
- Inter-VLAN Routing
- OSPF
- DHCP
- NAT/PAT
- ACLs
- IPv4 e Subnetting
- Troubleshooting de redes
- Análise de tabelas de routing
- Análise de traduções NAT
- Diagnóstico de problemas de conectividade

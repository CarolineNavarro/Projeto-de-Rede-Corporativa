# Projeto de Rede Corporativa
Projeto de rede com matriz e 3 filiais, totalizando 4 redes interligadas em anel com RIP. Cada rede tem 1 roteador, 2 switches e 4 VLANs com 6 dispositivos. A matriz possui servidores de DNS/HTTP (www.empresa.com) e e-mail. Dispositivos recebem IP via DHCP e acessam os serviços centralizados.

# Descrição da Rede (Português)
O projeto consiste na implementação de uma infraestrutura de rede corporativa composta por uma matriz e três filiais, totalizando quatro redes interligadas. Cada rede é formada por um roteador principal e dois switches de acesso. Os roteadores estão conectados em topologia de anel, configurados com o protocolo RIP, garantindo alta disponibilidade e visibilidade mútua entre as unidades.
Na matriz estão localizados dois servidores essenciais:

- Um servidor responsável pelos serviços de DNS e HTTP, hospedando o site institucional da empresa, acessado através de www.empresa.com.

- Um segundo servidor dedicado ao serviço de e-mail corporativo.

Cada rede (matriz e filiais) possui quatro VLANs, com 6 dispositivos por VLAN. O roteador de cada rede está configurado com serviço DHCP, atribuindo dinamicamente os endereços IP para os dispositivos em suas respectivas VLANs.
Todos os dispositivos da rede têm acesso funcional ao servidor DNS/HTTP e ao servidor de e-mail localizados na matriz.

# Network Description (English)
The project involves the implementation of a corporate network infrastructure consisting of a main office and three branch offices, totaling four interconnected networks. Each network is composed of a main router and two access switches. The routers are connected in a ring topology and configured with the RIP routing protocol, ensuring high availability and mutual visibility between the units.
At the main office, there are two essential servers:

- One server is responsible for DNS and HTTP services, hosting the company's official website, accessible via www.empresa.com.

- A second server is dedicated to the corporate email service.

Each network (main office and branches) has four VLANs, with 6 devices per VLAN. The router in each network is configured with DHCP service, dynamically assigning IP addresses to the devices within their respective VLANs.
All devices in the network have functional access to the DNS/HTTP server and the email server located at the main office.

# IPs Address

| Matriz |
| :---- |

| Device | Interface | Vlans |  | IP Address | Subnet Mask | Default Gateway |
| ----- | :---: | :---: | ----- | :---: | :---: | :---: |
| **Router 00** | Se2/0 |  |  | 200.0.0.1 | 255.255.255.252 |  |
|  |  |  |  |  |  |  |
|  | Se3/0 |  |  | 200.0.3.2 | 255.255.255.252 |  |
|  |  |  |  |  |  |  |
|  | Fa0/0.5 |  |  | 192.168.5.1 | 255.255.255.0 |  |
|  |  |  |  |  |  |  |
|  | Fa0/0.6 |  |  | 192.168.6.1 | 255.255.255.0 |  |
|  | Fa1/0.7 |  |  | 192.168.7.1 | 255.255.255.0 |  |
|  | Fa1/0.8 |  |  | 192.168.8.1 | 255.255.255.0 |  |
|  |  |  |  |  |  |  |
| **Switch 00** | Fa0/1-Fa0/6 e Fa0/23 | 5 |  | 192.168.5.0 | 255.255.255.0 | 192.168.5.1 |
|  | Fa0/7-Fa0/12 | 6 |  | 192.168.6.0 | 255.255.255.0 | 192.168.6.1 |
|  |  |  |  |  |  |  |
| **Switch 01** | Fa0/1-Fa0/6 Fa0/23 | 7 |  | 192.168.7.0 | 255.255.255.0 | 192.168.7.1 |
|  | Fa0/7-Fa0/12 | 8 |  | 192.168.8.0 | 255.255.255.0 | 192.168.8.1 |
|  |  |  |  |  |  |  |
| **Server DNS/HTTP** | Fa0/0 | 5 |  | 192.168.5.30 | 255.255.255.0 | 192.168.5.1 |
| **Server Email** | Fa0/0 | 7 |  | 192.168.7.30 | 255.255.255.0 | 192.168.7.1 |

| Filial 1 |
| :---- |

| Device | Interface | Vlans |  | IP Address | Subnet Mask | Default Gateway |
| ----- | :---: | :---: | ----- | :---: | :---: | :---: |
| **Router 01** | Se2/0 |  |  | 200.0.0.2 | 255.255.255.252 |  |
|  |  |  |  |  |  |  |
|  | Se3/0 |  |  | 200.0.1.1 | 255.255.255.252 |  |
|  |  |  |  |  |  |  |
|  | Fa0/0.9 |  |  | 192.168.9.1 | 255.255.255.0 |  |
|  |  |  |  |  |  |  |
|  | Fa0/0.10 |  |  | 192.168.10.1 | 255.255.255.0 |  |
|  | Fa1/0.11 |  |  | 192.168.11.1 | 255.255.255.0 |  |
|  | Fa1/0.12 |  |  | 192.168.12.1 | 255.255.255.0 |  |
|  |  |  |  |  |  |  |
| **Switch 02** | Fa0/1-Fa0/6 | 9 |  | 192.168.9.0 | 255.255.255.0 | 192.168.9.1 |
|  | Fa0/7-Fa0/12 | 10 |  | 192.168.10.0 | 255.255.255.0 | 192.168.10.1 |
|  |  |  |  |  |  |  |
| **Switch 03** | Fa0/1-Fa0/6 | 11 |  | 192.168.11.0 | 255.255.255.0 | 192.168.11.1 |
|  | Fa0/7-Fa0/12 | 12 |  | 192.168.12.0 | 255.255.255.0 | 192.168.12.1 |

| Filial 2 |
| :---- |

| Device | Interface | Vlans |  | IP Address | Subnet Mask | Default Gateway |
| ----- | :---: | :---: | ----- | :---: | :---: | :---: |
| **Router 02** | Se2/0 |  |  | 200.0.1.2 | 255.255.255.252 |  |
|  |  |  |  |  |  |  |
|  | Se3/0 |  |  | 200.0.2.1 | 255.255.255.252 |  |
|  |  |  |  |  |  |  |
|  | Fa0/0.13 |  |  | 192.168.13.1 | 255.255.255.0 |  |
|  |  |  |  |  |  |  |
|  | Fa0/0.14 |  |  | 192.168.14.1 | 255.255.255.0 |  |
|  | Fa1/0.15 |  |  | 192.168.15.1 | 255.255.255.0 |  |
|  | Fa1/0.16 |  |  | 192.168.16.1 | 255.255.255.0 |  |
|  |  |  |  |  |  |  |
| **Switch 04** | Fa0/1-Fa0/6 | 13 |  | 192.168.13.0 | 255.255.255.0 | 192.168.13.1 |
|  | Fa0/7-Fa0/12 | 14 |  | 192.168.14.0 | 255.255.255.0 | 192.168.14.1 |
|  |  |  |  |  |  |  |
| **Switch 05** | Fa0/1-Fa0/6 | 15 |  | 192.168.15.0 | 255.255.255.0 | 192.168.15.1 |
|  | Fa0/7-Fa0/12 | 16 |  | 192.168.16.0 | 255.255.255.0 | 192.168.16.1 |

| Filial 3 |
| :---- |

| Device | Interface | Vlans |  | IP Address | Subnet Mask | Default Gateway |
| ----- | :---: | :---: | ----- | :---: | :---: | :---: |
| **Router 03** | Se2/0 |  |  | 200.0.2.2 | 255.255.255.252 |  |
|  |  |  |  |  |  |  |
|  | Se3/0 |  |  | 200.0.3.1 | 255.255.255.252 |  |
|  |  |  |  |  |  |  |
|  | Fa0/0.17 |  |  | 192.168.17.1 | 255.255.255.0 |  |
|  |  |  |  |  |  |  |
|  | Fa0/0.18 |  |  | 192.168.18.1 | 255.255.255.0 |  |
|  | Fa1/0.19 |  |  | 192.168.19.1 | 255.255.255.0 |  |
|  | Fa1/0.20 |  |  | 192.168.20.1 | 255.255.255.0 |  |
|  |  |  |  |  |  |  |
| **Switch 06** | Fa0/1-Fa0/6 | 17 |  | 192.168.17.0 | 255.255.255.0 | 192.168.17.1 |
|  | Fa0/7-Fa0/12 | 18 |  | 192.168.18.0 | 255.255.255.0 | 192.168.18.1 |
|  |  |  |  |  |  |  |
| **Switch 07** | Fa0/1-Fa0/6 | 19 |  | 192.168.19.0 | 255.255.255.0 | 192.168.19.1 |
|  | Fa0/7-Fa0/12 | 20 |  | 192.168.20.0 | 255.255.255.0 | 192.168.20.1 |



# Endereçamento IP

## 1. Plano de endereçamento

A rede será estruturada utilizando endereçamento IPv4 privado, com uma rede /24 para cada VLAN.

| VLAN | Setor         | Rede            | Gateway      |
| ---- | ------------- | --------------- | ------------ |
| 10   | Administração | 192.168.10.0/24 | 192.168.10.1 |
| 20   | Suporte       | 192.168.20.0/24 | 192.168.20.1 |
| 30   | Servidores    | 192.168.30.0/24 | 192.168.30.1 |

## 2. Dispositivos

### VLAN 10 — Administração

* Gateway: `192.168.10.1`
* PC-ADM-01: `192.168.10.10`
* PC-ADM-02: `192.168.10.11`

Máscara:

`255.255.255.0`

### VLAN 20 — Suporte

* Gateway: `192.168.20.1`
* PC-SUP-01: `192.168.20.10`
* PC-SUP-02: `192.168.20.11`

Máscara:

`255.255.255.0`

### VLAN 30 — Servidores

* Gateway: `192.168.30.1`
* SRV-01: `192.168.30.10`

Máscara:

`255.255.255.0`

## 3. Roteador

O roteador utilizará subinterfaces para realizar o roteamento entre as VLANs.

| Interface | VLAN | Endereço IP  |
| --------- | ---: | ------------ |
| G0/0.10   |   10 | 192.168.10.1 |
| G0/0.20   |   20 | 192.168.20.1 |
| G0/0.30   |   30 | 192.168.30.1 |

## 4. Gateway dos dispositivos

Cada dispositivo deverá utilizar como gateway o endereço da subinterface correspondente à sua VLAN.

Exemplo:

Um computador da VLAN 10 deverá utilizar:

* IP: `192.168.10.10`
* Máscara: `255.255.255.0`
* Gateway: `192.168.10.1`

## 5. Objetivo do endereçamento

A separação das redes permite identificar facilmente a qual setor cada endereço pertence e facilita o gerenciamento da infraestrutura.

A utilização de redes distintas também possibilita o roteamento entre VLANs por meio do roteador.

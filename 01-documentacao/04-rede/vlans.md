# Configuração de VLANs

## 1. Objetivo

As VLANs serão utilizadas para separar logicamente os setores da empresa, permitindo melhor organização da rede e controle do tráfego entre os diferentes grupos de dispositivos.

## 2. VLANs utilizadas

| VLAN | Nome          | Finalidade                           |
| ---: | ------------- | ------------------------------------ |
|   10 | ADMINISTRACAO | Computadores do setor administrativo |
|   20 | SUPORTE       | Computadores do setor de suporte     |
|   30 | SERVIDORES    | Servidores da empresa                |

## 3. Portas do switch

As portas do switch serão distribuídas conforme a função dos dispositivos.

| Porta  | Função    |  VLAN |
| ------ | --------- | ----: |
| Fa0/1  | PC-ADM-01 |    10 |
| Fa0/2  | PC-ADM-02 |    10 |
| Fa0/3  | PC-SUP-01 |    20 |
| Fa0/4  | PC-SUP-02 |    20 |
| Fa0/5  | SRV-01    |    30 |
| Fa0/24 | Roteador  | Trunk |

## 4. Configuração das VLANs

No switch, serão criadas as três VLANs:

```text
VLAN 10 — ADMINISTRACAO
VLAN 20 — SUPORTE
VLAN 30 — SERVIDORES
```

As portas conectadas aos computadores e ao servidor serão configuradas como portas de acesso (`access`), associadas à respectiva VLAN.

A porta conectada ao roteador será configurada como `trunk`, permitindo o transporte das VLANs 10, 20 e 30.

## 5. Roteamento entre VLANs

O roteador utilizará subinterfaces para realizar o roteamento entre as VLANs.

As subinterfaces serão:

```text
G0/0.10 → VLAN 10 → 192.168.10.1
G0/0.20 → VLAN 20 → 192.168.20.1
G0/0.30 → VLAN 30 → 192.168.30.1
```

Cada subinterface será associada ao respectivo identificador de VLAN por meio de encapsulamento 802.1Q.

## 6. Resultado esperado

Após a configuração, os dispositivos deverão:

* comunicar-se com dispositivos da mesma VLAN;
* utilizar o gateway correspondente à sua rede;
* comunicar-se entre VLANs por meio do roteador;
* utilizar o enlace trunk entre o switch e o roteador.

Os testes de conectividade serão realizados posteriormente no Cisco Packet Tracer e registrados como evidências do projeto.

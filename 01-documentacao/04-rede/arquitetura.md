# Arquitetura de Rede

## 1. Objetivo

Propor uma arquitetura de rede empresarial simples, organizada e funcional para reduzir problemas de desempenho e permitir a segmentação lógica dos dispositivos.

A arquitetura será desenvolvida no Cisco Packet Tracer e utilizará VLANs para separar os diferentes setores da empresa.

## 2. Arquitetura proposta

A estrutura será composta por:

* conexão com a Internet;
* roteador;
* switch gerenciável;
* computadores do setor de Administração;
* computadores do setor de Suporte;
* servidor.

A comunicação entre as VLANs será realizada pelo roteador utilizando o modelo Router-on-a-Stick.

## 3. Estrutura lógica

```text
                    INTERNET
                       |
                    ROTEADOR
                       |
                 SWITCH GERENCIÁVEL
                  /       |       \
                 /        |        \
          VLAN 10      VLAN 20     VLAN 30
       Administração    Suporte    Servidores
            |              |           |
          PCs            PCs        Servidor
```

## 4. Segmentação

A rede será dividida em três VLANs:

| VLAN | Setor         | Rede            |
| ---- | ------------- | --------------- |
| 10   | Administração | 192.168.10.0/24 |
| 20   | Suporte       | 192.168.20.0/24 |
| 30   | Servidores    | 192.168.30.0/24 |

A segmentação permite separar logicamente os dispositivos de cada setor, facilitando a organização e o gerenciamento da infraestrutura.

## 5. Comunicação

O switch será responsável pela conexão dos dispositivos dentro da infraestrutura local.

O enlace entre o switch e o roteador será configurado como trunk, permitindo o transporte das VLANs.

O roteador realizará o roteamento entre as redes utilizando subinterfaces associadas a cada VLAN.

## 6. Benefícios da arquitetura

A arquitetura proposta proporciona:

* segmentação lógica da rede;
* melhor organização dos dispositivos;
* redução do domínio de broadcast;
* facilidade de gerenciamento;
* possibilidade de aplicar políticas diferentes por setor;
* comunicação controlada entre as VLANs;
* estrutura simples para implementação no Cisco Packet Tracer.

## 7. Implementação

A arquitetura será implementada no Cisco Packet Tracer utilizando um roteador, um switch gerenciável, computadores para os setores de Administração e Suporte e um servidor.

Após a montagem da topologia, serão configurados os endereços IP, VLANs, portas de acesso e enlace trunk.

Posteriormente serão realizados testes de conectividade entre os dispositivos.

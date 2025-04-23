# ✈️ Sistema de Reserva de Assentos de Avião

Este projeto simula um sistema de reserva de assentos de um avião, utilizando comunicação **cliente-servidor** via **sockets TCP** em Python. O servidor gerencia as reservas e os clientes se conectam para solicitar assentos.

## ⚙️ Funcionalidades

- Reserva de múltiplos assentos simultaneamente
- Verificação de disponibilidade em tempo real
- Respostas personalizadas indicando assentos reservados ou já ocupados
- Controle de concorrência para evitar reservas duplicadas

## 🛠 Tecnologias Utilizadas

- Python 3
- Módulo `socket` (para comunicação cliente-servidor)
- Módulo `threading` (para múltiplos clientes simultâneos)

## 📁 Estrutura do Projeto

Sistema_reserva/
├── cliente.py        # Código do cliente: conecta ao servidor e envia solicitações de reserva de assentos
├── servidor.py       # Código do servidor: gerencia reservas e lida com múltiplos clientes simultaneamente
└── README.md         # Documentação do projeto

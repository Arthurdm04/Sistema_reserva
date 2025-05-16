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

## 📌 Instruções de Uso

### 1. Clonar o repositório
```bash
git clone https://github.com/Arthurdm04/Sistema_reserva
cd Sistema_reserva
```

### 2. Executar o servidor
Abra um terminal e inicie o servidor com o comando:
```bash
python servidor.py
```
O servidor ficará escutando conexões dos clientes e gerenciará as reservas de assentos.

### 3. Executar os clientes
Em outro terminal (ou em vários, para simular múltiplos usuários simultâneos), execute o cliente:
```bash
python cliente.py
```

### 4. Funcionamento do sistema
- Ao iniciar, o cliente se conecta ao servidor via socket.
- O usuário será solicitado a informar quantos assentos deseja reservar.
- O servidor verifica a disponibilidade dos assentos e responde informando quais assentos foram reservados com sucesso ou se algum já estava ocupado.
- Cada cliente executado simula um usuário diferente, e o servidor é capaz de lidar com vários clientes simultaneamente graças à utilização de *threads*.

### Exemplo de uso:
```
Digite quantos assentos deseja reservar: 3
Assentos reservados com sucesso: [1, 2, 3]
```

Se outro cliente tentar reservar assentos já ocupados:
```
Digite quantos assentos deseja reservar: 2
Os seguintes assentos já estão ocupados: [2, 3]
Assentos reservados com sucesso: [4, 5]
```

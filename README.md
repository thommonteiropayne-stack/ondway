# ONDWAY

Pedidos pelo celular para barracas de praia. O cliente aponta a câmera para o QR Code do guarda-sol, faz o pedido e chama o garçom sem sair do lugar. O dono recebe tudo num painel no próprio celular.

## Como usar

- **Tela inicial do teste:** `index.html`
- **Painel do dono:** `index.html?b=<codigo-da-barraca>#barraca`
- **Cliente no guarda-sol N:** `index.html?b=<codigo-da-barraca>#gs-N`

Sem o parâmetro `b`, o sistema usa a barraca `teste`.

## Tecnologia

- Página única em HTML/JS, sem build.
- Banco de dados: Firebase Firestore (projeto `ondway-8def5`, região `southamerica-east1`).
- Dados de cada barraca ficam em `barracas/<codigo>/` (`cardapio`, `sessoes`, `pedidos`, `config`).

## Pendências antes de usar com clientes de verdade

- Regras de segurança do Firestore (hoje em modo de teste, que expira em 21/12/2026).
- Login para o painel do dono.

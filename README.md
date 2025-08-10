# Consulta de Pagamentos Automática com Selenium

Este script automatiza a consulta de pagamentos de clientes utilizando **Selenium** para acessar o site de consulta e **OpenPyXL** para manipular planilhas Excel.

## 📋 Funcionalidades
- Lê uma lista de clientes (nome, valor, CPF, vencimento) de um arquivo Excel (`dados_clientes.xlsx`).
- Acessa automaticamente o site de consulta de CPF.
- Pesquisa cada CPF e coleta:
  - Status do pagamento (em dia ou pendente).
  - Data de pagamento (se disponível).
  - Método de pagamento (se disponível).
- Registra as informações coletadas em um arquivo Excel de fechamento (`planilha fechamento.xlsx`).

## 📂 Estrutura esperada
├── dados_clientes.xlsx # Planilha de entrada com os clientes

├── planilha fechamento.xlsx # Planilha de saída com o resultado da consulta

└── app.py # Script principal

## 📦 Pré-requisitos
- **Python 3.x**
- **Google Chrome** instalado
- **Chromedriver** compatível com sua versão do Chrome
- Bibliotecas Python:
  ```bash
  pip install selenium openpyxl

📝 Formato da planilha dados_clientes.xlsx

A planilha deve conter os seguintes cabeçalhos na primeira linha:

| Nome        | Valor  | CPF         | Vencimento |
| ----------- | ------ | ----------- | ---------- |
| João Silva  | 150.00 | 12345678900 | 10/08/2025 |
| Maria Souza | 200.00 | 98765432100 | 15/08/2025 |

▶️ Como executar
Certifique-se de ter instalado os pré-requisitos.

Coloque as planilhas dados_clientes.xlsx e planilha fechamento.xlsx na mesma pasta do app.py.

Execute o script:

  ```bash
  python app.py
````

Aguarde o processo automático.

Os resultados serão salvos em planilha `fechamento.xlsx`.
 

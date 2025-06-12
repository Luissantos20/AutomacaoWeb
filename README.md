# 🤖 Automatizador de Downloads com Selenium

Este script Python automatiza o processo de **acesso, navegação, clique e download de arquivos** no site da Câmara Municipal de Valparaíso. Ele utiliza o Selenium com o navegador Google Chrome configurado para downloads automáticos, navega por várias páginas de tabelas e realiza o download de anexos de forma segura e eficiente.

---

## 📌 Objetivo

- Acessar automaticamente o site de atos administrativos.
- Percorrer todas as páginas da tabela de documentos.
- Clicar em cada item da tabela, realizar o download dos arquivos e retornar à lista.
- Repetir o processo para múltiplas páginas (16 no total).

---

## 🧰 Tecnologias Utilizadas

- [Python 3](https://www.python.org/)
- [Selenium](https://www.selenium.dev/)
- [webdriver-manager](https://pypi.org/project/webdriver-manager/)
- [Google Chrome](https://www.google.com/chrome/)
- XPath e Select para interação com elementos HTML

---
## ⚙️ Configurações do Navegador
Download automático ativado

Desativação de popups

Diretório de download customizado:

"download.default_directory": r"C:\Users\Usuario\Downloads\downloadsPV"

---

## 🚀 Como Executar
Certifique-se de ter o Google Chrome instalado.

Ajuste o caminho download.default_directory se necessário.

Execute o script:

python nome_do_arquivo.py
O navegador será aberto automaticamente, navegará até o site, aceitará cookies e começará a processar cada linha da tabela para realizar os downloads.

---

## 🔄 Lógica do Script
Abrir o site e maximizar a janela.

Aceitar cookies, se necessário.

Laço principal por 16 páginas da tabela:

Localiza todas as linhas da tabela.

Clica linha por linha:

Acessa a página de download.

Clica no botão de download.

Volta para a tabela.

Verifica se a página ainda é a mesma e recarrega se necessário.

Ao final de cada página, troca para a próxima página via menu suspenso (<select>).

---

## 📦 Requisitos

- Python 3 instalado
- Instalar as dependências:

```bash
pip install selenium webdriver-manager


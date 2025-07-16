# 🔍 OSINT Recon Script (Bash)

Este script automatiza a coleta básica de informações públicas sobre um domínio (reconhecimento passivo) usando ferramentas de linha de comando amplamente utilizadas na comunidade de segurança.

## ⚙️ Requisitos

Você deve ter as seguintes ferramentas instaladas:

- [`subfinder`](https://github.com/projectdiscovery/subfinder)
- [`assetfinder`](https://github.com/tomnomnom/assetfinder)
- [`httprobe`](https://github.com/tomnomnom/httprobe)
- [`gowitness`](https://github.com/sensepost/gowitness)
- `whois`
- `bash`

## 🚀 Como usar

```bash
chmod +x recon.sh
./recon.sh exemplo.com
```
## 📂 O que o script faz

Cria uma estrutura de diretórios para salvar os resultados:

info/ → informações WHOIS

subdomains/ → subdomínios encontrados e ativos

screenshots/ → capturas de tela dos domínios ativos

Executa:

whois no domínio-alvo

subfinder e assetfinder para encontrar subdomínios

httprobe para identificar quais estão ativos

gowitness para gerar screenshots das páginas

## 🧪 Exemplo de uso

```bash
./recon.sh plataformaexemplo.com
```
Resultado:

```css
[+] Iniciando pesquisa... 
[+] Rodando subfinder...
[+] Rodando assetfinder...
[+] Verificando domínios ativos...
[+] Fazendo capturas de tela...
```

## 📌 Observações

Os prints são salvos em screenshots/

Os dados são salvos em gowitness.jsonl, gowitness.csv e gowitness.sqlite3 (caso habilite)

Contribuições, melhorias ou sugestões são bem-vindas!

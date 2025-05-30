# Script de Atualização para o Sistema Food 3.0

Este script automatiza o processo de atualização de módulos essenciais do sistema Food 3.0, incluindo a instalação dos pacotes `.deb` mais recentes e a configuração do launcher `vsd-launcher`. Além disso, executa procedimentos de limpeza e reinicialização do terminal para garantir que as alterações sejam aplicadas corretamente.

---

## 🔧 O que este script faz

1. **Baixa os módulos mais recentes:**
   - `vs-os-interface`
   - `vs-autopag-se`

2. **Instala os módulos .deb** usando `dpkg` com fallback automático para `apt-get install -f`.

3. **Instala o launcher `vsd-launcher`** diretamente do GitHub.

4. **Executa limpeza de cache/token** e **configura o launcher para o ambiente Food 3.0**.

5. **Reinicia automaticamente o sistema**, com contagem regressiva.

---

## 📦 Pré-requisitos

- Distribuição baseada em Debian (ex: Ubuntu)
- Permissões de superusuário (`sudo`)
- Conexão com a internet via IPv4
- Ferramentas instaladas:
  - `wget`
  - `dpkg`
  - `apt-get`

---

## 🚀 Como executar

Você pode rodar o script diretamente com o comando abaixo:

```bash
sudo wget --inet4-only -O- https://raw.githubusercontent.com/CarloseOldenburg/Rollout-F3/refs/heads/main/F3 | bash
````

---

## 📄 Log de Execução

O script gera um log da instalação no arquivo `install_log.txt`, armazenando informações detalhadas sobre o progresso e possíveis erros.

---

## ⚠️ Avisos

* O script realiza **reinicialização automática do sistema** ao final do processo.
* Certifique-se de que **nenhuma operação crítica esteja em andamento** no terminal antes de executar.
* Caso ocorra erro durante a instalação de pacotes `.deb`, o script tentará corrigir dependências automaticamente via `apt-get install -f`.

---

## 🛠 Suporte

Caso precise de suporte ou deseje sugerir melhorias, entre em contato com o responsável pelo repositório ou abra uma issue no [GitHub](https://github.com/CarloseOldenburg/Rolout-F3).


# Calculadora de Reembolso Leves · LOC Frotas

Calculadora: https://gabrielpitter77.github.io/calculadora-reembolso/

- `index.html`: a calculadora. **Não contém dados de clientes**. Só muda quando a calculadora ganha funcionalidade nova.
- `dados.enc`: clientes, taxas, observações e tabelas MTBF, **criptografados** (AES-256). Abre só com o usuário e senha do Histórico de Manutenção.

A calculadora usa o mesmo login do painel Histórico de Manutenção e busca o histórico em `historico-manutencao/base.enc`.

## Atualizar clientes / MTBF (administrador)

1. Abra a calculadora pelo link e entre com o login do histórico.
2. ⚙ Administração → senha administrativa → edite clientes ou MTBF.
3. Clique em **🔒 Gerar dados.enc** (baixa o arquivo).
4. Neste repositório: **Add file → Upload files**, arraste o `dados.enc` (substitui o antigo) e **Commit changes**.
5. Em até ~10 minutos todos os analistas veem os dados novos no mesmo link.

## Cuidados

- Nunca suba aqui a calculadora antiga (arquivo .html com os clientes dentro), planilhas ou CSV: o repositório é público.
- Se a senha do Histórico mudar, gere o `dados.enc` de novo (ele usa a mesma chave da base do histórico).
- Os cálculos "Salvos por placa" ficam no navegador de cada analista. Para levar de um computador/versão para outro: **Salvos por placa → Exportar salvos / Importar salvos**.

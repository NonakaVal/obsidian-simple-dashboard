# Proveniência da base de código

## Fonte principal

- Repositório: `/home/val/Github/dashboard-navigator-for-obsidian`
- Revisão copiada: `a2b729544dd369c28eb66507a3da0faf08439d11`
- Versão declarada em `manifest.json` e `package.json`: `10.0.0`
- Estado da árvore de trabalho da fonte antes da cópia: limpo
- Conteúdo: arquivos rastreados nessa revisão, preservando a estrutura original. O README upstream foi mantido integralmente em `DASHBOARD_NAVIGATOR_README.md`; o README próprio do destino foi preservado e ampliado.

## Referência instalada no vault

- Caminho: `/home/val/Documentos/Notepad/.obsidian/plugins/dashboard-navigator`
- Versão declarada no manifesto: `9.1.0`
- A versão do manifesto é diferente da fonte. O hash SHA-256 de `styles.css` também difere: `438f144f177d827adc38c796f6cfe78f5e0495af046e0569f3e8893a889cfb19` na instalação e `034c17afb5536a5aa014aae4caeae6102e1bfcf982079bc372c2dff9bc310fa1` na fonte. Isso não estabelece equivalência nem diferença funcional entre os bundles.
- `data.json` é dado pessoal do vault: não foi lido, copiado ou incluído.

## Escopo e build

Os fontes, manifesto e arquivos de build são os da revisão indicada, sem alterações funcionais. O manifesto mantém identidade, autoria, versão e compatibilidade da referência. O build definido pelo projeto é `npm run build`; ele executa a checagem TypeScript e o esbuild em modo de produção para gerar `main.js`.

O repositório upstream não contém lockfile de dependências. Para não atualizar nem fixar dependências fora do escopo desta etapa, a instalação de dependências para validação foi feita sem salvar lockfile ou modificar o manifesto. Por isso, a resolução das dependências não fica integralmente fixada nesta cópia.

## Validação executada

- Ambiente: Node.js `v26.13.0`, npm `11.20.0`.
- Instalação para a validação: `npm install --ignore-scripts --no-save --no-package-lock`.
- Build: `npm run build` — concluído com sucesso; a checagem TypeScript e a geração esbuild passaram.
- O build gerou `main.js` (~197 KB), ignorado pelo Git conforme `.gitignore`; `node_modules/` também está ignorado.
- Uma comparação dos arquivos rastreados da fonte confirmou conteúdo idêntico em todos os arquivos copiados, incluindo o README upstream sob o nome `DASHBOARD_NAVIGATOR_README.md`.
- O npm reportou uma vulnerabilidade moderada entre dependências de desenvolvimento. Nenhuma dependência foi atualizada como parte desta etapa.
- O build, por si só, não valida o comportamento ou a aparência no Obsidian.

## Instalação para teste no vault

Após a validação do build, a pedido do usuário, os arquivos `main.js`, `styles.css` e `manifest.json` gerados/usados nesta distribuição foram copiados para `/home/val/Documentos/Notepad/.obsidian/plugins/dashboard-navigator`, substituindo os artefatos da versão instalada `9.1.0` pela distribuição `10.0.0`. Os hashes dos três arquivos no destino foram conferidos e coincidem com os do repositório de trabalho.

O arquivo pessoal `data.json` foi preservado e não foi lido nem copiado. O teste dentro do Obsidian ainda é necessário para validar comportamento e aparência.

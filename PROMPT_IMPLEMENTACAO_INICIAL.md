# Instrução inicial — obter o código-fonte compilável do plugin

## Objetivo

Prepare este repositório (`/home/val/Github/obsidian-simple-dashboard`) para conter o código-fonte completo e compilável do plugin Dashboard Navigator para Obsidian. Nesta etapa, a meta é obter uma base reproduzível para gerar o plugin; **não mudar funcionalidades, interface, comportamento, identidade ou arquitetura do código-fonte de referência**.

## Repositórios de referência

Use os caminhos abaixo como referências distintas e deixe clara a origem de cada arquivo:

1. **Código-fonte de referência, versão 10.0.0**  
   `/home/val/Github/dashboard-navigator-for-obsidian`

   Este é o projeto de desenvolvimento. Contém o TypeScript em `src/`, estilos, manifesto, configuração TypeScript, configuração do esbuild, scripts do npm, documentação e histórico de versões. A versão indicada em `manifest.json` e `package.json` é `10.0.0`. O commit observado na consulta inicial foi `a2b729544dd369c28eb66507a3da0faf08439d11` (`a2b7295`). Confirme o estado atual do repositório antes de copiar, para registrar a revisão efetivamente usada.

2. **Plugin atualmente instalado no vault, versão 9.1.0**  
   `/home/val/Documentos/Notepad/.obsidian/plugins/dashboard-navigator`

   Esta pasta contém os artefatos instalados (`main.js`, `styles.css`, `manifest.json`) e o arquivo `data.json`, que guarda preferências específicas daquele vault. Ela é uma referência do estado instalado, não a fonte principal para desenvolver: `main.js` é um bundle compilado e não substitui o TypeScript original.

3. **Repositório de destino**  
   `/home/val/Github/obsidian-simple-dashboard`

   Este é o repositório que deve passar a conter a cópia de trabalho do código-fonte e os arquivos necessários para compilá-lo.

## Decisão de versão para esta etapa

- Use como base do código-fonte a versão **10.0.0** do repositório de referência. Ela contém os fontes TypeScript e representa o ponto de partida compilável mais completo disponível.
- Consulte a instalação **9.1.0** para compreender o estado que está atualmente no vault e para comparar configurações ou resultados observáveis quando necessário. Não misture arquivos das versões 9.1.0 e 10.0.0 sem identificar e justificar a diferença.
- Registre no repositório de destino a revisão de origem e a versão escolhida, por exemplo em uma nota de proveniência. Não invente uma equivalência exata entre o bundle instalado e uma revisão do código-fonte se ela não tiver sido comprovada.

## Trabalho solicitado

1. Inspecione os dois locais de referência e o estado do repositório de destino antes de alterar arquivos.
2. Traga para o repositório de destino os fontes e arquivos de configuração necessários para desenvolvimento e build, preservando a estrutura existente do projeto de referência, em especial `src/`, `styles.css`, `manifest.json`, `package.json`, `tsconfig.json` e `esbuild.config.mjs`.
3. Preserve os fontes e metadados da referência sem refatoração, reescrita, limpeza oportunista ou alterações de estilo. O propósito desta etapa é disponibilizar a base compilável, não começar ainda a evolução das features.
4. Mantenha documentação e licença apropriadas, incluindo a licença MIT e os créditos/autoria originais. Acrescente uma nota de proveniência que identifique a versão e o commit efetivamente copiados.
5. **Não copie o `data.json` do vault para o projeto.** Ele contém preferências pessoais da instalação. Se for necessário estudar a compatibilidade das configurações, leia-o como referência e não o publique nem o trate como configuração padrão do plugin.
6. Não substitua `main.js` compilado por código escrito manualmente. Gere o bundle usando o processo de build já definido pelo projeto de referência. Não edite o vault durante esta etapa.
7. Não altere o identificador `dashboard-navigator`, o nome exibido, a versão, a autoria, as permissões ou a compatibilidade mínima do manifesto nesta etapa. Uma eventual mudança para uma identidade independente ou para instalação lado a lado deve ser decidida separadamente.
8. Preserve quaisquer arquivos que já existam no repositório de destino. O README inicial pode ser mantido ou ampliado sem contradizer a origem e o objetivo do projeto.

## Limites explícitos

Nesta etapa, não:

- implemente features novas ou correções;
- mude aparência, textos ou interações;
- refatore módulos ou reorganize diretórios;
- atualize dependências por iniciativa própria;
- faça downgrade para a versão instalada 9.1.0;
- copie preferências pessoais do vault;
- instale o resultado no vault, publique, faça release ou altere outro repositório;
- declare que o comportamento está validado apenas porque o bundle foi gerado.

Se encontrar uma diferença entre as referências que impeça uma cópia fiel ou um build, registre o problema e sua evidência. Não o resolva silenciosamente com uma alteração funcional.

## Critérios de conclusão

A etapa estará concluída quando:

- o repositório de destino contiver os fontes e a configuração de build necessários, preservando a organização da referência;
- a proveniência da cópia (versão e commit) estiver documentada;
- for possível executar o build definido pelo projeto e obter o bundle do plugin sem mudanças intencionais de funcionalidade;
- alterações e arquivos gerados estiverem identificados com clareza no resumo final;
- nenhuma preferência do vault tiver sido incorporada ao repositório.

No relatório final, informe a versão/commit de origem, os principais arquivos trazidos, o comando de build usado e o resultado. Separe fatos verificados de pontos que ainda precisem de comparação visual ou funcional com o Obsidian.

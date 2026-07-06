<!-- Multilanguage README.md for Eisenhower_Organizer -->

<p align="center">
  <b>Selecione o idioma / Select language:</b><br>
  <a href="#ptbr">Português (BR)</a> |
  <a href="#enus">English (US)</a>
</p>

---

## <a id="ptbr"></a>Português (BR)

> **Observação:** Este repositório refere-se à versão **v2026.7.2.1** do projeto EISENHOWER ORGANIZER. Apoie o projeto e adquira a versão paga por meio do link: [Instalar via Microsoft Store](https://apps.microsoft.com/detail/9P289X0185C3)

> **Observação:** Este repositório refere-se à versão **v2026.7.2.1** do 📚 Projeto Lúmen. Apoie o projeto e adquira a versão paga através do link: [Instalar via Microsoft Store](https://apps.microsoft.com/detail/9N70CLLMVRPN)

<details>
<summary>Clique para expandir o README em português</summary>

# EISENHOWER ORGANIZER / LÚMEN - Organizador de tarefas, estudos e foco

Versão: v2026.7.2.1<br>
Data técnica desta revisão: 2 de julho de 2026<br>
Autor: Fernando Nillsson Cidade<br>

## Resumo

EISENHOWER ORGANIZER / LÚMEN é um aplicativo desktop, desenvolvido em C++17 com Qt 6 Widgets, para organizar tarefas, estudos, foco, leitura assistida e atividades avaliativas em uma única janela. A aplicação principal funciona como host modular: o módulo Eisenhower está sempre disponível, e os módulos Feynman, Pomodoro, Mapa Mental, Audiolivro e Registro de Atividades aparecem automaticamente quando seus plugins estão presentes no ambiente de execução.

A série 2026.5.x consolidou a arquitetura por plugins, ampliou o sistema de compilação para MinGW e MSVC, adicionou os plugins Mapa Mental e Audiolivro, melhorou a persistência de preferências visuais, expandiu o menu de plugins e atualizou as notas internas exibidas na janela Sobre de acordo com os plugins efetivamente carregados.

A revisão 2026.6.13.0 acrescenta o **Registro de Atividades** como plugin opcional, com cadastro de atividades avaliativas, listas personalizadas, prioridade, nível de domínio, data, horário, cores por disciplina e integração das atividades como tarefas no Eisenhower, Pomodoro e Feynman quando a sincronização correspondente está ativa.

A revisão 2026.6.14.0 complementa a Agenda com agendas personalizadas, restauração da última agenda aberta, edição e remoção de agendas/listas, cores alternadas para agendas criadas pelo usuário e configurações próprias em `agenda_config.json`. Também reforça a estabilidade da `Lista Global de Tarefas` ao remover uma ou várias tarefas diretamente pelo calendário.

A revisão 2026.6.16.0 adiciona o **Layout Matriz 2x2** à Matriz de Eisenhower, com visualização dos quatro quadrantes ao mesmo tempo e abas internas para tarefas pendentes e concluídas. Também melhora o arraste de uma ou várias tarefas entre abas, corrige a marcação de tarefas já selecionadas pela caixa de seleção e atualiza a documentação de uso do novo recurso.

A revisão 2026.6.26.0 aprimora o **Registro de Atividades** com listas aninhadas em agendas personalizadas. Agora uma lista pode depender da escolha feita na lista anterior, permitindo montar agendas em formato de árvore, como curso, semestre e disciplina. A revisão também melhora a tradução dinâmica dos botões de diálogo da Agenda, incluindo `Sim`, `Não`, `OK` e `Cancelar`.

A revisão 2026.6.27.0 adiciona o **Gerenciador de logs** em `Ferramentas`, aprimora o **Gerenciador de plugins**, centraliza os registros do aplicativo e dos plugins nos arquivos do produto em uso e deixa as janelas auxiliares mais naturais durante a troca de idioma e alternância entre janelas. Também corrige a inicialização das versões MSVC-Ninja e reduz arquivos desnecessários nas pastas finais de distribuição.

A revisão 2026.6.30.0 melhora a remoção de tarefas pelo menu de contexto. No Eisenhower, a confirmação de `Remover Tarefa` passa a traduzir corretamente os botões `Sim` e `Não` conforme o idioma ativo. No Feynman, o menu da lista `Minhas Tarefas` permite excluir diretamente uma tarefa ou várias tarefas selecionadas, preservando o grupo quando o clique direito ocorre sobre uma tarefa já selecionada.

A revisão 2026.7.2.0 melhora o uso diário das tarefas com cores, arquivos vinculados e confirmação de edição. O Registro de Atividades passa a atualizar a cor das tarefas em tempo de execução, inclusive em tarefas antigas carregadas de versões anteriores, e permite vincular qualquer arquivo externo ao cadastro por botão ou arraste. A edição de tarefas passa a mostrar uma confirmação de sucesso no Eisenhower, Pomodoro e Feynman, e o menu `Colorir tarefas` permite aplicar uma cor manual às tarefas selecionadas.

## Funcionalidades principais

- Organização de tarefas pela Matriz de Eisenhower, com quadrantes, prioridades, nível de domínio, data, horário, descrição e arquivo vinculado.
- Calendário integrado com filtros por dia, semana, mês e ano, incluindo uma lista global de tarefas do período filtrado.
- Coloração manual de tarefas selecionadas em `Configurações -> Espaço Reservado -> Colorir tarefas`, com preservação visual nos módulos compatíveis.
- Confirmação de sucesso ao editar tarefas no Eisenhower, Pomodoro e Feynman.
- Remoção de tarefas pelo menu de contexto, com confirmação traduzida e opção `Não` como escolha inicial para reduzir exclusões acidentais.
- Exclusão de uma ou várias tarefas no Feynman pelo menu de contexto da lista `Minhas Tarefas`.
- Cadastro opcional de atividades avaliativas por curso, ementa, semestre, disciplina, turma, tipo, sequência, data, horário, prioridade, nível de domínio e arquivo vinculado quando o plugin Registro de Atividades está disponível.
- Agendas personalizadas com listas próprias e, quando desejado, listas aninhadas que filtram opções conforme a seleção anterior.
- Alternância entre layout em abas, layout em quadrantes e layout matriz 2x2 para a área Eisenhower.
- Abas de módulos com ordem persistente, bloqueio/desbloqueio de reorganização e restauração da ordem padrão.
- Contador do módulo ativo, com exibição da seleção e do total de itens da aba atual.
- Ferramentas de produtividade integradas para busca global, painel de curto prazo, recorrências em lote, lembretes locais, exportação de calendário, histórico, templates, revisões espaçadas e fluxo integrado de estudo.
- Gerenciador de plugins para conferir quais módulos opcionais foram encontrados, carregados e qual caminho foi usado.
- Gerenciador de logs para listar arquivos de log, abrir o log selecionado e acompanhar novos registros em tempo real.
- Recorrências e lembretes trabalham sobre itens unificados dos módulos disponíveis, com filtro, seleção de itens, prevenção de duplicadas, fallback de data/horário e temporizadores locais enquanto o aplicativo está aberto.
- Persistência local de tarefas, idioma, layout e preferências dos plugins no diretório do usuário.
- Interface em português (Brasil) e inglês (Estados Unidos), com recarregamento imediato dos textos.
- Importação e exportação de tarefas em JSON, CSV, XLSX e PDF, conforme o fluxo de arquivos usado pelo aplicativo.
- Janela Sobre com histórico, detalhes, avisos, licenças, política de privacidade e notas de lançamento filtradas pelos plugins disponíveis.
- Operação local sem telemetria do aplicativo. Recursos de voz e IA podem depender de ambientes de execução, modelos ou serviços configurados no ambiente.

## Módulos disponíveis

| Módulo | Disponibilidade | Função |
| --- | --- | --- |
| Eisenhower | Integrado ao host | Planejamento e acompanhamento de tarefas por importância e urgência. |
| Feynman | Plugin opcional | Estudos por conceitos, explicações simples, lacunas de entendimento e revisões. |
| Pomodoro | Plugin opcional | Execução de ciclos de foco, pausas, alarmes e acompanhamento de progresso. |
| Mapa Mental | Plugin opcional | Criação visual de conceitos conectados, importação assistida de documentos e exportação de mapas. |
| Audiolivro | Plugin opcional | Leitura assistida de texto e PDF, síntese de voz, configuração de fonte, busca e destaque durante a leitura. |
| Registro de Atividades | Plugin opcional | Cadastro de atividades avaliativas e criação de tarefas integradas ao Eisenhower, Pomodoro e Feynman. |

## Novidades técnicas da versão 2026.5.5.0

- Inclusão do plugin **Mapa Mental**, com nós conceituais, conexões, cores, notas, arquivo vinculado, backup automático, salvamento/carregamento em JSON, exportação em PNG e layouts vertical, horizontal, radial e em árvore.
- Inclusão do plugin **Audiolivro**, com editor de texto, leitor de PDF, controles de leitura, velocidade, volume, fonte, vozes, busca em texto/PDF, seleção em PDF, régua de foco e destaque sincronizado durante a fala.
- Menu **Configurações -> Plugins** expandido para centralizar a abertura dos plugins e as preferências específicas de Mapa Mental, Audiolivro, Feynman e Pomodoro.
- Sistema de abas de módulo ampliado para até cinco frentes de trabalho: Eisenhower, Pomodoro, Feynman, Mapa Mental e Audiolivro.
- Caminhos de descoberta dos plugins atualizados para localizar compilações MinGW/MSVC dentro de `build/build_*_mingw` e `build/build_*_msvc`, além dos caminhos legados mantidos por compatibilidade.
- CMake reorganizado com opções independentes para o host, Feynman, Pomodoro, Mapa Mental, Audiolivro e ferramentas auxiliares em `mocks`.
- Presets de compilação separados para MinGW e MSVC, incluindo o host, os plugins e os utilitários de tradução/desenvolvimento.
- Fluxo de implantação ajustado para copiar o ambiente de execução do Qt, traduções, plugins, drivers SQL, ambiente de execução multimídia e arquivos auxiliares dos novos plugins.
- Ferramentas de tradução centralizadas em `mocks`, substituindo utilitários duplicados dentro de módulos individuais.
- Notas de lançamento e telas Sobre agora exibem seções de Feynman, Pomodoro, Mapa Mental e Audiolivro apenas quando os respectivos plugins estão disponíveis.
- Tradução de botões padrão de diálogos corrigida para usar o contexto visual correto da interface.
- Scripts de limpeza atualizados para remover artefatos regeneráveis do novo layout de compilação.
- Instaladores e recursos institucionais atualizados para a versão 2026.5.5.0.

## Complementos funcionais da versão 2026.5.9.0

- O diálogo **Gerar próximas recorrências** permite escolher métodos de origem/destino, filtrar itens, usar todos os itens filtrados ou somente selecionados, revisar uma prévia do que será criado e restaurar padrões.
- A geração de recorrências aceita frequência padrão para itens sem regra própria, data/hora de referência para itens sem data ou horário, limite por item, prevenção de duplicadas e restauração do estado anterior da última geração.
- O diálogo **Ativar lembretes locais** permite filtrar/selecionar itens, escolher data/hora do item ou data/hora manual, definir período rápido, configurar aviso no app e/ou bandeja do sistema e cancelar lembretes ativos.
- Lembretes com a mesma data/hora são agrupados em um aviso com a lista de itens; o campo `Máximo` define quantas repetições serão disparadas para cada horário agendado.

## Complementos funcionais da versão 2026.6.13.0

- Inclusão do plugin **Registro de Atividades** em `Ferramentas -> Registro de Atividades` e `Configurações -> Plugins -> Registro de Atividades`, visível somente quando o plugin está presente.
- Janela **Cadastro de Atividades** com listas de curso, ementa, semestre, disciplina, turma, tipo de atividade, sequência, prioridade, nível de domínio, calendário, vínculo de data, vínculo de horário e botões `Registrar Definições`, `Limpar` e `Fechar`.
- Atividades registradas pela Agenda passam a ser gravadas como tarefas em `tarefas.json`, usando a pasta persistente correta do produto: `%LOCALAPPDATA%/EisenhowerOrganizer` ou `%LOCALAPPDATA%/Lumen`.
- Listas personalizadas da Agenda são salvas em `listas.db` dentro da pasta persistente do produto, evitando o uso do diretório legado da aplicação Agenda independente.
- O menu `Configurações -> Plugins -> Registro de Atividades` concentra `Excluir item` e `Cores`, com tradução dinâmica em tempo de execução.
- O modo `Cores -> Coloridas` aplica a cor da disciplina nas tarefas criadas pela Agenda no Eisenhower, no Pomodoro, no Feynman e na lista global do calendário. Quando há arquivo vinculado, o título também recebe destaque visual de vínculo.
- Textos de Sobre, notas de lançamento e manual interno usam blocos condicionais da Agenda para não mencionar o plugin quando ele não está disponível.
- Presets, tasks do VS Code, deploy e utilitários de tradução foram ampliados para compilar o plugin Registro de Atividades em MinGW e MSVC.

## Complementos funcionais da versão 2026.6.14.0

- A janela **Cadastro de Atividades** passa a permitir alternar entre o exemplo `Engenharia Civil` e agendas personalizadas criadas pelo usuário.
- O menu interno da Agenda permite criar uma nova agenda, abrir agenda, editar agenda, remover agenda, editar título de lista e remover título de lista.
- Agendas personalizadas podem conter múltiplas listas suspensas próprias, criadas progressivamente para evitar listas vazias ocupando a interface.
- A última agenda aberta é restaurada na próxima sessão: se o último uso foi `Engenharia Civil`, esse exemplo volta; se foi uma agenda personalizada, ela é reaberta.
- O menu `Configurações -> Plugins -> Registro de Atividades -> Excluir item` passa a acompanhar a agenda ativa, mostrando listas compatíveis com `Engenharia Civil` ou com a agenda personalizada aberta.
- O modo `Cores -> Coloridas` usa cores alternadas nas agendas personalizadas e evita repetir imediatamente a última cor aplicada.
- As preferências da Agenda passam a ficar em `agenda_config.json`, separadas das demais configurações do produto.
- A `Lista Global de Tarefas` ficou mais estável ao remover uma ou várias tarefas pelo menu de contexto, preservando a remoção correta no quadrante de origem.

## Complementos funcionais da versão 2026.6.16.0

- Inclusão do **Layout Matriz 2x2** em `Configurações -> Layout de Tarefas -> Interface do Usuário -> Matriz de Eisenhower`.
- O novo layout mostra os quatro quadrantes simultaneamente em duas linhas e duas colunas.
- Cada quadrante possui abas `Pendente` e `Concluídas`, facilitando acompanhar o que ainda está aberto e o que já foi finalizado.
- As abas pendentes usam a cor do quadrante; as abas concluídas usam azul para padronizar a leitura visual.
- Marcar a caixa de seleção de uma tarefa pendente move a tarefa para `Concluídas`; desmarcar uma tarefa concluída move a tarefa de volta para `Pendente`.
- O clique na caixa de seleção funciona mesmo quando a tarefa já está selecionada.
- O arraste de uma ou várias tarefas agora aceita soltar diretamente sobre abas de quadrante, `Pendente` ou `Concluídas`, ajustando o destino e o estado da tarefa.
- O manual interno e o `MANUAL.md` foram atualizados com instruções de uso do novo layout.

## Complementos funcionais da versão 2026.6.26.0

- As agendas personalizadas do **Registro de Atividades** agora podem ter listas aninhadas, permitindo criar uma sequência de escolhas dependentes.
- Ao criar uma lista depois de outra já preenchida, a Agenda pergunta se a nova lista deve ficar ligada à lista anterior.
- Quando o usuário escolhe aninhar, cada item novo da lista filha é associado a um item da lista anterior.
- Ao selecionar um item pai, a lista seguinte mostra somente os itens relacionados a ele.
- O menu `Excluir item` respeita melhor as relações entre listas, evitando que itens dependentes fiquem sem ligação válida.
- Os botões de diálogo do Registro de Atividades, como `Sim`, `Não`, `OK` e `Cancelar`, acompanham a troca de idioma em tempo de execução.
- O manual interno, o `MANUAL.md`, o `README.md` e as notas de lançamento foram atualizados com instruções sobre o novo fluxo.

## Complementos funcionais da versão 2026.6.27.0

- Inclusão do **Gerenciador de logs** em `Ferramentas -> Gerenciador de logs`, logo abaixo do Gerenciador de plugins.
- O botão `Abrir log` passou a ficar no Gerenciador de logs, junto da lista de arquivos e do monitor em tempo real.
- O monitor de logs mostra novos registros durante a execução, em ordem temporal, do registro mais antigo para o mais recente.
- Os logs do Eisenhower Organizer usam arquivos `file_eisenhower`; os logs do Lúmen usam arquivos `file_lumen`.
- O aplicativo e os plugins passam a registrar mensagens de diagnóstico de forma centralizada, incluindo carregamento de plugins, ações importantes, avisos e erros.
- As janelas **Gerenciador de plugins** e **Gerenciador de logs** acompanham a troca de idioma sem reiniciar o aplicativo.
- As janelas auxiliares podem ficar atrás da janela principal, permitindo consultar diagnósticos sem bloquear o uso normal.
- As versões MSVC-Ninja do Eisenhower Organizer e do Lúmen voltaram a inicializar corretamente depois da preparação do pacote final.
- A distribuição MSVC ficou mais enxuta, mantendo os componentes necessários e removendo arquivos opcionais que não eram usados diretamente pelo aplicativo.

## Complementos funcionais da versão 2026.6.30.0

- O menu de contexto do Eisenhower mantém a remoção de uma tarefa ou de várias tarefas selecionadas com uma confirmação mais consistente.
- Os botões da confirmação `Remover Tarefa` acompanham o idioma em tempo de execução: `Sim`/`Não` em português e `Yes`/`No` em inglês.
- A opção `Não` fica como escolha inicial na confirmação para evitar remoções acidentais.
- O Feynman ganhou as ações `Excluir Tarefa` e `Excluir Tarefas Selecionadas` no menu de contexto da lista `Minhas Tarefas`.
- Um clique direito direto em uma tarefa do Feynman seleciona aquela tarefa para exclusão individual.
- Quando várias tarefas do Feynman já estão selecionadas, clicar com o botão direito sobre qualquer uma delas preserva o grupo para exclusão em lote.
- As mensagens de confirmação, sucesso e erro do Feynman foram ajustadas para usar a palavra `tarefas` e acompanhar o idioma ativo.
- O manual interno, o `MANUAL.md`, o `README.md`, as observações do projeto e as notas de lançamento foram atualizados com instruções de uso desses fluxos.

## Complementos funcionais da versão 2026.7.2.0

- O menu `Configurações -> Espaço Reservado -> Colorir tarefas` permite escolher uma cor para uma ou várias tarefas selecionadas.
- As cores aplicadas às tarefas são preservadas no Eisenhower, no calendário, no Pomodoro e no Feynman quando os módulos estão disponíveis.
- Tarefas com arquivo vinculado mantêm o destaque visual de arquivo e preservam a cor da fonte sempre que possível.
- A janela `Editar Tarefa` mostra uma confirmação de sucesso depois que o usuário clica em `OK` e as alterações são aplicadas.
- A confirmação de edição acompanha o idioma ativo no Eisenhower, no Pomodoro e no Feynman.
- O Registro de Atividades permite vincular qualquer arquivo externo ao cadastrar uma atividade, usando o botão `Escolher...` ou arrastando o arquivo para o campo indicado.
- O arquivo vinculado passa a acompanhar a tarefa criada pela Agenda e pode ser aberto posteriormente pelas telas que exibem a tarefa.
- O modo `Cores -> Preto` do Registro de Atividades usa fonte preta no tema claro do Windows 11 e fonte branca no tema escuro.
- O modo `Cores -> Coloridas` mantém a cor definida para a atividade tanto no tema claro quanto no tema escuro.
- A troca entre `Preto` e `Coloridas` atualiza as tarefas já exibidas sem exigir reinício.
- Tarefas antigas criadas por versões anteriores ou pelo sistema antigo passam a ser tratadas ao carregar, para seguir as novas regras de cor.
- README, observações, manual interno, `MANUAL.md` e notas de lançamento foram atualizados para explicar os novos fluxos.

## Persistência local

O aplicativo usa a pasta persistente do usuário, normalmente resolvida como `%LOCALAPPDATA%/EisenhowerOrganizer` no Eisenhower Organizer e `%LOCALAPPDATA%/Lumen` no Lúmen.

Arquivos e grupos relevantes:

- `tarefas.json`: armazenamento unificado das tarefas e itens compartilhados entre Eisenhower, Feynman e Pomodoro.
- `layout.json`: preferências do layout de tarefas, painéis e abas de módulos.
- `language.json`: idioma atual.
- `recorrencias_config.json`: preferências do diálogo de geração de recorrências.
- `recorrencias_estado_original.json`: snapshot usado para restaurar o estado anterior à última geração de recorrências.
- `lembretes_locais_config.json`: preferências do diálogo de lembretes locais.
- `mapa_mental_autosave.json`: backup automático do Mapa Mental.
- `mapamental_config.json`: preferência de layout do Mapa Mental.
- Configurações do Audiolivro: voz atual, fonte, tamanho, estilo e preferências associadas.
- `listas.db`: listas personalizadas usadas pelo Registro de Atividades quando o plugin está disponível.
- `agenda_config.json`: preferência de cores do Registro de Atividades, última agenda aberta e ajustes próprios do plugin.
- `agendas/*.json`: agendas personalizadas criadas pelo usuário no plugin Registro de Atividades.
- `logs/file_eisenhower_*.log` ou `logs/file_lumen_*.log`: registros do aplicativo, dos plugins e de eventos importantes da sessão.
- Dados auxiliares de execução.

## Importação e exportação

- O Eisenhower importa e exporta tarefas pelos fluxos de arquivo disponíveis, incluindo JSON, CSV, XLSX e PDF.
- XLSX trabalha com seções/abas por quadrante e por estado de conclusão.
- PDF gera documentos com seções de quadrantes, tarefas concluídas e campos adicionais.
- O Mapa Mental salva e carrega mapas em JSON e exporta a visualização em PNG.
- O Mapa Mental importa documentos para análise em formatos como PDF, EPUB, DOC, DOCX, TXT, MD, CSV, XLSX, JSON, SQLite e XML.
- O Audiolivro abre texto e PDF, com suporte a arrastar e soltar arquivos nas áreas apropriadas.

## Solução de problemas

- Plugin não aparece:
  - compile o preset do plugin correspondente e confirme se o deploy gerou a pasta `plugins/<nome-do-plugin>` na saída esperada.
  - abra `Ferramentas -> Gerenciador de plugins` para conferir caminho, status e erro de carregamento.
  - abra `Ferramentas -> Gerenciador de logs` para acompanhar o log mais recente da sessão.
- Registro de Atividades não aparece:
  - compile `agenda-plugin-mingw-release` ou `agenda-plugin-msvc-release`, confirme o deploy de `plugins/agenda/AgendaPlugin.dll` e reinicie o host.
- Mapa Mental não processa documento por IA:
  - confirme se o runtime `llama.cpp` e o modelo configurado estão disponíveis nos caminhos esperados.
- Audiolivro não gera voz:
  - verifique a conexão, a voz selecionada, a permissão de áudio e a disponibilidade do serviço/voz usado pelo ambiente.
- Falha na importação de XLSX/PDF:
  - use arquivos estruturados de acordo com o formato esperado pelo aplicativo.
- Recorrências não geram novas ocorrências:
  - confirme métodos, filtro/seleção, regra de recorrência ou frequência padrão, período de aplicação, data/hora de referência para itens incompletos e a opção de evitar duplicadas.
- Lembretes locais não aparecem:
  - mantenha o aplicativo aberto, confira métodos, filtro/seleção, data/hora futura, aviso interno ou bandeja ativa e horário padrão para tarefas com data sem hora.
- Tarefas ou preferências não persistem:
  - verifique a permissão de escrita na pasta persistente do usuário.
- Atalhos:
  - `Ctrl+Shift+Del` limpa a sessão atual.
  - `Ctrl+Shift+L` abre o Audiolivro quando o plugin está carregado.

## Licenças, avisos e privacidade

- Disponíveis em `Opções -> Sobre`.
- Os textos são carregados dos recursos internos da aplicação.
- As seções de plugins nas notas internas são exibidas conforme os plugins efetivamente carregados no host.

## Autor

Fernando Nillsson Cidade

---

</details>

## <a id="enus"></a>English (US)

> **Note:** This repository refers to the **v2026.7.2.1** version of the EISENHOWER ORGANIZER project. Support the project and purchase the paid version through the link: [Install via Microsoft Store](https://apps.microsoft.com/detail/9P289X0185C3)

> **Note:** This repository refers to the **v2026.7.2.1** version of the 📚 Lúmen Project. Support the project and purchase the paid version through the link: [Instalar via Microsoft Store](https://apps.microsoft.com/detail/9N70CLLMVRPN)

<details>
<summary>Click to expand the README in English</summary>

# EISENHOWER ORGANIZER / LÚMEN - Task, study, and focus organizer

Version: v2026.7.2.1<br>
Technical revision date: July 2, 2026<br>
Author: Fernando Nillsson Cidade<br>

## Summary

EISENHOWER ORGANIZER / LÚMEN is a C++17 desktop application built with Qt 6 Widgets for managing tasks, study workflows, focus sessions, assisted reading, and assessment activities in one window. The main application works as a modular host: Eisenhower is always available, while Feynman, Pomodoro, Mind Map, Audiobook, and Activity Registration are loaded automatically when their plugins are present at runtime.

The 2026.5.x series consolidated the plugin architecture, expanded the build system for MinGW and MSVC, added the Mind Map and Audiobook plugins, improved visual preference persistence, expanded the plugin menu, and updated the internal release notes shown in the About window based on the plugins that are actually loaded.

Revision 2026.6.13.0 adds the **Activity Registration** as an optional plugin, with assessment-activity registration, custom lists, priority, mastery level, date, time, subject-based colors, and integration of those activities as tasks in Eisenhower, Pomodoro, and Feynman when the corresponding synchronization is active.

Revision 2026.6.14.0 complements Activity Registration with custom agendas, restoration of the last opened agenda, agenda/list editing and removal, alternating colors for user-created agendas, and dedicated settings in `agenda_config.json`. It also improves the stability of the `Global Task List` when removing one or more tasks directly from the calendar.

Revision 2026.6.16.0 adds the **2x2 Matrix Layout** to the Eisenhower Matrix, with all four quadrants visible at the same time and internal tabs for pending and completed tasks. It also improves dragging one or multiple tasks between tabs, fixes checkbox handling on already selected tasks, and updates the user documentation for the new feature.

Revision 2026.6.26.0 improves **Activity Registration** with nested lists in custom agendas. A list can now depend on the previous list, allowing tree-like agendas such as course, semester, and subject. This revision also improves runtime translation for Activity Registration dialog buttons, including `Yes`, `No`, `OK`, and `Cancel`.

Revision 2026.6.27.0 adds the **Log Manager** under `Tools`, improves the **Plugin Manager**, centralizes application and plugin records in the active product log files, and makes auxiliary windows behave more naturally during language changes and window switching. It also fixes startup for MSVC-Ninja builds and reduces unnecessary files in final distribution folders.

Revision 2026.6.30.0 improves task removal from context menus. In Eisenhower, the `Remove Task` confirmation now correctly translates the `Yes` and `No` buttons according to the active language. In Feynman, the `My Tasks` list menu can delete one task directly or delete multiple selected tasks while keeping the group when right-clicking an already selected task.

Revision 2026.7.2.0 improves daily task use with colors, linked files, and edit confirmation. Activity Registration now updates task colors at runtime, including older tasks loaded from previous versions, and lets users link any external file to a registration through a button or drag and drop. Task editing now shows a success confirmation in Eisenhower, Pomodoro, and Feynman, and the `Color Tasks` menu applies a manual color to selected tasks.

## Key features

- Eisenhower Matrix task management with quadrants, priority, mastery level, date, time, description, and linked file.
- Integrated calendar with day, week, month, and year filters, including a global task list for the selected period.
- Manual coloring of selected tasks under `Settings -> Reserved Space -> Color Tasks`, with visual preservation in compatible modules.
- Success confirmation when editing tasks in Eisenhower, Pomodoro, and Feynman.
- Task removal from the context menu, with translated confirmation and `No` as the initial choice to reduce accidental deletion.
- Deletion of one or multiple Feynman tasks from the `My Tasks` context menu.
- Optional assessment-activity registration by course, syllabus, semester, subject, class, activity type, sequence, date, time, priority, mastery level, and linked file when the Activity Registration plugin is available.
- Custom agendas with user-defined lists and, when desired, nested lists that filter options according to the previous selection.
- Switchable tabbed, quadrant, and 2x2 matrix layouts for the Eisenhower task area.
- Module tabs with persistent order, lock/unlock control, and default order restore.
- Active-module counter showing selected and total items in the current tab.
- Integrated productivity tools for global search, near-term review, batch recurrences, local reminders, calendar export, history, templates, spaced reviews, and integrated study flow.
- Plugin Manager to check which optional modules were found, loaded, and which path was used.
- Log Manager to list log files, open the selected log, and follow new records in real time.
- Recurrences and reminders work over unified items from available modules, with filtering, item selection, duplicate prevention, date/time fallback, and local timers while the application is open.
- Local persistence for tasks, language, layout, and plugin preferences in the user directory.
- Portuguese (Brazil) and English (United States) interface, with immediate text refresh.
- Task import/export in JSON, CSV, XLSX, and PDF depending on the file workflow used by the application.
- About window with history, details, notices, licenses, privacy policy, and release notes filtered by available plugins.
- Local application operation with no app telemetry. Voice and AI features may depend on runtimes, models, or services configured in the environment.

## Available modules

| Module | Availability | Purpose |
| --- | --- | --- |
| Eisenhower | Built into the host | Task planning and tracking by importance and urgency. |
| Feynman | Optional plugin | Study concepts, simple explanations, knowledge gaps, and reviews. |
| Pomodoro | Optional plugin | Focus cycles, breaks, alarms, and progress tracking. |
| Mind Map | Optional plugin | Visual connected concepts, assisted document import, and map export. |
| Audiobook | Optional plugin | Assisted text/PDF reading, text-to-speech, font settings, search, and reading highlight. |
| Activity Registration | Optional plugin | Assessment-activity registration and task creation integrated with Eisenhower, Pomodoro, and Feynman. |

## Technical changes in version 2026.5.5.0

- Added the **Mind Map** plugin with concept nodes, connections, colors, notes, linked files, automatic backup, JSON save/load, PNG export, and vertical, horizontal, radial, and tree layouts.
- Added the **Audiobook** plugin with text editor, PDF reader, playback controls, speed, volume, font settings, voice selection, text/PDF search, PDF text selection, focus ruler, and synchronized speech highlighting.
- Expanded **Settings -> Plugins** to centralize plugin launching and preferences for Mind Map, Audiobook, Feynman, and Pomodoro.
- Extended module tabs to up to five work areas: Eisenhower, Pomodoro, Feynman, Mind Map, and Audiobook.
- Updated plugin discovery paths to locate MinGW/MSVC builds under `build/build_*_mingw` and `build/build_*_msvc`, while keeping legacy paths for compatibility.
- Reworked CMake with independent options for the host, Feynman, Pomodoro, Mind Map, Audiobook, and `mocks` utility tools.
- Added separate MinGW and MSVC presets for the host, plugins, and translation/development utilities.
- Adjusted deployment to copy the Qt runtime, translations, plugins, SQL drivers, multimedia runtime, and auxiliary files required by the new plugins.
- Centralized translation utilities under `mocks`, replacing duplicated tools inside individual modules.
- Release notes and About screens now show Feynman, Pomodoro, Mind Map, and Audiobook sections only when the corresponding plugins are available.
- Fixed standard dialog button translation to use the correct interface context.
- Updated cleanup scripts for the new generated-build layout.
- Updated installers and institutional assets to version 2026.5.5.0.

## Functional additions in version 2026.5.9.0

- The **Generate Next Recurrences** dialog lets you choose source/destination methods, filter items, use all filtered items or only selected items, preview what will be created, and restore defaults.
- Recurrence generation supports a default frequency for items without their own rule, reference date/time for items without a date or time, per-item limits, duplicate prevention, and restoration of the state before the latest generation.
- The **Enable Local Reminders** dialog lets you filter/select items, choose item date/time or a manual date/time, set a quick period, configure in-app and/or system-tray alerts, and cancel active reminders.
- Reminders with the same date/time are grouped into one alert with the item list; the `Maximum` field defines how many repeated alerts fire for each scheduled time.

## Functional additions in version 2026.6.13.0

- Added the **Activity Registration** plugin under `Tools -> Activity Registration` and `Settings -> Plugins -> Activity Registration`, visible only when the plugin is present.
- The **Activity Registration** window now includes lists for course, syllabus, semester, subject, class, activity type, sequence, priority, mastery level, calendar, date linking, time linking, and the `Register Definitions`, `Clear`, and `Close` buttons.
- Activities registered through Activity Registration are stored as tasks in `tarefas.json`, using the correct product persistent folder: `%LOCALAPPDATA%/EisenhowerOrganizer` or `%LOCALAPPDATA%/Lumen`.
- Custom Activity Registration lists are stored in `listas.db` inside the product persistent folder, avoiding the legacy standalone Activity Registration directory.
- `Settings -> Plugins -> Activity Registration` centralizes `Delete item` and `Colors`, with dynamic runtime translation.
- `Colors -> Colored` applies the subject color to tasks created by Activity Registration in Eisenhower, Pomodoro, Feynman, and the calendar global list. When a linked file exists, the title also receives linked-file visual emphasis.
- About texts, release notes, and the internal manual use conditional Activity Registration blocks so the plugin is not mentioned when it is not available.
- Presets, VS Code tasks, deployment, and translation utilities were expanded to build the Activity Registration plugin with MinGW and MSVC.

## Functional additions in version 2026.6.14.0

- The **Activity Registration** window can now switch between the `Civil Engineering` example and custom agendas created by the user.
- The internal Schedule menu lets users create a new agenda, open an agenda, edit an agenda, remove an agenda, edit a list title, and remove a list title.
- Custom agendas can contain multiple user-defined drop-down lists, created progressively so unused empty lists do not fill the interface.
- The last opened agenda is restored in the next session: if the latest agenda was `Civil Engineering`, that example returns; if it was a custom agenda, it is reopened.
- `Settings -> Plugins -> Activity Registration -> Delete item` now follows the active agenda, showing lists compatible with `Civil Engineering` or with the open custom agenda.
- `Colors -> Colored` uses alternating colors for custom agendas and avoids immediately repeating the latest applied color.
- Activity Registration preferences are now stored in `agenda_config.json`, separated from the product's other settings.
- The `Global Task List` is more stable when removing one or more tasks through the context menu, preserving correct removal in the source quadrant.

## Functional additions in version 2026.6.16.0

- Added the **2x2 Matrix Layout** under `Settings -> Task Layout -> User Interface -> Eisenhower Matrix`.
- The new layout shows all four quadrants at the same time in two rows and two columns.
- Each quadrant has `Pending` and `Completed` tabs, making it easier to follow what is still open and what has already been finished.
- Pending tabs use the quadrant color; completed tabs use blue for consistent visual reading.
- Checking a pending task moves it to `Completed`; unchecking a completed task moves it back to `Pending`.
- Clicking a checkbox works even when the task is already selected.
- Dragging one or multiple tasks now supports dropping directly onto quadrant tabs, `Pending`, or `Completed`, updating the destination and task state.
- The internal manual and `MANUAL.md` were updated with instructions for using the new layout.

## Functional additions in version 2026.6.26.0

- Custom agendas in **Activity Registration** can now use nested lists, creating a sequence of dependent choices.
- When a list is created after a previous list that already has items, Activity Registration asks whether the new list should be linked to the previous one.
- When nesting is enabled, each new child-list item is assigned to an item from the previous list.
- Selecting a parent item filters the next list so it shows only related items.
- The `Delete item` menu better respects list relationships, avoiding dependent items without a valid link.
- Activity Registration dialog buttons such as `Yes`, `No`, `OK`, and `Cancel` now follow runtime language changes.
- The internal manual, `MANUAL.md`, `README.md`, and release notes were updated with instructions for the new flow.

## Functional additions in version 2026.6.27.0

- Added **Log Manager** under `Tools -> Log Manager`, directly below Plugin Manager.
- The `Open log` action now belongs to Log Manager, together with the file list and real-time monitor.
- The log monitor shows new records while the application is running, in chronological order from oldest to newest.
- Eisenhower Organizer logs use `file_eisenhower`; Lúmen logs use `file_lumen`.
- The application and plugins now record diagnostics centrally, including plugin loading, important actions, warnings, and errors.
- **Plugin Manager** and **Log Manager** follow language changes without restarting the application.
- Auxiliary windows can move behind the main window, allowing diagnostics to stay open without blocking regular use.
- MSVC-Ninja builds of Eisenhower Organizer and Lúmen now start correctly after final package preparation.
- The MSVC distribution is leaner, keeping required components and removing optional files not directly used by the application.

## Functional additions in version 2026.6.30.0

- The Eisenhower context menu keeps removal of one task or multiple selected tasks with a more consistent confirmation.
- The `Remove Task` confirmation buttons follow the runtime language: `Sim`/`Não` in Portuguese and `Yes`/`No` in English.
- `No` is the initial confirmation choice to reduce accidental removals.
- Feynman now includes `Delete Task` and `Delete Selected Tasks` actions in the `My Tasks` context menu.
- Right-clicking directly on a Feynman task selects that task for individual deletion.
- When multiple Feynman tasks are already selected, right-clicking any selected task keeps the group for batch deletion.
- Feynman confirmation, success, and error messages now use task wording and follow the active language.
- The internal manual, `MANUAL.md`, `README.md`, project notes, and release notes were updated with usage instructions for these flows.

## Functional additions in version 2026.7.2.0

- `Settings -> Reserved Space -> Color Tasks` lets users choose a color for one or more selected tasks.
- Applied task colors are preserved in Eisenhower, calendar views, Pomodoro, and Feynman when those modules are available.
- Tasks with linked files keep their linked-file visual emphasis while preserving the font color whenever possible.
- The `Edit Task` window shows a success confirmation after the user clicks `OK` and the changes are applied.
- The edit confirmation follows the active language in Eisenhower, Pomodoro, and Feynman.
- Activity Registration can link any external file while registering an activity, using `Choose...` or dragging the file onto the indicated field.
- The linked file follows the task created by Activity Registration and can be opened later from screens that display the task.
- Activity Registration `Colors -> Black` uses black font in the Windows 11 light theme and white font in the dark theme.
- Activity Registration `Colors -> Colored` keeps the defined activity color in both light and dark themes.
- Switching between `Black` and `Colored` updates already displayed tasks without requiring a restart.
- Older tasks created by previous versions or by the old system are handled when loaded, so they follow the new color rules.
- README, project notes, internal manual, `MANUAL.md`, and release notes were updated to explain the new workflows.

## Local persistence

The application uses the user's persistent folder, normally resolved as `%LOCALAPPDATA%/EisenhowerOrganizer` for Eisenhower Organizer and `%LOCALAPPDATA%/Lumen` for Lúmen.

Relevant files and groups:

- `tarefas.json`: unified storage for tasks and shared items across Eisenhower, Feynman, and Pomodoro.
- `layout.json`: task layout, panels, and module tab preferences.
- `language.json`: current language.
- `recorrencias_config.json`: Generate Next Recurrences dialog preferences.
- `recorrencias_estado_original.json`: snapshot used to restore the state before the latest recurrence generation.
- `lembretes_locais_config.json`: Local Reminders dialog preferences.
- `mapa_mental_autosave.json`: Mind Map automatic backup.
- `mapamental_config.json`: Mind Map layout preference.
- Audiobook settings: current voice, font, size, style, and related preferences.
- `listas.db`: custom lists used by Activity Registration when the plugin is available.
- `agenda_config.json`: Activity Registration color preference, last opened agenda, and plugin-specific settings.
- `agendas/*.json`: custom agendas created by the user in the Activity Registration plugin.
- `logs/file_eisenhower_*.log` or `logs/file_lumen_*.log`: application, plugin, and important session records.
- Runtime support data.

## Import and export

- Eisenhower imports/exports tasks through the available file flows, including JSON, CSV, XLSX, and PDF.
- XLSX uses sections/sheets by quadrant and completion state.
- PDF generates documents with quadrant sections, completed tasks, and additional fields.
- Mind Map saves/loads maps as JSON and exports the visual map as PNG.
- Mind Map imports documents for analysis in formats such as PDF, EPUB, DOC, DOCX, TXT, MD, CSV, XLSX, JSON, SQLite, and XML.
- Audiobook opens text and PDF, including drag-and-drop support for the appropriate areas.

## Troubleshooting

- Plugin is not visible:
  - build the matching plugin preset and confirm that deployment generated `plugins/<plugin-name>` in the expected output.
  - open `Tools -> Plugin Manager` to check path, status, and load error.
  - open `Tools -> Log Manager` to follow the latest session log.
- Activity Registration is not visible:
  - build `agenda-plugin-mingw-release` or `agenda-plugin-msvc-release`, confirm deployment of `plugins/agenda/AgendaPlugin.dll`, and restart the host.
- Mind Map cannot process a document with AI:
  - confirm that the `llama.cpp` runtime and configured model are available in the expected paths.
- Audiobook does not generate speech:
  - check connectivity, selected voice, audio permissions, and the service/voice available in the environment.
- XLSX/PDF import fails:
  - use files structured according to the expected application format.
- Recurrences do not generate new occurrences:
  - confirm methods, filter/selection, recurrence rule or default frequency, application period, reference date/time for incomplete items, and duplicate prevention.
- Local reminders do not appear:
  - keep the application open and check methods, filter/selection, future date/time, active in-app or tray alert, and default time for dated tasks without a time.
- Tasks or preferences are not persisted:
  - check write permissions in the user's persistent folder.
- Shortcuts:
  - `Ctrl+Shift+Del` clears the current session.
  - `Ctrl+Shift+L` opens Audiobook when that plugin is loaded.

## Licenses, notices, and privacy

- Available under `Options -> About`.
- Text is loaded from internal application assets.
- Plugin sections in internal release notes are displayed according to the plugins actually loaded by the host.

## Author

Fernando Nillsson Cidade

---

</details>

# Engenharia Civil — Matriz 636

Mapa interativo das disciplinas obrigatórias de Engenharia Civil da UTFPR, Campus Pato Branco. Os componentes são organizados por período e conectados pelas suas cadeias de pré-requisitos conforme a Matriz 636.

## Visão geral

| Informação | Conteúdo da versão atual |
| --- | --- |
| Matriz curricular | 636 |
| Períodos | 10 |
| Componentes obrigatórios | 62 |
| Carga horária dos componentes exibidos | 3.660 horas |

## Funcionalidades

- Mapa mental com o período no centro e as disciplinas conectadas ao redor.
- Navegação individual pelos dez períodos e opção **Todos os períodos**.
- Seleção de uma disciplina para visualizar seus pré-requisitos e os componentes que dependem dela, direta ou indiretamente.
- Conexões entre disciplinas de diferentes períodos, com setas indicando a direção da dependência.
- Painel com código, nome, período, carga horária e quantidade de componentes nas cadeias anterior e posterior.
- Consulta das conexões diretas e navegação entre elas.
- Zoom por botões, roda do mouse e gesto de pinça, além de movimentação por arraste.
- Modo claro e modo escuro, com armazenamento da preferência no navegador.
- Layout responsivo para celular e notebook, sem barra de rolagem horizontal no mapa.
- Navegação por teclado e respeito à preferência por movimento reduzido.

## Tecnologias

| Tecnologia | Uso |
| --- | --- |
| HTML | Estrutura da página, controles e informações das disciplinas |
| CSS | Paleta de cores, temas, tipografia e adaptação às telas |
| JavaScript puro | Organização do mapa, seleção, cálculo das cadeias e navegação |
| SVG | Linhas, setas e ícones |
| Pointer Events | Arraste com mouse, movimentação por toque e pinça |
| ResizeObserver | Ajuste do mapa quando sua área muda de tamanho |
| localStorage | Persistência da escolha entre tema claro e escuro |

## Como executar

É necessário um navegador atualizado com JavaScript habilitado. Não é preciso instalar pacotes, executar uma compilação ou configurar um banco de dados.

1. Baixe o HTML do projeto. O arquivo entregue pode estar nomeado como `index.html`.
2. Abra `index.html` no navegador.

O mapa funciona localmente, sem internet. O acesso ao PDF da matriz oficial pelo link do rodapé depende de conexão.

## Como usar

1. Escolha um período pelos botões de **1º** a **10º**. A visualização inicial apresenta o primeiro período.
2. Clique ou toque em uma disciplina para abrir sua cadeia de relações entre os períodos.
3. Use os controles de zoom e arraste o mapa para explorar as conexões.
4. Consulte o painel abaixo do mapa para ver os detalhes e as quantidades de componentes relacionados.
5. Expanda **Ver conexões diretas** para consultar os pré-requisitos imediatos e as dependências imediatas. Clique em um desses componentes para explorar sua cadeia.

Na visualização de uma cadeia, aparecem apenas as disciplinas relacionadas à seleção. O centro de cada período mantém o total de componentes e de horas daquele período; a etiqueta **n nesta cadeia** informa quantos componentes estão sendo exibidos naquele grupo.

Escolher outro período ou **Todos os períodos** limpa a seleção. Clicar novamente na disciplina selecionada também retorna à visualização do período dela.

### Legenda

| Destaque | Significado |
| --- | --- |
| Âmbar — Cadeia anterior | Pré-requisitos diretos e indiretos da disciplina selecionada |
| Amarelo — Selecionada | Disciplina que está sendo analisada |
| Verde — Cadeia posterior | Componentes que dependem da disciplina selecionada, direta ou indiretamente |

As setas partem do pré-requisito e apontam para a disciplina que o exige. Um componente na cadeia posterior pode exigir outros pré-requisitos além da disciplina selecionada.

### Controles

| Ação ou controle | Resultado |
| --- | --- |
| Botão `+` | Aumenta o zoom |
| Botão `−` | Diminui o zoom |
| Botão com a porcentagem | Define o zoom em 100% |
| Botão **Enquadrar mapa** | Ajusta a visualização ao mapa atual |
| Roda do mouse sobre o mapa | Aproxima ou afasta a região sob o ponteiro |
| Arrastar com o mouse ou com um dedo | Move o mapa |
| Gesto de pinça com dois dedos | Altera o zoom no celular |
| Duplo clique em uma área livre | Aproxima a região clicada |
| **Focar disciplina** | Aproxima a disciplina selecionada |
| **Ver cadeia completa** | Enquadra a cadeia da seleção atual |
| **Limpar seleção** | Retorna ao período da disciplina selecionada |

O zoom varia de **12% a 250%**. Em celulares, os grupos usam uma organização mais estreita; períodos com muitas disciplinas podem ser explorados movendo o mapa na vertical.

### Atalhos de teclado

Com o foco no mapa:

| Tecla | Ação |
| --- | --- |
| `+` ou `=` | Aumentar o zoom |
| `-` | Diminuir o zoom |
| `0` | Enquadrar o mapa |
| Setas direcionais | Mover o mapa |

Use `Tab` para navegar pelos controles e disciplinas, e `Enter` ou espaço para ativar um botão. A tecla `Esc` limpa a seleção atual.

## Referência curricular

O rodapé do projeto contém o link para a [Matriz 636 de Engenharia Civil — UTFPR, Campus Pato Branco](https://www.utfpr.edu.br/cursos/coordenacoes/graduacao/pato-branco/pb-engenharia-civil/documentos/matrizes-curriculares-636.pdf/@@download/file).

Os dados estão incorporados ao HTML e não são atualizados automaticamente. O mapa não inclui as disciplinas optativas dos grupos 785 e 786 nem os registros de ENADE.

# Mapa Civil UTFPR-PB — Matriz 636

Mapa curricular interativo e responsivo da Engenharia Civil da UTFPR-PB — Matriz 636, com disciplinas obrigatórias e cadeias de pré-requisitos.

O projeto ajuda a visualizar o percurso acadêmico: ao selecionar uma disciplina, o mapa destaca todos os seus pré-requisitos diretos e indiretos, além dos componentes que dependem dela nos períodos seguintes.

> Projeto independente, sem vínculo institucional com a UTFPR. O mapa é uma ferramenta de consulta e não substitui a matriz oficial, os regulamentos acadêmicos ou a orientação da coordenação do curso.

## Escopo

- **Campus:** Pato Branco.
- **Curso:** Engenharia Civil.
- **Matriz curricular:** 636 — Engenharia Civil 2023.
- **Componentes obrigatórios representados:** 62.
- **Carga horária representada:** 3.660 horas.
- **Organização:** 10 períodos.

A contagem inclui estágio, atividades complementares e trabalhos de conclusão de curso. Não inclui as optativas dos grupos 785 e 786, os registros de ENADE ou equivalências de outras matrizes. As 3.660 horas correspondem aos componentes obrigatórios representados, não à totalidade dos requisitos para concluir o curso.

## Funcionalidades

- Visualização das disciplinas por período, com código e carga horária.
- Destaque de toda a cadeia anterior de pré-requisitos.
- Destaque dos componentes que dependem direta ou indiretamente da disciplina selecionada.
- Contadores das disciplinas anteriores e posteriores na cadeia.
- Limpeza da seleção pelo botão **Limpar** ou ao selecionar novamente o mesmo cartão.
- Navegação por mouse, toque e teclado.
- Interface responsiva para computador, tablet e celular.

Em telas maiores, os períodos aparecem em colunas com linhas de conexão e rolagem horizontal. Em telas de até 900 px, os períodos ficam empilhados, as linhas são ocultadas e o resumo da seleção aparece na parte inferior da tela. Os destaques continuam funcionando.

## Como usar

1. Abra o mapa no navegador.
2. Clique ou toque em uma disciplina.
3. Observe os destaques conforme a legenda:

| Cor | Significado |
| --- | --- |
| Amarelo | Pré-requisitos diretos e indiretos da disciplina selecionada. |
| Roxo | Disciplina selecionada. |
| Verde | Componentes que dependem direta ou indiretamente dela. |

Para navegar pelo teclado, use **Tab** para focar os cartões e **Enter** ou **Espaço** para selecioná-los.

> **Sobre “libera depois”:** o destaque indica uma relação de dependência curricular, não uma autorização automática de matrícula. Uma disciplina pode exigir outros pré-requisitos e estar sujeita a regras adicionais, oferta de turmas e disponibilidade de vagas.

## Executar localmente

Baixe o arquivo `index.html` e abra-o diretamente em um navegador moderno.

Não é necessário instalar Python, Node.js, pacotes ou um servidor. HTML, CSS, JavaScript e dados estão reunidos no próprio arquivo. O mapa funciona sem internet após o download; apenas o acesso à fonte oficial exige conexão.

## Publicar no GitHub Pages

1. Crie um repositório chamado `mapa-civil-utfpr-pb`.
2. Envie `index.html` e `README.md` para a raiz do repositório.
3. Abra **Settings → Pages**.
4. Em **Build and deployment → Source**, selecione **Deploy from a branch**.
5. Em **Branch**, selecione `main` e a pasta `/(root)`. Se sua branch principal tiver outro nome, selecione-a.
6. Clique em **Save**.
7. Aguarde a publicação e abra o endereço exibido na seção **Pages**.

Mantenha o nome `index.html` em letras minúsculas para que o arquivo seja reconhecido como a página inicial. No plano gratuito do GitHub, utilize um repositório público para disponibilizar o site pelo Pages.

Para atualizar a página, substitua o `index.html` na mesma branch e pasta configuradas. O GitHub Pages publicará a nova versão após processar a alteração.

## Estrutura e tecnologias

| Arquivo | Responsabilidade |
| --- | --- |
| `index.html` | Interface, estilos, dados curriculares e lógica de interação. |
| `README.md` | Apresentação e instruções de uso e publicação. |

O projeto utiliza **HTML5**, **CSS3**, **JavaScript puro** e **SVG** para as conexões. Não usa frameworks, bibliotecas externas ou serviços de backend.

## Atualizar os dados curriculares

Os dados estão no array `COURSES`, dentro do `index.html`. Cada componente informa:

| Campo | Conteúdo |
| --- | --- |
| `code` | Código único da disciplina na matriz. |
| `name` | Nome da disciplina. |
| `period` | Período indicado na matriz. |
| `hours` | Carga horária em horas. |
| `type` | Categoria visual utilizada pelo cartão. |
| `prerequisites` | Lista dos códigos dos pré-requisitos diretos. |

As cadeias indiretas e as conexões são calculadas automaticamente a partir de `prerequisites`. Todos os códigos referenciados precisam existir no array.

Antes de modificar os dados, confira a fonte oficial. Caso altere a quantidade de componentes ou a carga horária, revise também os números do cabeçalho, deste README e as validações de 62 componentes e 3.660 horas presentes no JavaScript.

Os dados são estáticos: mudanças no documento da universidade não atualizam o mapa automaticamente. Pré-requisitos ausentes na fonte não devem ser inferidos apenas pelo nome ou pela numeração de uma disciplina.

## Fonte

[Matriz Curricular 636 — Engenharia Civil, UTFPR Campus Pato Branco (PDF oficial)](https://www.utfpr.edu.br/cursos/coordenacoes/graduacao/pato-branco/pb-engenharia-civil/documentos/matrizes-curriculares-636.pdf/@@download/file)


---
title: Como contribuir
description: Como escrever e editar páginas desta documentação.
---

Toda página é um arquivo Markdown no repositório de conteúdo. Para corrigir algo, use o link **Editar no GitHub** no fim de qualquer página.

## Estrutura

- Cada área é uma pasta dentro de `docs`.
- O arquivo `meta.json` de cada pasta define o título e a ordem das páginas no menu.
- O começo de cada arquivo define o título e a descrição da página:

```md
---
title: Ligar o sistema de som
description: Checklist para deixar tudo pronto antes do culto.
---
```

## Publicação

- Mudanças na branch `main` aparecem no site em segundos.
- Para revisar antes de publicar, crie uma branch e abra `/preview/nome-da-branch` no site.
- Depois de publicar, abra a página no site e confira se ficou como esperado.

## Componentes

Além do Markdown comum, estes componentes estão disponíveis. Deixe uma linha em branco entre a tag e o conteúdo.

### Aviso

```md
<Callout type="warn" title="Atenção">
Texto do aviso.
</Callout>
```

Tipos: `info`, `warn`, `error`, `success` e `idea`.

### Passos

```md
<Steps>
<Step>

### Primeiro passo

Texto.

</Step>
</Steps>
```

### Abas

```md
<Tabs>
<Tab title="Domingo">

Texto.

</Tab>
<Tab title="Eventos">

Texto.

</Tab>
</Tabs>
```

### Checklist

Os itens podem ser marcados e o progresso fica salvo no aparelho de quem está usando. O `id` diferencia checklists na mesma página.

```md
<Checklist id="ligar">

- [ ] Primeiro item
- [ ] Segundo item

</Checklist>
```

### Vídeo do YouTube

Use o código que aparece no endereço do vídeo, depois de `v=`.

```md
<YouTube id="codigo-do-video" title="Título do vídeo" />
```

### Imagens

Coloque a imagem em uma pasta `img` ao lado da página e use um caminho relativo:

```md
![Painel traseiro da mesa](./img/painel-traseiro.jpg)
```

## Cuidados

- Se o título ou a descrição tiver dois-pontos, coloque o texto entre aspas, como em `description: "Do apoio à liderança: como crescer"`. Sem as aspas, o começo do arquivo aparece como texto na página.
- Os caracteres `<` e `{` têm significado especial. Para usá-los no texto, coloque-os entre crases, como em `` `<` ``.
- Nunca escreva senhas, chaves de transmissão ou outros segredos: este conteúdo é público.

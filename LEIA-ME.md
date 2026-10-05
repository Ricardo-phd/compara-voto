# Compara Voto: como colocar no ar em comparavoto.com.br

Arquivos desta pasta:

- `index.html`: o site inteiro (dados, fotos e QR Code já estão dentro dele)
- `favicon.svg`: ícone da aba do navegador (a urna)
- `icon-180.png`: ícone para quem salvar o site na tela inicial do celular
- `og-image.png`: imagem de prévia quando o link é compartilhado no WhatsApp e nas redes
- `.nojekyll`: arquivo vazio que evita que o GitHub processe o site (não apague)

O site já está configurado para o endereço https://comparavoto.com.br.

## 1. Registrar o domínio

1. Entre em registro.br, pesquise `comparavoto.com.br` e registre com seu CPF.
2. Deixe o DNS no próprio Registro.br (opção "Utilizar os servidores DNS do Registro.br").

## 2. Criar o repositório no GitHub

1. Em github.com, clique em **New repository**.
2. Nome: `compara-voto`. Deixe **Public**.
3. Clique em **Create repository**.
4. Clique em **uploading an existing file** e arraste todos os arquivos desta pasta, inclusive o `.nojekyll`.
   (No Windows ele pode ficar oculto. Se não aparecer, crie no GitHub: **Add file > Create new file**, nome `.nojekyll`, conteúdo vazio.)
5. Clique em **Commit changes**.

## 3. Ligar o GitHub Pages

1. No repositório, vá em **Settings > Pages**.
2. Em **Source**, escolha **Deploy from a branch**. Branch `main`, pasta `/ (root)`. Clique em **Save**.
3. Em **Custom domain**, digite `comparavoto.com.br` e clique em **Save**.

## 4. Apontar o domínio para o GitHub (no Registro.br)

No painel do domínio no Registro.br, em **DNS > Editar zona**, crie:

| Tipo  | Nome | Valor                      |
|-------|------|----------------------------|
| A     | (em branco) | 185.199.108.153     |
| A     | (em branco) | 185.199.109.153     |
| A     | (em branco) | 185.199.110.153     |
| A     | (em branco) | 185.199.111.153     |
| CNAME | www  | SEU-USUARIO.github.io      |

Troque `SEU-USUARIO` pelo seu usuário do GitHub. Salve.

A propagação leva de alguns minutos a algumas horas. Quando o GitHub mostrar o domínio como verificado em **Settings > Pages**, marque **Enforce HTTPS** (o cadeado). Pode levar até uma hora para essa opção ficar disponível.

## 5. Testar antes de divulgar

- Abra https://comparavoto.com.br no celular e teste: Comparar, Quiz, Candidatos, Faltei e Apoie.
- Faça um Pix de R$ 1,00 pelo QR Code da página Apoie.
- Envie um pedido de correção pelo link de um resumo e confira se chega no Google Forms.
- Cole o link numa conversa do WhatsApp para ver a prévia com a imagem.

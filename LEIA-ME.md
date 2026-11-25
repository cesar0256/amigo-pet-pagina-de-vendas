# Página de vendas do AmigoPet: pasta pronta para publicar

Esta pasta já está configurada com o link de compra da Greenn. É só publicar num endereço público.

## O que tem na pasta

| Arquivo | Para que serve |
|---|---|
| `index.html` | A página de vendas |
| `termos.html` | Termos de Uso (link no rodapé da página) |
| `privacidade.html` | Política de Privacidade (link no rodapé da página) |
| `legal-config.js` | Dados da sua empresa e o e-mail de suporte, usados nos Termos e na Política |
| `icon-192.png` | Ícone das páginas de Termos e Privacidade |

## Como cada peça se encaixa

- **Página de vendas:** fica no seu endereço, publicada por você (passos abaixo).
- **Checkout:** fica na Greenn. Os botões "Quero organizar a vida do meu pet por R$ 27,00" já levam para `https://payfast.greenn.com.br/redirect/825782`.
- **App:** fica no endereço onde você já hospedou o AmigoPet. A Greenn entrega esse link ao cliente depois da compra.

## Passo 1: preencher os dados da empresa

Abra o `legal-config.js` num editor de texto e troque os campos entre colchetes:

```
EMPRESA: '[NOME DA EMPRESA]',
CNPJ: '[CNPJ]',
PLATAFORMA: 'Greenn',
DPO: '[NOME DO ENCARREGADO PELOS DADOS]',   // pode ser você mesmo(a)
```

O e-mail `amigopet56@gmail.com` já está preenchido. Faça a mesma edição no `legal-config.js` do app, para os dois ficarem iguais.

## Passo 2: publicar no GitHub Pages (gratuito)

1. Entre no GitHub e clique em **+** e depois em **New repository**.
2. Nome do repositório: `amigopet-vendas`. Marque **Public** e clique em **Create repository**.
3. Na página que abrir, clique em **uploading an existing file**.
4. Arraste os **arquivos de dentro desta pasta** (não a pasta em si). O `index.html` precisa ficar na raiz do repositório.
5. Clique em **Commit changes**.
6. Vá em **Settings > Pages**. Em *Build and deployment*, deixe **Deploy from a branch**, escolha a branch **main**, a pasta **/ (root)** e clique em **Save**.
7. Espere de 1 a 3 minutos. O endereço aparece nessa mesma página, parecido com `https://seu-usuario.github.io/amigopet-vendas/`.
8. Abra o endereço no celular e no computador e confira a página.

## Passo 3: testar antes de divulgar

- Toque em todos os botões "Quero organizar a vida do meu pet": todos devem abrir o checkout da Greenn com o valor certo.
- Abra os links **Termos de uso**, **Política de privacidade** e **Contato** no rodapé.
- Confira se o texto dos Termos e da Política mostra o nome e o CNPJ da sua empresa, e não os campos entre colchetes.
- Faça uma compra de teste na Greenn, se ela permitir, para ver o que o cliente recebe.

## Passo 4: conectar com a Greenn

Não conheço o menu exato da Greenn, então confirme na central de ajuda dela. O que você precisa fazer lá:

1. **Divulgar o link da página de vendas** (o do Passo 2) nos seus anúncios e redes sociais.
2. **Configurar a entrega:** no produto, coloque o link do AmigoPet (o endereço onde o app está hospedado) como conteúdo ou mensagem de acesso, para o cliente receber depois da compra. Sugestão de texto:
   > Obrigado por comprar o AmigoPet! 🐾 Abra este link no celular: **(link do app)**. No Android use o Chrome e no iPhone use o Safari. Depois entre na aba **Instalar** para colocar o app na tela inicial. Qualquer dúvida: amigopet56@gmail.com
3. **Reembolso:** a página não menciona garantia, mas os Termos de Uso ainda citam o reembolso em até 7 dias (direito de arrependimento em compras online, art. 49 do Código de Defesa do Consumidor). Configure a política de reembolso na Greenn de acordo e, em caso de dúvida, confirme com um advogado.
4. Se a Greenn pedir a página de vendas do produto, informe o link do Passo 2.

## Domínio próprio (recomendado para vender)

Com um domínio como `amigopet.com.br`, o link fica mais profissional e confiável. No GitHub, em **Settings > Pages > Custom domain**, informe o domínio e crie no painel dele quatro registros **A** apontando para `185.199.108.153`, `185.199.109.153`, `185.199.110.153` e `185.199.111.153`, e um **CNAME** de `www` para `seu-usuario.github.io`. Depois ligue **Enforce HTTPS**.

## Mudar alguma coisa depois

- **Preço ou link de compra:** abra o `index.html` no GitHub (clique no arquivo e depois no lápis) e edite as linhas no começo do script, em `CONFIGURE AQUI`: `CHECKOUT_URL`, `PRICE` e `PRICE_NOTE`. Clique em **Commit changes**.
- **Texto da página:** edite o `index.html` do mesmo jeito, ou me peça a alteração e eu devolvo o arquivo novo para você enviar por **Add file > Upload files**.
- **Dados da empresa e e-mail:** edite o `legal-config.js`.
- O GitHub pode levar alguns minutos para mostrar a mudança.

## Cuidados

- **Promessas:** não prometa nos anúncios resultados de saúde ou de comportamento do animal. O app organiza e não substitui o veterinário.
- **Revisão jurídica:** peça a um advogado, de preferência com experiência em LGPD, que revise os Termos e a Política antes de vender.
- **Telas da página:** são ilustrativas (usam o Thor como exemplo).

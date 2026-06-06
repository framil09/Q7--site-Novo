# Qode7 Site

Site institucional estático da Qode7.

## Estrutura do projeto

- `index.html` -> Página inicial
- `empresa.html` -> Página da Empresa
- `compliance.html` -> Página de Compliance, Privacidade e LGPD

## Requisitos

- macOS, Linux ou Windows
- Python 3 instalado (para subir servidor local)

## Como rodar localmente

No terminal, entre na pasta do projeto e rode um servidor HTTP:

```bash
cd "/Users/Mac-Kener/Desktop/Q7-Projetos/qode7 Site"
python3 -m http.server 5500
```

Abra no navegador:

- Home: `http://localhost:5500/`
- Empresa: `http://localhost:5500/empresa.html`
- Compliance: `http://localhost:5500/compliance.html`

Para parar o servidor: `Ctrl + C` no terminal.

## Deploy na Cloudflare Pages

O projeto ja esta pronto para Cloudflare (site estatico com `index.html` na raiz).

### Opcao A - Conectando repositório Git (recomendado)

1. Suba este projeto para GitHub/GitLab.
2. No Cloudflare, acesse **Workers & Pages** -> **Create application** -> **Pages**.
3. Conecte seu repositório.
4. Configure o build:
   - **Framework preset**: `None`
   - **Build command**: *(deixe vazio)*
   - **Build output directory**: `/`
5. Clique em **Save and Deploy**.

### Opcao B - Upload manual (sem Git)

1. No Cloudflare, acesse **Workers & Pages** -> **Create application** -> **Pages**.
2. Escolha **Upload assets**.
3. Envie os arquivos:
   - `index.html`
   - `empresa.html`
   - `compliance.html`
4. Finalize o deploy.

## Checklist antes de publicar

- Conferir links internos funcionando (`/`, `/empresa.html`, `/compliance.html`)
- Atualizar dados reais da empresa (contato, CNPJ, DPO, e-mails)
- Testar em mobile e desktop

## Comandos uteis

Rodar local:

```bash
python3 -m http.server 5500
```

Verificar resposta da home:

```bash
curl -I http://localhost:5500/
```

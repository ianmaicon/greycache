# GREYCACHE — *Your Ground Zero*

> *"Quando tudo falhar, você ainda tem o GREYCACHE."*

Central de operações **100% offline** para preppers, sobrevivencialistas e gestores de crise. Um PWA self-hosted que funciona sem nuvem, sem cadastro e sem telemetria: **todos os dados ficam no dispositivo de quem usa** (IndexedDB), com backup por export JSON. Este container serve apenas os arquivos estáticos — nenhum dado de usuário passa pelo servidor.

## O que o app faz

- **Modo Preparação** (rotina): inventário com autonomia calculada (calorias estimadas automaticamente, validades por lote), estoque mínimo com Lista de Recompra, caixa de medicamentos, frota com checklists, equipamentos e manutenção, arsenal com documentos vigiados, mapa offline com waypoints, biblioteca de conhecimento, Índice de Prontidão 0–100 e Revisão Semanal guiada.
- **Modo Colapso** (crise ativa): decisão de Bug Out por gatilhos, plano de reunificação, painel de água, calculadora de energia, mapa de situação, registro de perímetro e consumo real vs planejado.
- **Privacidade por arquitetura**: sem anúncios, sem conta, sem "ligar para casa" — para sempre.

## Instalação rápida

```bash
docker run -d --name greycache -p 8090:80 --restart unless-stopped ghcr.io/ianmaicon/greycache:latest
```

Abra `http://SEU_IP:8090`. No celular, use **"Adicionar à tela inicial"** para instalar como app.

## Docker Compose / Portainer

```yaml
services:
  greycache:
    image: ghcr.io/ianmaicon/greycache:latest
    container_name: greycache
    ports:
      - "8090:80"
    restart: unless-stopped
    # Sem volumes, de propósito: os dados vivem no dispositivo de cada
    # usuário (IndexedDB) — backup pelo próprio app (Ajustes → Exportar JSON)
    read_only: true
    tmpfs:
      - /var/cache/nginx
      - /run
    security_opt:
      - no-new-privileges:true
    healthcheck:
      test: ["CMD", "wget", "-q", "--spider", "http://127.0.0.1/"]
      interval: 60s
      timeout: 5s
      retries: 3
      start_period: 5s
```

No Portainer: **Stacks → Add stack → Web editor**, cole o YAML acima e faça o deploy.
O container roda com filesystem **somente leitura** (endurecimento) — o nginx escreve apenas em tmpfs.

## Notas de operação

- **Sem volumes**: o servidor não guarda nada — os dados vivem no navegador/dispositivo de cada usuário. Atualizar o container não afeta dados de ninguém.
- **Atualização**: `docker compose pull && docker compose up -d` (ou re-pull da Stack no Portainer).
- **Tags**: `latest` acompanha a última versão; versões fixas em `ghcr.io/ianmaicon/greycache:0.1.0` etc.
- **HTTPS**: para instalar o PWA fora de `localhost`, os navegadores exigem HTTPS — use seu reverse proxy habitual (Traefik, NPM, Caddy) na frente da porta 80.
- **Faça backup**: Ajustes → Exportar Backup JSON. Dados 100% locais significam que o backup é responsabilidade sua — o app avisa quando ele envelhece.
- Multi-arch: **amd64** e **arm64** (roda em NAS, mini-PC e Raspberry Pi).

## Bugs e sugestões

Abra uma **[Issue](https://github.com/ianmaicon/greycache/issues)** neste repositório — este é o canal oficial de suporte da versão self-hosted.

## Apoie o projeto

O GREYCACHE é e sempre será **100% offline — sem anúncios, sem telemetria e sem conta**.
Se ele é útil na sua preparação, considere apoiar o desenvolvimento:
**[livepix.gg/mrmayc](https://livepix.gg/mrmayc)** (Pix). O apoio é voluntário e não
desbloqueia nada — o app inteiro já é seu.

---

*O código-fonte é desenvolvido em repositório privado; este repositório é a casa pública da distribuição self-hosted (imagem Docker, instruções e suporte).*

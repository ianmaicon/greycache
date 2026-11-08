# GREYCACHE — Política de Privacidade

*Última atualização: 08/11/2026. O app mostra estes termos na primeira abertura e pede o aceite; eles ficam em Ajustes → Sobre e apoio → Termos de uso e privacidade.*

O GREYCACHE foi feito para funcionar sem nuvem e sem conta. Esta política
explica, em detalhe, o que acontece com os seus dados.

## O que coletamos

**Nada.** O app não tem servidor próprio, não exige conta, não mostra anúncios
e não usa ferramentas de análise ou rastreamento. Inventário, remédios, dados
do grupo (inclusive médicos), mapas, diário e todo o resto ficam **somente no
seu aparelho**.

## Conexões que o app faz

O app funciona offline. Ele só usa a internet nestes casos, e nenhum deles
envia os seus dados:

- **Aviso de nova versão** (pode ser desligado em Ajustes): no máximo uma vez
  por semana, baixa um arquivo público de versão do GitHub
  (`raw.githubusercontent.com`). O GitHub recebe o endereço IP da conexão, como
  em qualquer acesso a um site.
- **Mapa**: as imagens do mapa vêm do servidor de mapas configurado (por padrão,
  o OpenStreetMap). Esse servidor recebe o IP e a área do mapa que está sendo
  vista, como em qualquer site de mapas.
- **Links que você abrir** (repositório, página de apoio) abrem no navegador.
- **Servidor da rede de casa** (opcional, só se você ligar): o app troca os
  pacotes de sincronização do grupo com o servidor que **você mesmo** instalou
  (container `greycache-sync`), no endereço que você informou. Os pacotes vão
  cifrados de ponta a ponta com a chave do grupo, que nunca vai para o
  servidor: ele guarda os pacotes sem conseguir ler. Ninguém além de você e do
  seu grupo tem acesso a esse servidor.

## Dados de saúde e de outras pessoas

Tipo sanguíneo, alergias e remédios são dados pessoais sensíveis pela Lei
Geral de Proteção de Dados (Lei nº 13.709/2018). No GREYCACHE eles ficam
somente no aparelho e nos backups que você exporta. Ao cadastrar familiares
e membros do grupo, é você quem decide guardar esses dados: peça a
autorização de cada pessoa, cadastre só o necessário e, para crianças e
adolescentes, faça isso como responsável por eles.

## Segurança é responsabilidade de quem usa

Não nos responsabilizamos pelo tipo de informação guardada no app, nem pelo
acesso de outras pessoas ao seu aparelho ou aos seus backups. Manter o app
seguro é responsabilidade de quem usa, com as ferramentas disponíveis: PIN
de bloqueio, desbloqueio por digital ou rosto, bloqueio automático, senha do
backup (o arquivo sai cifrado), o cartão de emergência só com o necessário e
o bloqueio de tela do próprio celular. Guarde a senha do backup: sem ela,
ninguém consegue abrir o arquivo, nem nós.

## Informação de referência e fontes

Guias, listas, cálculos e catálogos são informação de referência e não
substituem orientação médica nem de autoridades (SAMU 192, Bombeiros 193,
Defesa Civil 199). O catálogo de remédios vem da lista de preços de
medicamentos da CMED (Anvisa), sem os preços; a data da lista usada aparece
no app (Ajustes → Sobre e apoio). A tradução da apresentação ("caixa com 30
comprimidos") é automática: confira com a embalagem e a bula.

## Troca rápida e escambo

A Troca rápida passa informações de um celular para outro por QR, sem
internet: nada sai do aparelho por outro caminho. Nos escambos, cada recibo
(com o apelido da outra pessoa) fica só no seu aparelho e no seu backup; o
cartão de credibilidade que você mostra leva só números e datas, nunca com
quem você trocou nem o que foi trocado.

## Permissões do Android

- **Localização**: mostrar a sua posição no mapa e gravar rastros, só com o
  app aberto e quando você pede. A posição fica no aparelho.
- **Câmera**: ler QR codes de compartilhamento entre celulares do grupo. As
  imagens não são guardadas nem enviadas.
- **Biometria**: desbloquear o app no lugar do PIN. O app só recebe "sim" ou
  "não" do sistema; a digital ou o rosto nunca chegam a ele.
- **Notificações**: lembretes de validade, manutenção e remédio de uso
  contínuo, agendados no próprio aparelho. Para isso o app também pode
  reagendá-los quando o celular liga e mantê-lo acordado no instante do aviso.
- **Vibração**: resposta ao toque e alertas.
- **Funcionar em segundo plano** (ignorar a otimização de bateria): só se você
  tocar em "Permitir" em Ajustes → Avisos, o app pede ao Android para não
  fechá-lo por economia de bateria. Dá para desfazer nas configurações de
  bateria do Android.
- **Internet e estado da rede**: as conexões descritas acima e saber se o
  aparelho está offline.

Você pode negar qualquer permissão, exceto internet e rede: o resto do app
continua funcionando.

## Seus direitos sobre os dados

Como os dados ficam com você, você mesmo consulta, corrige, exporta (Ajustes →
Backup e dados) e apaga (Ajustes → Backup e dados → Redefinir banco de dados,
ou desinstalando o app).

## Sem garantia

O GREYCACHE é gratuito e fornecido como está, sem garantia de que funcionará
sem falhas em todos os aparelhos ou situações. Use também fontes oficiais e
mantenha cópias em papel do que for essencial.

## Backup

O backup é um arquivo que **você** exporta e guarda onde quiser. Se você
definir uma senha em Ajustes, o arquivo sai cifrado (AES-256). Sem a senha,
nem nós conseguimos abri-lo.

## Crianças

O app não coleta dados de ninguém, inclusive de crianças.

## Contato

Dúvidas: abra uma Issue em https://github.com/ianmaicon/greycache/issues.

---

# GREYCACHE — Privacy Policy (English)

*Last updated: November 2026.*

**We collect nothing.** GREYCACHE has no server, no account, no ads and no
analytics. All your data (inventory, medicine, group and medical data, maps,
log) stays **only on your device**.

The app only goes online to: check for a new version (a public file on GitHub,
at most weekly, can be turned off); load map tiles from the configured tile
server (OpenStreetMap by default); open links you tap; and, only if you turn
it on, exchange end-to-end encrypted group sync packages with the home server
you installed yourself (`greycache-sync`), which cannot read them. These servers see
your IP address, as with any website; none of your data is sent.

Health data (blood type, allergies, medicines) is sensitive personal data
under Brazil's General Data Protection Law (Law 13,709/2018) and stays only on
the device and in your backups. Ask family and group members for permission
before adding their data.

**We are not responsible for the kind of information kept in the app, nor for
other people accessing your device or backups.** Keeping the app secure is the
user's responsibility, with the tools provided: lock PIN, biometric unlock,
auto-lock, backup password, and the phone's own screen lock.

Reference information (guides, the medicine catalog from the CMED/Anvisa price
list, leaflets) does not replace medical advice; always check the package.
The app is free and provided as is, without warranty.

Android permissions: location (show your position and record tracks, only
while the app is open), camera (read QR codes between group phones),
biometrics (unlock instead of the PIN; the app only gets yes/no),
notifications (local reminders, rescheduled when the phone starts),
vibration, run in the background (only if you tap "Allow" in Settings →
Reminders, asks Android not to close the app to save battery), internet and
network state (the connections above).

Backups are files you export yourself; with a password set, they are
encrypted (AES-256). Questions: https://github.com/ianmaicon/greycache/issues.

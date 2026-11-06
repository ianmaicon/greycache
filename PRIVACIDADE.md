# GREYCACHE — Política de Privacidade

*Última atualização: novembro de 2026.*

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

## Troca rápida e escambo

A Troca rápida passa informações de um celular para outro por QR, sem
internet: nada sai do aparelho por outro caminho. Nos escambos, cada recibo
(com o apelido da outra pessoa) fica só no seu aparelho e no seu backup; o
cartão de credibilidade que você mostra leva só números e datas, nunca com
quem você trocou nem o que foi trocado.

## Permissões do Android

- **Localização**: mostrar a sua posição no mapa, quando você pede. A posição
  fica no aparelho.
- **Câmera**: ler QR codes de compartilhamento entre celulares do grupo. As
  imagens não são guardadas nem enviadas.
- **Biometria**: desbloquear o app no lugar do PIN. O app só recebe "sim" ou
  "não" do sistema; a digital ou o rosto nunca chegam a ele.
- **Notificações**: lembretes de validade, manutenção e remédio de uso
  contínuo, agendados no próprio aparelho.
- **Internet**: as conexões descritas acima.

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

Android permissions: location (show your position on the map when you ask), camera (read
QR codes between group phones), biometrics (unlock instead of the PIN; the app
only gets yes/no), notifications (local reminders), internet (the connections
above).

Backups are files you export yourself; with a password set, they are
encrypted (AES-256). Questions: https://github.com/ianmaicon/greycache/issues.

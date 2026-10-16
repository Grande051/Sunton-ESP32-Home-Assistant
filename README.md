# Painel Sunton ESP32-S3 8048S070 — ESPHome / LVGL

Versão pública do painel de automação residencial com menus de clima, iluminação, energia solar, segurança, impressora 3D, NerdMiner e finanças.

## Como começar
1. Instale o ESPHome e use a placa Sunton ESP32-S3 8048S070 (800 × 480, GT911).
2. Copie `secrets.example.yaml` para `secrets.yaml` e informe seus próprios dados. **Nunca faça commit do `secrets.yaml`.**
3. Ajuste os `entity_id` do YAML para os seus dispositivos Home Assistant; identificadores de exemplo não correspondem a entidades reais.
4. Disponibilize os arquivos de imagem `images/` e fonte `fonts/` referenciados no YAML. **Esses recursos não acompanham este pacote**, pois não foram enviados com o arquivo original. Verifique licenças antes de redistribuí-los.
5. Compile, valide e teste localmente antes de gravar na placa.

## Segurança
- Wi-Fi, código do alarme e URL da câmera são lidos de `secrets.yaml`.
- O código ainda contém ações de abrir portão e desarmar alarme: use apenas em rede confiável e com autenticação/autorização adequadas no Home Assistant.
- O endpoint de câmera pode exigir proteção adicional no go2rtc; ocultar o URL no repositório não protege o serviço.
- Revise os `entity_id` e nomes de cômodos antes de publicar.
- Se já houve commit de credenciais reais, excluir o arquivo do último commit não apaga o histórico; rotacione as credenciais expostas.

## Observações
Este YAML foi anonimizado a partir de uma configuração privada, mas **não foi compilado nem testado em hardware**. A substituição de nomes e IDs exige adaptação manual.

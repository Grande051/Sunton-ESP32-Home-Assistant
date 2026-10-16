# Painel Sunton ESP32-S3 8048S070 — ESPHome / LVGL

Projeto de automação residencial desenvolvido com **ESP32-S3, ESPHome, LVGL e Home Assistant**, utilizando uma tela touchscreen de 7 polegadas (800 × 480).

Versão pública **v1.9.1** do painel, com interface gráfica personalizada e menus para controle e monitoramento residencial.

## Funcionalidades

- 🏠 **HOME:** Tela inicial com informações da residência.
- 🌡️ **CLIMA:** Monitoramento de temperatura, umidade e condições meteorológicas.
- ❄️ **CLIMATIZAÇÃO:** Controle de ventiladores e dispositivos de climatização.
- 💡 **ILUMINAÇÃO:** Controle de lâmpadas inteligentes.
- ☀️ **SOLAR:** Monitoramento da geração de energia solar.
- 🔒 **SEGURANÇA:** Monitoramento de portas, portões, câmeras e alarme.
- 🖨️ **IMPRESSORA 3D:** Monitoramento de impressora 3D.
- 📊 **FINANÇAS:** Indicadores financeiros personalizados.
- ⛏️ **NERDMINER:** Informações de mineração experimental.
- ⚙️ **CONFIGURAÇÕES:** Ajustes de brilho, aparência e configurações do painel.

## Hardware utilizado

- **Placa:** Sunton ESP32-S3 8048S070
- **Tela:** LCD touchscreen de 7 polegadas
- **Resolução:** 800 × 480 pixels
- **Controlador touch:** GT911
- **Firmware:** ESPHome
- **Interface gráfica:** LVGL
- **Integração:** Home Assistant

## Estrutura do repositório

```text
Sunton-ESP32-Home-Assistant/
├── case-3d/
│   ├── README.md
│   └── Arquivo 3MF da case
├── fonts/
├── images/
├── .gitignore
├── LICENSE
├── README.md
├── painel_sunton_v1.9.1_publico.yaml
└── secrets.example.yaml
```

## Como começar

1. Instale o **ESPHome** e utilize uma placa compatível com a Sunton ESP32-S3 8048S070 (800 × 480, GT911).
2. Baixe os arquivos deste repositório, mantendo as pastas `images/` e `fonts/` no mesmo diretório do YAML.
3. Copie `secrets.example.yaml` para `secrets.yaml` e informe seus próprios dados. **Nunca faça commit do `secrets.yaml`.**
4. Ajuste os `entity_id` do YAML para os dispositivos do seu Home Assistant. Os identificadores de exemplo não correspondem a entidades reais.
5. Configure as integrações necessárias para utilizar os recursos de segurança, climatização, energia solar, impressora 3D e demais funcionalidades.
6. Valide e compile o firmware pelo ESPHome antes de gravar na placa.

## Segurança

Esta versão foi preparada para compartilhamento público, com substituição de informações privadas por exemplos.

- Wi-Fi, código do alarme e URL da câmera são lidos de `secrets.yaml`.
- O código contém ações de abertura de portão e controle de alarme. Utilize somente com autenticação, autorização e rede adequadamente protegidas.
- O endpoint da câmera pode exigir proteção adicional no go2rtc; ocultar a URL no repositório não protege o serviço.
- Revise os `entity_id` e nomes de dispositivos antes de utilizar.
- Nunca publique senhas, tokens ou arquivos de configuração privados.
- Caso credenciais reais tenham sido publicadas anteriormente, excluí-las do commit mais recente não elimina sua presença no histórico. Substitua as credenciais comprometidas.

## Case para impressão 3D

O projeto também disponibiliza uma **case para impressão 3D em formato 3MF**, adaptada para a tela Sunton ESP32-S3 de 7 polegadas.

O modelo foi baseado no projeto original [ESP32-8048S070 N/C Case](https://www.printables.com/model/350263-esp32-8048s070-nc-case), disponível no Printables.

**Modificações realizadas:**
- Adição de frestas para melhorar a ventilação.
- Adaptação para utilização no painel de automação residencial.

A case modificada é compartilhada sob a licença **Creative Commons CC BY-NC-SA 4.0**, respeitando os direitos do criador original.

Os arquivos e informações de licenciamento estão disponíveis na pasta `case-3d/`.

## Licenças

- **Código ESPHome:** MIT License, para os arquivos de autoria própria abrangidos pela licença.
- **Case 3D:** Creative Commons Attribution-NonCommercial-ShareAlike 4.0 (CC BY-NC-SA 4.0).
- **Imagens e fontes:** sujeitas às respectivas licenças de seus autores.

## Histórico de versões

**v1.9.1 — Versão pública**

- Disponibilização do YAML completo do painel.
- Remoção e substituição de identificadores privados.
- Inclusão dos arquivos de imagens e fontes.
- Inclusão da case modificada para impressão 3D.
- Documentação para configuração inicial e integração com Home Assistant.

## Observações

Este YAML foi anonimizado a partir de uma configuração privada. A substituição de nomes e identificadores exige adaptação manual.

A versão pública deve ser validada e compilada antes de ser utilizada. O funcionamento depende dos dispositivos e integrações disponíveis na instalação de cada usuário.

O projeto é disponibilizado para fins de estudo, personalização e desenvolvimento de soluções de automação residencial.

---

**Desenvolvido por [Grande051](https://github.com/Grande051)**

*ESP32 • ESPHome • LVGL • Home Assistant • IoT • 3D Printing*

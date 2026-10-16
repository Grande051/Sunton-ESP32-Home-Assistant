# Sunton ESP32-S3 7" — Home Assistant Dashboard

**ESPHome + LVGL + Home Assistant + 3D Printing**

Projeto de painel touchscreen de automação residencial desenvolvido para a placa **Sunton ESP32-S3 8048S070**, com tela de 7 polegadas (800 × 480 pixels).

O painel utiliza ESPHome e LVGL para criar uma interface gráfica personalizada, integrada ao Home Assistant para monitoramento e controle de dispositivos inteligentes.

Este repositório contém a versão pública **v1.9.1**, adaptada para compartilhamento com a comunidade maker.

## Funcionalidades

- 🏠 **HOME:** Tela inicial com informações da residência.
- 🌡️ **CLIMA:** Monitoramento de temperatura, umidade e condições ambientais.
- ❄️ **CLIMATIZAÇÃO:** Controle de dispositivos de climatização.
- 💡 **ILUMINAÇÃO:** Controle de lâmpadas inteligentes.
- ☀️ **SOLAR:** Monitoramento da geração de energia solar.
- 🔒 **SEGURANÇA:** Monitoramento de portas, portões, câmeras e alarme.
- 🖨️ **IMPRESSORA 3D:** Monitoramento de impressora compatível.
- 📊 **FINANÇAS:** Indicadores financeiros personalizados.
- ⛏️ **NERDMINER:** Informações de mineração experimental.
- ⚙️ **CONFIGURAÇÕES:** Ajustes de brilho e aparência do painel.

As funcionalidades dependem dos dispositivos e integrações configurados no Home Assistant.

## Hardware

| Componente | Especificação |
|---|---|
| Placa | Sunton ESP32-S3 8048S070 |
| Display | 7 polegadas |
| Resolução | 800 × 480 pixels |
| Touchscreen | GT911 |
| Firmware | ESPHome |
| Interface gráfica | LVGL |
| Integração | Home Assistant |
| Comunicação | Wi-Fi |

## Estrutura do projeto

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

## Instalação

### 1. Preparar o ambiente

Instale o ESPHome e configure seu Home Assistant.

Utilize uma placa compatível com o modelo Sunton ESP32-S3 8048S070.

### 2. Baixar o projeto

Baixe os arquivos deste repositório e mantenha as pastas `images` e `fonts` no mesmo diretório do YAML.

### 3. Configurar as credenciais

Copie o arquivo `secrets.example.yaml` para `secrets.yaml`.

Configure os valores correspondentes à sua rede e instalação:

```yaml
wifi_ssid: "SEU_WIFI"
wifi_password: "SUA_SENHA"
alarme_code: "SEU_CODIGO"
camera_snapshot_url: "http://SEU_SERVIDOR_LOCAL:1984/api/frame.jpeg?src=SUA_CAMERA&w=360&h=400"
```

**Importante:** nunca publique seu arquivo `secrets.yaml` com credenciais reais.

### 4. Configurar o Home Assistant

Abra o arquivo `painel_sunton_v1.9.1_publico.yaml` e substitua os identificadores de exemplo (`entity_id`) pelas entidades correspondentes aos seus dispositivos.

Os sensores, controles e demais integrações precisam ser adaptados à sua residência.

### 5. Compilar e instalar

No ESPHome:

1. Importe ou configure o YAML.
2. Execute a validação da configuração.
3. Compile o firmware.
4. Instale na placa compatível.
5. Conecte o dispositivo ao Home Assistant.

Confira a compatibilidade da revisão da placa antes da gravação.

## Segurança

Esta versão foi preparada para compartilhamento público.

- Senhas e credenciais são referenciadas por `!secret`.
- Identificadores pessoais foram substituídos por exemplos.
- Endereços de câmera devem ser configurados localmente.
- O arquivo `.gitignore` impede o rastreamento de arquivos de credenciais comuns.
- Os controles de portão e alarme exigem autenticação e permissões adequadas no Home Assistant.

A configuração publicada não deve ser utilizada sem revisão das permissões de segurança.

## Case para impressão 3D

O projeto também disponibiliza uma case adaptada para impressão 3D, em formato **3MF**.

A adaptação foi baseada no modelo [ESP32-8048S070 N/C Case](https://www.printables.com/model/350263-esp32-8048s070-nc-case), disponível no Printables.

**Modificação realizada:** adição de aberturas para melhorar a circulação de ar e a dissipação de calor.

A case modificada é distribuída sob a licença **Creative Commons CC BY-NC-SA 4.0**.

Consulte a pasta `case-3d` para os créditos e condições de uso.

## Licenças

**Código ESPHome:** MIT License, para os arquivos de autoria própria cobertos por essa licença.

**Case 3D modificada:** [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).

Imagens, fontes e outros materiais de terceiros permanecem sujeitos às suas respectivas licenças.

## Versão

**v1.9.1 — Public Release**

Versão pública anonimizada do painel completo, destinada ao estudo, à personalização e ao desenvolvimento de projetos de automação residencial.

A compilação e o funcionamento dependem da configuração local. O projeto deve ser validado antes da instalação.

---

**Developed by [Grande051](https://github.com/Grande051)**

*ESP32 • ESPHome • LVGL • Home Assistant • IoT • 3D Printing*

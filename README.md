# Panora

O **Panora** distribui e organiza wallpapers em Macs com vários monitores, com controles acessíveis pela barra de menus.

## Recursos

- Wallpapers estáticos e dinâmicos, incluindo pares para as aparências Claro e Escuro.
- Distribuição de wallpapers entre múltiplos monitores.
- Biblioteca, editor e pré-visualização antes de aplicar.
- Início exclusivamente na barra de menus, sem ícone no Dock.
- Dois atalhos globais opcionais, configuráveis pelo usuário.
- Interface em português brasileiro e inglês.

## Requisitos

- macOS 15 ou posterior.
- Mac Intel ou Apple Silicon.

## Disponibilidade

A primeira versão planejada para distribuição é a **1.0.0**. O instalador ainda não está publicado. Quando a versão estiver disponível, os arquivos de instalação serão anunciados na página de releases deste repositório.

O código-fonte principal do Panora é mantido em um repositório privado. Este repositório público é destinado à documentação e aos artefatos oficiais de distribuição.

## Instalação

Depois que uma release for publicada:

1. Baixe o DMG anexado à release oficial.
2. Baixe também o arquivo de checksum SHA-256 correspondente e deixe ambos na mesma pasta.
3. No Terminal, dentro dessa pasta, confira a integridade do DMG com:

   ```sh
   shasum -a 256 -c Panora-1.0.0-Universal.dmg.sha256
   ```

   A saída deve indicar `OK`. Se o resultado for diferente, não abra o instalador.
4. Abra o DMG e arraste `Panora.app` para a pasta Aplicativos, usando o atalho exibido na janela do instalador.
5. Ejete o DMG. Na primeira abertura, siga as instruções do macOS descritas abaixo, se forem exibidas.

## Aviso do macOS (Gatekeeper)

O build 1.0.0 (3) foi assinado com um certificado **Apple Development** e usa Hardened Runtime. Ele não usa assinatura **Developer ID** e não foi notarizado pela Apple. O App Sandbox está desativado. A avaliação local por `spctl` rejeitou o pacote.

A assinatura Apple Development usada neste build não equivale à assinatura Developer ID para distribuição pública. Por isso, o macOS pode bloquear ou avisar sobre a primeira abertura, e a experiência pode variar conforme as políticas de cada Mac. Não é possível garantir que a instalação será permitida em todos os computadores.

Se você obteve o app de uma fonte confiável, verificou o arquivo e decidiu prosseguir, consulte somente as orientações oficiais da Apple para autorização manual: [Abrir apps com segurança no Mac](https://support.apple.com/pt-br/102445). As opções disponíveis variam conforme o alerta e as políticas aplicadas ao Mac. Não prossiga se não tiver certeza da origem ou integridade do app.

## Créditos e licenças

O Panora deriva do [SpreadPaper](https://github.com/spreadpaper/SpreadPaper), criado por Robin van Baalen. A licença MIT e o aviso de copyright do código original são preservados nos avisos de terceiros. O SpreadPaper não é responsável pelas alterações e decisões próprias do Panora.

Consulte [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) para atribuições e avisos de componentes e fotografias. Esses avisos não significam que o aplicativo Panora, suas modificações ou seu código-fonte estejam licenciados sob MIT.

# Soundboard

Vincule áudios a teclas do teclado e toque com um toque. Roda em **Windows, macOS e Linux** (Electron).

## Baixar

Baixe a versão mais nova (ou veja todas em [Releases](https://github.com/YuriAtzler/soundboard-releases/releases)):

| Sistema | Arquivo |
| --- | --- |
| Windows (instalador) | [Soundboard-Setup.exe](https://github.com/YuriAtzler/soundboard-releases/releases/latest/download/Soundboard-Setup.exe) |
| Windows (portátil, sem instalar) | [Soundboard-Portatil.exe](https://github.com/YuriAtzler/soundboard-releases/releases/latest/download/Soundboard-Portatil.exe) |
| macOS com chip Apple (M1 ou mais novo) | [Soundboard-mac-arm64.dmg](https://github.com/YuriAtzler/soundboard-releases/releases/latest/download/Soundboard-mac-arm64.dmg) |
| macOS com Intel | [Soundboard-mac-x64.dmg](https://github.com/YuriAtzler/soundboard-releases/releases/latest/download/Soundboard-mac-x64.dmg) |
| Linux (AppImage) | [Soundboard-linux.AppImage](https://github.com/YuriAtzler/soundboard-releases/releases/latest/download/Soundboard-linux.AppImage) |
| Linux (Debian/Ubuntu) | [soundboard-linux.deb](https://github.com/YuriAtzler/soundboard-releases/releases/latest/download/soundboard-linux.deb) |

O app não tem assinatura digital paga, então o sistema avisa na primeira vez:

- **Windows**: na tela azul "O Windows protegeu o computador", clique em **Mais informações → Executar assim mesmo**.
- **macOS**: arraste o app para Aplicativos e abra. Quando aparecer que a Apple não pôde verificar o app, vá em
  **Ajustes do Sistema → Privacidade e Segurança** e clique em **Abrir Mesmo Assim**. Se ainda disser que o app
  "está danificado", rode no Terminal `xattr -cr /Applications/Soundboard.app` e abra de novo.
- **Linux (AppImage)**: dê permissão de execução (`chmod +x Soundboard-linux.AppImage`) e abra.

## Atualizar

O app procura versões novas sozinho (ao abrir e a cada 6 horas) e avisa no pé da barra lateral.

- **Windows (instalador e portátil)** e **Linux (AppImage)**: a versão nova é baixada em segundo plano; clique em **Reiniciar** e pronto.
  (O portátil troca o próprio `.exe`; se ele estiver numa pasta sem permissão de escrita, cai no botão **Baixar**.)
- **macOS** e **.deb**: o aviso tem um botão **Baixar**, que já abre o arquivo certo; instale por cima.
  (No Mac, atualizar sozinho exigiria a assinatura paga da Apple.)

Seus sons, perfis e configurações continuam depois de atualizar. Quem está na 2.0.0 precisa baixar a próxima versão à mão uma vez;
dali em diante o aviso aparece no próprio app. Também dá para procurar em **Configurações → Atualizações**.

## Como usar

- **Adicionar áudio**: botão **Adicionar** no topo ou arraste arquivos (mp3, wav, ogg, m4a, aac, flac, webm, opus). Cada arquivo abre
  uma janela para escolher o nome, o trecho que toca (arraste as alças na forma de onda e use **Ouvir trecho**) e a
  tecla (pelo menos uma é obrigatória). O som só é adicionado ao confirmar. Com vários arquivos, eles abrem um de cada vez ("2 de 5"),
  e dá para pular algum.
- **Importar de link**: na seta ao lado de **Adicionar → Importar de link…**, cole o link de um áudio ou de uma página que
  tenha um, como os botões do [MyInstants](https://www.myinstants.com/pt/index/br/). Também dá para colar o link direto
  na janela (`Ctrl+V`) ou arrastá-lo do navegador. O áudio é baixado e abre a mesma janela de nome, trecho e tecla.
- **Editar**: clique no nome do som ou no lápis para mudar o nome, o trecho ou a tecla. O corte não altera o arquivo,
  então **Usar o áudio inteiro** desfaz.
- **Teclas**: um som pode ter várias teclas. Clique numa tecla do som e aperte outra para trocá-la, ou no **+** para
  acrescentar uma (combinações com Ctrl/Alt/Shift/Cmd funcionam). `Esc` cancela e `Backspace` remove a tecla, desde que
  sobre outra. Uma tecla que já é de outro som, de um perfil ou de "parar tudo" é recusada: aperte outra.
- **Tocar**: aperte a tecla (apertar de novo para) ou clique no play. `Esc` para tudo.
- **Segundo plano**: as teclas funcionam mesmo com o app minimizado ou em outra janela. Fechar a janela só a esconde:
  o app continua no ícone perto do relógio (Windows/Linux; no Windows ele pode estar dentro da setinha **^**), cujo menu
  troca de perfil, para todos os sons, abre a janela ou sai. No Mac, o mesmo menu fica no clique direito do ícone no Dock,
  e sai-se com Cmd+Q. Se preferir que o ✕ feche o app, mude em **Configurações → Ao fechar a janela**.
  Use teclas como F1–F12 ou combinações (ex.: `Ctrl+1`, `Ctrl+Num 1`), porque o atalho global "rouba" a tecla dos outros apps.
  No Windows, deixe o NumLock ligado para usar o teclado numérico como atalho global. Uma tecla com ⚠ só funciona com o
  app em foco (passe o mouse para ver o motivo).
- **Buscar e ordenar**: `Ctrl+F` busca pelo nome; clique em **Nome** ou **Tecla** no cabeçalho para ordenar.
- **Vários de uma vez**: marque os sons (Shift+clique marca um intervalo) para mudar o volume de todos ou removê-los.
- **Teclado na lista**: ↑/↓ escolhem o som, `Espaço` toca, `Enter` ou `F2` edita e `Delete` remove.
  Teclas vinculadas a sons têm prioridade.
- **Perfis** (na barra lateral): cada perfil é um conjunto separado de sons e teclas (ex.: "Live", "Jogo"), e a tecla do
  perfil troca para ele de qualquer lugar. O **⋯** (ou clique direito) de cada perfil renomeia, define a tecla, exporta ou
  apaga. O **+** cria um perfil novo ou importa um.
- **Levar perfis para outro computador**: **Exportar…** gera um arquivo `.soundboard` com os sons, os trechos, os volumes
  e as teclas. No outro computador, use **+ → Importar perfil…** ou arraste o arquivo para a janela. Se o nome ou a tecla
  já existirem, o perfil entra como "Nome (2)" e as teclas repetidas ficam de fora.
- **Tema**: Sistema, Claro ou Escuro, no pé da barra lateral.
- **Configurações** (⚙ no pé da barra lateral), cada uma com a explicação do que faz:
  - **Áudio**: saída de áudio (fone, caixa ou um cabo virtual, como o VB-Cable, para mandar ao Discord), volume geral e
    "um som por vez".
  - **Teclas**: a tecla de parar tudo (vale como atalho global, em qualquer perfil), **Confirmar antes de tocar** (a
    tecla de um som mostra o nome dele num aviso na tela, e só a segunda batida em até 4 segundos toca, com o aviso passando a mostrar o progresso do som; a tecla
    de outro som troca o aviso. Em **Posição do aviso** escolha o canto ou o meio, em cima ou embaixo. O aviso fica por cima de janelas em tela cheia sem borda, mas não de jogos em tela cheia
    exclusiva) e, no Windows, o **teclado dos sons**:
    escolha "Identificar teclado…" e aperte uma tecla no teclado que vai disparar os sons, por exemplo um teclado numérico USB.
    Daí em diante só ele dispara os sons, e as mesmas teclas nos outros teclados ficam livres. Ctrl/Alt/Shift podem vir de
    qualquer teclado. A tecla também chega ao app em foco, então prefira teclas que não façam nada nele.
  - **Segundo plano**: o que o ✕ faz e **Iniciar com o sistema** (o app abre escondido, com as teclas já funcionando).
  - **Backup**: **Exportar tudo** guarda todos os perfis, sons e configurações num `.soundboard`; **Restaurar** junta os
    perfis do backup aos atuais ou substitui tudo. A saída de áudio e o teclado escolhido não vão no backup.
  - **Atualizações** e **Aparência**: tema e **idioma** (português ou inglês; por padrão, o do sistema).

Os áudios são copiados para a pasta de dados do app, então o arquivo original pode ser movido ou apagado.

## Observações

- **Linux/Wayland**: atalhos globais podem não funcionar em algumas sessões Wayland; nesse caso as teclas continuam funcionando com a janela em foco.
- **macOS**: atalhos globais podem pedir permissão de Acessibilidade.

## Licença

© 2026 Yuri Atzler. Todos os direitos reservados. O Soundboard não pode ser redistribuído,
vendido ou modificado sem autorização.

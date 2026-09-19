# zmk-config-AroundFortyRB


Around Forty RightBallのファームウェア。

AMLはOFF。

→ config/boards/shields/AroundForty-RB/AroundForty-RB_R.overlay　61行目

# Keymaps

## Mac (& NUM & settings)

![mac](figs/mac_and_setting_layer.svg)

## Windows

![windows](figs/win-keymap.svg)

# 更新手順

ビルドは ZMK `v0.2-branch` を使用しています。互換性を維持するため、
`.github/workflows/build.yml` の再利用ワークフローと、`config/west.yml` の
`inorichi/zmk-pmw3610-driver` はコミット SHA に固定しています。
ワークフローは 2026-02-17 の成功時の版、ドライバーは既存の
`CONFIG_PMW3610_*` と `scroll-layers` に対応する版です。
これらを更新する際は、ZMK・ドライバー・シールド設定の互換性を合わせて確認してください。

1. [keymap-editor](https://nickcoutsos.github.io/keymap-editor/)で好きにいじる(repoは自分のを読ます)
2. [Save]をおしてcommitする
3. Actiosが終わったらLatestのファームウェアをDL＆解凍する
4. 右手側をPCとUSBで直接接続して&bootloaderを実行、ビルドしたファームウェアを配置する
5. [keymap-drawer](https://keymap-drawer.streamlit.app/) で.keymapを読ませてキーマップを更新する

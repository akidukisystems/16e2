# AS 16bit Extended Emulator (16E2)

## これ何？
AS 16bit Extended Emulator (16E2) は、独自の16bit命令セット・アーキテクチャであるAS216を採用したエミュレータを中心とする開発プロジェクトです。
IntelのIA-32マイクロアーキテクチャと似て非なるものです。
コードの互換性はありません。

## ISA
本プロジェクトに関連する命令セット・アーキテクチャは以下のとおりです。
| 名称 | 概要 |
|---|---|
| AS16 | 以前に設計した16bit命令セット・アーキテクチャ（リポジトリ「AS-16bit-Emu」を参照） |
| AS116 | AS16を改良した命令セット・アーキテクチャ |
| AS216 | AS116を見直し、微調整した命令セット・アーキテクチャ |

AS16からAS116、AS216へと設計を発展させていきます。

## エミュレータ
| 名称 | 採用ISA |
|---|---|
| AS 16bit Emulator | AS16 |
| AS 16bit Extended Emulator (16E2) | AS216 |

## アセンブリ変換ツール
AS216の機械語コードを生成するため、アセンブリ言語と機械語の間に中間言語ASILを使用します。
変換処理は以下の2つのツールで構成されます。
| 名称 | 機能 |
|---|---|
| ASM2IL | アセンブリ言語からASILへの変換 |
| IL2MCH | ASILから機械語コードへの変換 |

変換の流れは以下のとおりです。
アセンブリ言語
  ↓ ASM2IL
ASIL
  ↓ IL2MCH
AS216機械語コード

## 関連仕様
各命令セット・アーキテクチャおよび中間言語の詳細は、それぞれの仕様書を参照してください。

## 免責事項
このソフトウェアを使用し、いかなる損害が発生しても製作者は一切責任を負いません。

## 注意事項
このソフトウェアは、クリエイティブ・コモンズ 表示 - 継承 4.0 国際 ライセンス の下に提供されています。 
This software is licensed a CC BY-SA 4.0 .

## 動作環境
開発環境
OS      : Windows 11 Pro 26H2 (Build 26300.9711)
ｿﾌﾄｳｪｱ  : Microsoft VS Code
CPU     : AMD Ryzen 9 5950X 16-Core Processor
Graphic : NVIDIA GeForce RTX 3060
RAM     : DDR4-3200 PC4-25600 32GBx4

最低動作環境
OS      : AMD64アーキテクチャで動作する　Windows Vista 以上の Windows NT系 OS
CPU     : 特になし
Graphic : 特になし
Display : 特になし
RAM     : 特になし
空き容量 : 特になし

## 雑記
製作者：秋月
連絡先：support@AkidukiSystems.com
ホームページ：https://akidukisystems.com

最終更新    : 2026/11/22
# IoTミニチュアハウス (Miniature IoT Unit Set)

本リポジトリは、神奈川工科大学 杉村研究室が企業と共同で開発・製作した、IoT教育用教材**「IoTミニチュアハウス (Miniature IoT Unit Set)」**の紹介ウェブサイトおよび関連ドキュメント（仕様書・マニュアル）を管理するリポジトリです。

紹介サイト： [https://miniature.sugi-lab.net/](https://miniature.sugi-lab.net/)

**開発はv1フォルダで行ってください。完成したらdocsフォルダにコピーしてGitHubにPushすればデプロイされます。**

---

## 1. プロジェクト概要

「IoTミニチュアハウス」は、実際のスマートホームや家電製品と同様のネットワーク通信を模した**「ハードウェアエミュレーター」**です。
各ミニチュア機器にはマイコン（ESP32等）が搭載されており、本物の家電製品と同じ業界標準規格 **ECHONET Lite** に準拠した通信を行います。
実社会に即した本格的なスマートホーム制御の実習を、安全かつ省スペースで実現できます。

---

## 2. 開発目的と特徴

従来のIoT教育やスマートホームの実習には、主に以下の3つの課題がありました。

1. **設置と保管の課題**：住宅や大型家電の実機を学校・研究室内に設置・保管するのが困難。
2. **通信・ネットワークの課題**：シミュレーターだけでは、各機器に個別のIPアドレスを割り当ててリアルな通信ネットワークを構築する実習が難しい。
3. **可搬性の課題**：デモや実習のために機材を学外や展示会等へ持ち運ぶのが極めて困難。

本プロジェクトでは、これらを**「スーツケースに収まるサイズのミニチュア化」**と**「Wi-Fiルーターの内蔵によるネットワーク再現」**によって解決しました。これにより、どこにでも持ち運べる高品質なIoT実習環境を実現しています。

---

## 3. 提供・再現されているデバイス一覧

本ミニチュアハウスには、以下のスマート家電および設備機器が搭載されています。

| デバイス名 | 特徴・シミュレート機能 |
| :--- | :--- |
| **スマートメーター** | 瞬時電力、積算電力、電圧、電流などのデータを保持。機器の稼働状況に応じた電力量の変化を模擬します。 |
| **鍵付き玄関扉** | 電動式のカギ（電気錠）を搭載。開閉センサーにより、扉やカギの状態（施錠・解錠）を通信で管理・取得できます。 |
| **壁照明** | 調光機能および照明の向きを物理的に調整可能です。 |
| **床暖房** | 運転状態に合わせたオレンジ色のLED点灯。設定温度による明るさ変化や、ブロックごとの制御に対応します。 |
| **テレビ** | 電源制御、音量調整に加え、画面でMP4ファイルを自動再生できます。 |
| **フロア照明** | フルカラーLED（RGBLED）を搭載。RGB調光・調色機能および照明モード切り替えに対応。 |
| **エアコン** | 電源、冷暖房運転モード切り替え、風量設定など。内部に温湿度センサーを搭載し、センサーデータの取得実習も可能です。 |
| **電動窓** | 電動で窓を開閉。任意の位置で開閉を停止する制御にも対応します。 |

---

## 4. ドキュメント（マニュアル・仕様書）

本リポジトリには、学習やファームウェア開発に必要な以下のPDFドキュメントが収録されています。

### 開発・インストールマニュアル
- [Miniature Set Manual (Ver.0.02ax)](docs/Development%20board%20installation%20instructions-Ver.0.02ax.pdf)
- [Miniature Set 追加パーツ資料](docs/Miniature%20Set%20Parts%20.pdf)

### ECHONET Lite 機器仕様書（Firmware仕様）
| 機器 | 日本語版仕様書 | 英語版仕様書（Global Edition） |
| :--- | :--- | :--- |
| **エアコン** | [PDFを見る](docs/Miniatur%20IoT%20Air-Conditioner%20Unit%20model-1%20Frimware%20%20%20ECHONET%20Lite仕様書.pdf) | [PDFを見る](docs/Miniatur%20IoT%20Air-Conditioner%20Unit%20model-1%20Frimware%20%20%20ECHONET%20Lite%20Specification_GlobalEdition.pdf) |
| **電気錠（扉）** | [PDFを見る](docs/Miniatur%20IoT%20Door%20Unit%20model-1%20Frimware%20%20%20ECHONET%20Lite仕様書.pdf) | [PDFを見る](docs/Miniatur%20IoT%20Door%20Unit%20model-1%20Frimware%20%20%20ECHONET%20Lite%20Specification_GlobalEdition.pdf) |
| **一般照明** | [PDFを見る](docs/Miniatur%20IoT%20Light%20Unit%20model-1%20Frimware%20%20%20ECHONET%20Lite仕様書.pdf) | [PDFを見る](docs/Miniatur%20IoT%20Light%20Unit%20model-1%20Frimware%20%20%20ECHONET%20Lite%20Specification_GlobalEdition.pdf) |

---

## 5. 関連リンク

- **ファームウェアソースコード**： [Hiroshi-Sugimura/EL-Firmwares-for-Miniature](https://github.com/Hiroshi-Sugimura/EL-Firmwares-for-Miniature)
- **導入・お問い合わせ（Notion）**： [杉村研究室 お問い合わせ窓口](https://sugi-lab.notion.site/1ca39dcd62488038bbdbfbbe3eaa5f50?pvs=105)
- **関連規格・団体**：
  - [ECHONET Lite規格について（エコーネットコンソーシアム）](https://echonet.jp/about/features/)
  - [神奈川工科大学 杉村研究室](https://hiroshi.sugimura.jp/)

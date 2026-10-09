# 第三方來源聲明

Tsuzuri 衍生自 Arben Apura 的 XianScan，兩者都以 MIT 授權發布（見 LICENSE）。以下模型、字典與字型不在 MIT 授權範圍內，各自適用自己的授權。

## 第一次啟動時下載的辨識模型

Tsuzuri 的發行包不含這些模型。第一次啟動時，程式會列出每個模型的來源與授權。你同意之後，程式直接從原始來源下載。使用這些模型時，請遵守各來源的條款。Tsuzuri 不會另外授權這些模型。

| 模型 | 用途 | 來源 | 授權 |
| --- | --- | --- | --- |
| encoder_model.onnx、decoder_model.onnx | 日文文字辨識（Manga OCR） | [mayocream/manga-ocr-onnx](https://huggingface.co/mayocream/manga-ocr-onnx)，由 [kha-white/manga-ocr-base](https://huggingface.co/kha-white/manga-ocr-base) 轉換 | Apache-2.0；訓練資料為 Manga109-s，使用前請自行查看該資料集的條款 |
| rfdetr-seg-2xlarge.onnx | 偵測對話框與版面 | [DevilishDaoSaint/koharu-layout-rfdetr](https://huggingface.co/DevilishDaoSaint/koharu-layout-rfdetr) | 依來源頁面：Manga109 學術條款，僅限非商業使用 |
| lama.onnx | 清除原文（修圖） | [ogkalu/lama-manga-onnx-dynamic](https://huggingface.co/ogkalu/lama-manga-onnx-dynamic) | Apache-2.0 |
| PP-OCRv6_det_small.onnx、PP-OCRv6_rec_small.onnx | 文字位置偵測、多語文字辨識 | [RapidAI/RapidOCR](https://www.modelscope.cn/models/RapidAI/RapidOCR) | 見來源頁面 |
| korean_mobile_v2.0_rec.onnx、cyrillic_mobile_v2.0_rec.onnx、th_PP-OCRv5_mobile_rec.onnx | 韓文、西里爾字母、泰文文字辨識 | [xberg-io/paddleocr-onnx-models](https://huggingface.co/xberg-io/paddleocr-onnx-models) | Apache-2.0 |

每個檔案的下載網址、大小與 SHA256，列在發行包的 `models\manifest.tsv` 與 `models\download-manifest.tsv`。

## 隨附的字典檔

| 檔案 | 來源 | 授權 |
| --- | --- | --- |
| `models\manga-ocr-vocab.txt` | [cl-tohoku/bert-base-japanese-char-v2](https://huggingface.co/cl-tohoku/bert-base-japanese-char-v2)，Tohoku NLP Group（東北大學） | CC BY-SA（模型卡內文標示 3.0，頁首標示 4.0）。本檔案依模型卡的條款散布，並標示出處：cl-tohoku/bert-base-japanese-char-v2，Tohoku NLP Group |
| `models\ppocr_keys_v1.txt`、`korean_dict.txt`、`th_dict.txt`、`cyrillic_dict.txt`、`rapidocr_keys.json` | [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR)、[RapidOCR](https://github.com/RapidAI/RapidOCR) | Apache-2.0 |

## 內嵌在 Tsuzuri.exe 的字型

| 字型 | 授權 |
| --- | --- |
| Noto Sans TC、Noto Sans Devanagari、Noto Sans Thai | SIL Open Font License 1.1 |
| Comic Neue、Lexend、Montserrat、Poppins、Sigmar One、Tajawal | SIL Open Font License 1.1 |
| Friendly Sans（作者 ggbot） | SIL Open Font License 1.1 |
| 文泉驛微米黑（WenQuanYi Micro Hei） | Apache-2.0 |

## 程式元件

Rust crate、npm 套件，以及 Node.js、ONNX Runtime、DirectML、Microsoft Visual C++ 執行階段的授權，見 THIRD_PARTY_LICENSES.md。

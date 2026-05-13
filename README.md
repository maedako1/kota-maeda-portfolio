# Kota Maeda — portfolio & slides

Single-page portfolio (`index.html`) and a **Reveal.js** deck (`slides/index.html`) in **English**, aligned with the July 2025 self-introduction materials.

## PowerPoint (python-pptx)

The parent folder (one level above this repo) holds your template `20250701*.pptx` and the generator script.

```bash
cd ..
pip install -r scripts/requirements.txt
python scripts/build_intro_en_pptx.py
```

This writes **`Kota_Maeda_SelfIntroduction_EN.pptx`** next to the template (same 4:3 size, theme / colours from your deck: red `#D51317`, footer teal `#009FB2`, Segoe UI).

## Preview locally

```bash
python -m http.server 8080
```

- Site: `http://localhost:8080/`
- Slides: `http://localhost:8080/slides/` (arrow keys to navigate)

## Vercel

1. [Vercel にログイン](https://vercel.com)し、**Add New… → Project** を開きます。
2. **Import Git Repository** で `maedako1/kota-maeda-portfolio` を選びます（初回は GitHub の Vercel アプリを承認）。
3. **Framework Preset** は *Other* のまま、**Root Directory** は `.`（リポジトリ直下）のままにします。Build / Output の追加設定は不要です。
4. **Deploy** を押すと、本番 URL（例: `https://kota-maeda-portfolio.vercel.app`）が発行されます。
5. スライドは `https://（あなたのドメイン）/slides/` です。

CLI でデプロイする場合は、一度 `npx vercel login` のあと、リポジトリのルートで `npx vercel --prod` を実行してください。

### Git（Windows で SSL エラーが出る場合）

このローカルリポジトリでは `git config http.sslBackend schannel` を設定してから `git push` しています。別 PC で同様のエラーが出る場合は、同じ設定を試すか、社内の証明書ポリシーを確認してください。

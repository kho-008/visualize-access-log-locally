# ロールでのアクセスログの視覚化

## 準備作業
1. cPanelにログイン
1. メトリック / 未加工のアクセスをクリック
1. 対象のドメインを選択
1. 〇〇.gzファイルをダウンロード
1. gzファイルを解凍
```bash
gzip -cd 〇〇.gz > access.log
```

## goaccessをインストール
```bash
# Mac
brew install goaccess

# WSL
sudo apt update
sudo apt install goaccess
```

## ログをHTML化
```bash
goaccess access.log -o log.html --log-format=COMBINED
```

## 参考サイト
- [アクセスログ・エラーログの確認方法 – mixhost ヘルプ＆サポート](https://help.mixhost.jp/hc/ja/articles/4407888551193-%E3%82%A2%E3%82%AF%E3%82%BB%E3%82%B9%E3%83%AD%E3%82%B0-%E3%82%A8%E3%83%A9%E3%83%BC%E3%83%AD%E3%82%B0%E3%81%AE%E7%A2%BA%E8%AA%8D%E6%96%B9%E6%B3%95)
- [gzipコマンドの使い方: 小粋空間](https://www.koikikukan.com/archives/2012/06/01-235555.php#:~:text=%E3%81%82%E3%82%8B%E3%83%87%E3%82%A3%E3%83%AC%E3%82%AF%E3%83%88%E3%83%AA%E9%85%8D%E4%B8%8B%E3%81%AB%E3%81%82%E3%82%8B,%E5%90%8D%E3%82%92%E6%8C%87%E5%AE%9A%E3%81%97%E3%81%BE%E3%81%99%E3%80%82)
- [NginxのログをGoAccessでアクセス解析【2020/07】 | テック備忘LOG](https://yuki-yamashita.site/blog/post/nginx-goaccess/)
- [Ubuntu22.04にWebログ解析ツールGoAccessをインストールする - 最新IT技術情報_arkgame.com](https://arkgame.com/2022/10/08/post-313665/)
- [goaccess を用いて Apache のログを1 コマンドで HTML ファイル化する（Ubuntu 上）](https://www.kkaneko.jp/tools/server/goaccess.html)
- [goaccess — Homebrew Formulae](https://formulae.brew.sh/formula/goaccess)
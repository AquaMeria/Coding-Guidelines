# モックアップ使用方法


## 検証・対応ブラウザ  
|| **Windows** | **Mac** | **スマートフォン・タブレット** |
|:----- |:-----:|:-----:|:-----:|
|InternetExplorer 11|○|×|×|
|Safari 最新版|×|○|○|
|GoogleChrome 最新版|○|○|○|
|Firefox 最新版|○|○|×|
|iOS 10~|×|×|○|
|AndroidOS 5.0~|×|×|○|  
 
 
## ディレクトリ構造  
 ルート  
　├ [css] … サイトで使われるCSSファイルを全て格納する  
　│　├ bootstrap.min.css … Bootstrapの標準CSS  
　│　├ common.css … 全ページで使用するCSS(グロナビetc)  
　│　├ module.css … 全ページで共通で使用するパーツCSS(ボタンetc)   
　│　└ pagename.css …  各ページでのみ使用するCSS  
　│   
　├ [img] … サイトで使われる画像を全て格納する  
　│　├ [common] … 全ページ共通で使用する画像  
　│　└ [directory] …  各ディレクトリで使用する画像  
　│   
　├ [js] … サイトで使われるJavaScriptを全て格納する  
　│　├ bootstrap.min.js … Bootstrapの標準JS  
　│　├ common.js … 全ページで使用するJS(グロナビetc)  
　│　├ module.js … 全ページで共通で使用するパーツJS(ボタンetc)   
　│　└ pagename.js …  各ページでのみ使用するJS  
　│    
　├ [plugin] … サイトで使われるプラグインを全て格納する  
　│　├ [css] … CSSのプラグイン  
　│　└ [js] …  JSのプラグイン  
　│   
　└ index.html  
 
 
## 命名規則・各言語ルール  

### 共通  
 * 半角英数字のみ使用  
 * 記号は「-」（ハイフン）、「_」（アンダースコア）のみ使用  
 * 原則、英単語を使用  
 * 日本語をローマ字で表記する場合は、[ヘボン式](http://tomari.org/main/java/hebon.html)を使用  
 * インデントはタブ

### HTML  
 * ファイル名はページの内容に適しているものを使用  

### CSS  
 * CSSはheadタグ内で読み込む
 * Bootstrap以外のクラス名を使用する場合は[BEM](https://en.bem.info/)記法をベースに設定     
 * JSでHTMLを操作する場合は、接頭語に「js」をつける(ex:js-xxx)    
 * 1つのHTMLに複数のクラスを用いる場合は、左から下記の優先度で記述  
    1. コンポーネント用クラス(BEM記法ベース)  
    2. Bootstrapクラス  
    3. プラグインクラス  
    4. js用クラス  
 * CSSの記述順番は下記  
  * プロパティ：アルファベット順  
  * ベンダーフレックス：下記の順番で記載  
    1. -webkit-  
    2. -moz-  
    3. -ms-  
    4. -o-  
    5. ベンダープレフィックスなし  
 * メディアクエリのブレイクポイントは下記  
    * PC:1025px~  
    * タブレット:769~1024px  
    * スマートフォン:~768px 

### JavaScript  
 * JSはbodyタグの終了直前で読み込む  
 
 
## 参考URL
 * [BEMの基本概念](https://app.codegrid.net/entry/bem-basic-1)

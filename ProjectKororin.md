<link href="style.css" rel="stylesheet" />

<img src="Markdown_sprite\title.png" width="600" alt="タイトル画像">

---

<br>

<span style="font-size: 30px;">目次</span>
---

> [1. 自己紹介](#1自己紹介)
> <span style="display:block;margin-bottom:0.2em;"></span>
> [2. 作品概要](#2作品概要)
> <span style="display:block;margin-bottom:0.2em;"></span>
> [3. ゲーム紹介](#3ゲーム紹介)<br>
> 　[・ ゲーム内容](#1作品内容)<br>
> 　[・ ルール](#2ルール)<br>
> 　[・ 演出](#3演出)<br>
> 　[・ 操作説明](#4操作説明)
> <span style="display:block;margin-bottom:0.4em;"></span>
> [4. 技術紹介](#4技術紹介)

--- 

<span style="display:block;margin-bottom:3.0em;"></span>  


# 1. 自己紹介

<span style="font-size: 20px;">**所属**</span>
<span style="display:block;margin-bottom:0.1em;"></span>
　　　河原電子ビジネス専門学校　　ゲームクリエイター科</span>

<span style="font-size: 18px;">**名前**</span> 
<span style="display:block;margin-bottom:0.1em;"></span>
　　　三好 爽太　(みよし そうた)</span>

<span style="font-size: 18px;">**メールアドレス**</span> 
<span style="display:block;margin-bottom:0.1em;"></span>
　　　CA01244028@st.kawahara.ac.jp</span>

<span style="display:block;margin-bottom:3.0em;"></span>  

# 2.作品概要


| 項目 | 内容 |
|------|------|
| タイトル | ころりん |
| 制作人数 | 1人 |
| 制作期間 | 2025年9月~2025年12月 |
| ゲームジャンル | 3Dアクションゲーム |
| プレイ人数 | 1人 |
| 対応ハード | PC, Windows11 |
| 対応コントローラー | Xbox360コントローラー |
| エンジン | 学内エンジン(K2Engine), Unity |
| エディタ | VisualStudio2022 |
| 使用言語 | C++, C#, HLSL |
| 3Dモデル | 3DSMax2025 |
| エフェクト | Effekseer |
| 画像 | Adobe Photoshop |
| バージョン管理 | Github, fork |
| GitHub | [githubリンクはこちら](https://github.com/miyosisouta/ProjectKororin) |
| YouTube | [動画リンクはこちら](https://youtu.be/dcFpaZ94y3U) |

<span style="display:block;margin-bottom:3.0em;"></span>


# 3.ゲーム紹介

<br>

<span style="font-size: 22px;">**1. ゲーム内容**</span> 
<span style="display:block;margin-bottom:0.1em;"></span>
　　　ステージ上のオブジェクトを巻き込み塊を大きくする成長型アクションゲーム

<span style="display:block;margin-bottom:2.5em;"></span>


<span style="font-size: 22px;">**2. ルール**</span> 
<span style="display:block;margin-bottom:0.1em;"></span>
> <span style="font-size: 20px;">**くっつけて大きくする**</span> 
> - 街中のオブジェクトに接触すると、自分の塊に巻き込んで大きくすることができます。
> - 小さいものから順に巻き込んでいく戦略性が求められます。</p>

<div class="image-row">
  <img src="Markdown_sprite\beforeAttach.png" width="150" alt="付着前">
  <img src="Markdown_sprite\LightArrow.png" width="100" alt="矢印">
  <img src="Markdown_sprite\afterAttach.png" width="150" alt="付着後">
</div>

---
<br>

> <span style="font-size: 20px;">**大きさによる判定とリスク**</span> 
> - 塊にはレベルがあり、レベル不足の状態で大きなオブジェクトに挑むと弾き飛ばされてしまいます。
> - タイムロスを防ぐため、自分の大きさに合った対象を瞬時に見極める判断力が必要です。

<img src="Markdown_movie\cantAttach.gif" width="450" alt="はじかれる様子">

---
<br>


> <span style="font-size: 20px;">**レベルアップによる探索範囲の拡大**</span> 
> - オブジェクトを一定数巻き込むとレベルアップし、より巨大な物を吸着できるようになります。
> - 今まで障害物だったものが「巻き込める対象」に変わる、カタルシスを感じられる設計にしました。

<img src="Markdown_movie\LevelUpSphere.gif" width="450" alt="レベルアップ"></li>

---
<br>


> <span style="font-size: 20px;">**制限時間とルート構築**</span> 
> - ゲームには制限時間が設定されています。
> - 効率よく大きくするために「どこから攻めるか」というルート構築を考える戦略性が生まれます。

<img src="Markdown_movie\timerUI.gif" width="450" alt="タイマーUI"></li>

---
<br>


> <span style="font-size: 20px;">**視覚的な目標管理**</span> 
> - 「現在の大きさ」と「クリアに必要な目標サイズ」を常に比較表示しています。<br>
> - あとどれくらいでクリアできるかを可視化することで、プレイヤーのモチベーションを維持させます。

<img src="Markdown_movie\SphereSizeTextUI.gif" width="450" alt="サイズUI"></li>

---
<br>


<span style="font-size: 22px;">**3. 演出**</span> 
<span style="display:block;margin-bottom:0.1em;"></span>

> <span style="font-size: 20px;">**ゲームクリア**</span>  
<img src="Markdown_movie/GameClear.gif" width="450" alt="タイマーUI"></li>

<br>

> <span style="font-size: 20px;">**ゲームオーバー**</span>  
<img src="Markdown_movie/GameOver.gif" width="450" alt="タイマーUI"></li>


---

<br>

<span style="font-size: 22px;">**4. 操作説明**</span> 
<span style="display:block;margin-bottom:0.1em;"></span>  

  | 操作 | 説明 |
|------|------|
| 移動（Lスティック） | 塊の移動操作に使用します |
| カメラ操作（Rスティック） | 塊を基点としたカメラ移動操作を行います |
| 決定（Aボタン / トリガー） | 決定操作に使用します |

<br>

> <span style="font-size: 20px;">**ゲームパッド**</span>  
<img src="Markdown_sprite\OperationInstructions.png" width="450" alt="操作説明図">

<br>


# 4.技術紹介

<br>

<span style="font-size: 22px;">**1. 空間分割**</span> 
<span style="display:block;margin-bottom:0.1em;"></span>  
> - AABBを使ってステージ全体で空間分割を行う
> - 塊が存在する空間にあるオブジェクトのみ当たり判定を行う

  <img src="Markdown_sprite\SpaceDivision.png" width="400" alt="空間分割図">

<br>

<span style="font-size: 18px;">【課題】</span>  
　　　全オブジェクト総当たり判定による著しいFPS低下。
<span style="display:block;margin-bottom:0.5em;"></span>
<span style="font-size: 18px;">【結果】</span>  
　　　大量のオブジェクト描画時も60FPS安定動作を実現。

<br>

<img src="Markdown_sprite\SpaceDivisionResult.png" width="500" alt="空間分割結果">  

<br>

---

<br>

<span style="font-size: 22px;">**2. Unityの拡張エディタ**</span> 
<span style="display:block;margin-bottom:0.1em;"></span>  

> -   Unityのエディタ拡張でオブジェクト配置とパラメータ設定を行い、JSON形式で書き出し。
> - 自作エンジンで読み込むことで、レベルデザインの効率を最大化しました。


<img src="Markdown_sprite\UnityScript.png" width="200" alt="Unityスクリプト">
<img src="Markdown_sprite\LightArrow.png" width="80" alt="矢印">
<img src="Markdown_sprite\json.png" width="200" alt="JSON">

<br>

---

<br>

<span style="font-size: 22px;">**3. 吸着判定**</span> 
<span style="display:block;margin-bottom:0.1em;"></span>  

<img src="Markdown_sprite\MatrixCalculation.png" width="450" alt="行列計算">

<br>

---

<br>

<span style="font-size: 22px;">**4. オフスクリーンレンダリング**</span> 
<span style="display:block;margin-bottom:0.1em;"></span> 

> - レンダリングターゲットを切り替えてバッファをクリア。
> - UI用カメラで「くっついた物」のみを描画し、メインシーンと合成して表示。

<img src="Markdown_movie\UnderLeftViewUI.gif" width="500" alt="オフスクリーンレンダリングUI">

<br>

[目次へ戻る](#目次)

---
<link rel="stylesheet" href="style.css">

# ころりん
<img src = "Markdown_sprite\title.png" width = "500">
<br>
<br>


## 目次  
- [1. 自己紹介](#1自己紹介)   
- [2. 作品概要](#2作品概要)  
- [3. ゲーム紹介](#3ゲーム紹介)   
 ・ [ゲーム内容](#1-ゲーム内容)  
 ・ [ルール](#2-ルール)  
 ・ [操作説明](#3-操作説明)  
- [4. 技術紹介](#4技術紹介)


## 1.自己紹介
### **所属**
- 河原電子ビジネス専門学校　　ゲームクリエイター科  
### **名前**
- 三好 爽太(みよし そうた)  


## 2.作品概要
### *タイトル*
ころりん
### *制作人数*
1人
### *制作期間*
2025年9月~2025年12月
### *ゲームジャンル*
3Dアクションゲーム
### *プレイ人数*
1人
### *対応ハード*
PC,Window11
### *対応コントローラー*
Xbox360コントローラー
### *エンジン*
学内エンジン(K2Engine)
### *使用言語*
C++,C#,HLSL
### *プログラム*
VisualStudio2022,Unity
### *3Dモデル*
3DSMax2025
### *エフェクト*
Effeckseer
### *画像*
Adobe Photoshop
### *バージョン管理*
Github,fork
### *GitHubのURL*
<a href="https://example.com/" target="_blank">https://github.com/miyosisouta/ProjectKororin</a>

### *動画リンク(youtube)*
<a href="https://example.com/" target="_blank">https://youtu.be/dcFpaZ94y3U</a>


## 3.ゲーム紹介
#### 1. ゲーム内容  
ステージ上のオブジェクトを巻き込み塊を大きくする成長型アクションゲーム  

---

#### 2. ルール  
- 街中のオブジェクトをくっつけることが出来る。  
<img src = "Markdown_sprite\beforeAttach.png" width = "100">
<img src = "Markdown_sprite\LightArrow.png" width = "100">
<img src = "Markdown_sprite\afterAttach.png" width = "100">  
<br>

---

- 塊にはレベルが設定されている
- 塊のレベルが足りないとき、オブジェクトに引っ付こうとするとはじかれる  
<br>
<img src = "Markdown_movie\cantAttach.gif" width = "300">
<br>

---

- オブジェクトを一定個数引っ付けるとレベルアップ
- より大きいものを吸着可能になる  
<img src = "Markdown_movie\LevelUpSphere.gif" width = "300">

---

- 制限時間がある  
<img src = "Markdown_movie\timerUI.gif" width = "300">

---

- 塊の目標サイズと塊の現在の大きさが表示されている。  
<img src = "Markdown_movie\sphereSizeTextUI.gif" width = "300">

---
#### 3. 操作説明  
<br>
<img src = "Markdown_sprite\OperationInstructions.png" width = "300">

## 4.技術紹介
1. 空間分割
- AABBを使ってステージ全体で空間分割を行う
- 塊が存在する空間にあるオブジェクトのみ当たり判定を行う  
<img src = "Markdown_sprite\SpaceDivision.png" width = "300">  

課題：  
　　全オブジェクト総当たり判定による著しいFPS低下。  
結果：  
　　大量のオブジェクト描画時も安定動作

<img src = "Markdown_sprite\SpaceDivisionResult.png" width = "400">  

---

2. Unityの拡張エディタ
- Unityのエディタ拡張でオブジェクト配置とパラメータ設定を行い、JSON形式で書き出し。
- 自作エンジンで読み込むことで、レベルデザインの効率を最大化しました。  
<br>
<img src = "Markdown_sprite\UnityScript.png" width = "150">
<img src = "Markdown_sprite\LightArrow.png" width = "100">
<img src = "Markdown_sprite\json.png" width = "150">  

---

1. 吸着判定  
- 塊のワールド座標を逆行列にする  
- オブジェクトの拡大・回転・平行移動行列を乗算  
- 逆行列とオブジェクトの行列を乗算
- オブジェクトのローカル行列と塊のワールド行列を乗算  
　　　　　　　　　　↓  
**塊が原点のオブジェクトのワールド行列を求められる**  
<br>
<img src = "Markdown_sprite\CalcMatrix.png" width = "400"> 

---

4. オフスクリーンレンダリング
- レンダリングターゲットを切り替えてバッファをクリア、UI用カメラで「くっついた物」のみ描画。
- メインシーンと合成することでUIとして表示しました。  
<img src = "Markdown_movie\UnderLeftViewUI.gif" width = "400"> 
<br>

---
- [目次に戻る](#jump-目次)   




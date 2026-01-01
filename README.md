# FrostOrtho ビルドガイド

## 組み立て方法

### 



## キーマップの変更方法

### 前提
- GitHubアカウントを作成していること

### Keymap Editor を使用したキーマップ変更方法

1. [ファームウェア用リポジトリ](https://github.com/imo00o/zmk-config-FrostOrtho)へアクセスする。

2. 「fork」をクリックしてリポジトリをフォークする。
![alt text](/img/image-4.png)

3. 「Copy the main-jp branch only」のチェックを外して「Create fork」をクリックする。
![alt text](/img/image-1.png)

4. Create fork をクリックする

5. フォークができたら、Actions タブを開く。
![alt text](/img/image-5.png)

6. 「I understand my workflows, go ahead and enable them」をクリックし、GitHub Actionsを有効化する。
![alt text](/img/image-3.png)

7. [Keymap Editor](https://nickcoutsos.github.io/keymap-editor/)へアクセスする。

8. GitHub を選択する。
![alt text](/img/image-6.png)

9. 「Login with GitHub」をクリックし、画面に従ってログインする。
![alt text](/img/image-7.png)

10. 「Authorize Keymap Editor」をクリックする。
![alt text](/img/image-9.png)

11. 「Add Repository」をクリックする。
![alt text](/img/image-10.png)

12. 「Only select repositories」を選択し、「Select repositories」からzmk-config-FrostOrthoを選択する。  
Installをクリックする。  
![alt text](/img/image-11.png)


13. キーマップ変更画面が表示されたら、使用したい配列に従いブランチを選択してキーマップを編集する。
- 日本語配列用キーマップ：main-jp
- US配列用キーマップ：main-us
![alt text](/img/image-12.png)

14. キーマップの変更が終わったら、「Save」をクリックする。

15. 「Latest」をクリックするとGitHub Actionsの画面へ遷移する。  
ビルドが完了するとファームウェアのダウンロードが可能となるのでダウンロードする。  
※ ビルドには2分程度かかる
![alt text](/img/image-13.png)

### ファームウェアの書き込み方法

1. キーボードとPCをケーブルで接続し、リセットスティックを2回押す

2. 

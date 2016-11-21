# Azure-CLI
acure-cliのインストールとセットアップまとめ



- Cygwinにnode.jsをインストールするメモ

Download site: https://nodejs.org/en/


`$ wget https://nodejs.org/dist/v6.9.1/node-v6.9.1-x64.msi`
`$ msiexec /i node-v6.9.1-x64.msi`

-> cygwinを再起動したら nodeコマンドが使えるようになった

`$ npm install -g azure-cli`

- Azure CLIを使えるようにする

`$ azure config mode asm`
```
info:    Executing command config mode
info:    New mode is asm
info:    config mode command OK
```

`$ azure account download`

- ブラウザで自動で開かれたサイト(ページ)にAzureのアカウントとパスワードを入力する

- 証明書をダウンロードする
`$ vim credentials.publishsettings`

- 証明書をimportする
`$ azure account import credentials.publishsettings`
```
info:    Executing command account import
info:    account import command OK
```

- サービス管理モード
- `$ azure config mode asm`
  - `$ azure account list`
  - `$ azure account env list`

- リソースマネージャーモード 
- `$ azure config mode arm`
   - `$ azure vm list`

  







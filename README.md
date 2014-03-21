# Veewee-definitions

## 構築方法

※CentOS-4.8-i386-ja での構築方法

veeweeをインストールする。

	$ git clone git://github.com/jedi4ever/veewee.git

Veewee-definitionsをveewee/definitionsにコピーする。

必要なISOファイルをveewee/isoにコピーしておく。

 VBOXを作成する。

	$ bundle exec veewee vbox build CentOS-4.8-i386-ja --force

Vagrantのboxファイルをエクスポートする。

	$ bundle exec veewee vbox export CentOS-4.8-i386-ja --force

Vagrant でサーバーを起動する。

	$ vagrant box add 'CentOS-4.8-i386-ja' 'CentOS-4.8-i386-ja.box' --force
	$ vagrant init 'CentOS-4.8-i386-ja'
	$ vagrant up
	$ vagrant ssh

## 残件

*　CentOS-4.8-i386-ja では 、ライブラリが足りないのでchef & Puppetをインストールしないようにコメントアウトしておく。

## 開発者

[ikikko](https://github.com/ikikko)

cli_memo
========

memo tool on CLI(Command Line Interface)

（概要）
本ツールはLinuxなどのコマンドライン上で動作するシンプルなメモツールです。

CUIで作業中に思いついた便利なシェルスクリプトのアイデアなどを素早く記録するために作成しました。

（構成）
cli_memo/
	LICENSE:	MITライセンスです
	README.md:	後に英語で書く予定です
	README(ja):	日本語の本ファイルです。
	memo.py:	プログラム本体です
	memo.csv:	メモが保存されるCSVファイルです。

（動作）
memo.pyを実行すると、
shell>memo:
と帰ってくるので
shell>memo:memo_testi_memo
と打ち込んでエンターすると
memo.csvに日付とともに記録されます。
閲覧は現在のところcatコマンドなどで行います。

（シェルスクリプトとして使用する方法）
ホームディレクトリにclimemoディレクトリを配置する場合

shell>cd cli_memo 		#cli_memoディレクトリへ移動
shell>mv memo.py memo 		#実行時に.pyを打つのは面倒なので短いファイル名に変更

shell>cd ~
shell>vim .bashrc		#bashファイルを編集
  vim>PATH="$PATH":~/cli_memo/ 	#パスを追加で通す
shell>memo
shell>memo:testmemo001

shell>cat cli_memo/memo.csv
20130718,testmemo001		#日付とともにメモが記録されます。

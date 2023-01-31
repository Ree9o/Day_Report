# 取り組んだ課題一覧
- Progate
  - Rails4-5,dozyo2
## わかったこと
- getとpostの使い分け
get:dbを変更しないaction
post:dbを変更するaction
- 変数flash
Railsではフラッシュを表示するために、特殊な変数flashが用意されている。アクションで変数flash[:notice]="文字列"で、flash[:notice]をビューで使うことができる。変数flashは１度表示された後に自動で削除される

- 不正なデータがデータベースに保存されないように、データをチェックする仕組みのことをバリデーションと言う。validatesを用いてカラム名と内容を指定。
{presence: true}を用いることで、「そのカラムの値が存在するかどうか」をチェックすることができる。
validates :検証するカラム,{presence:true}

# 次やること
- Rails続き
# 感じたこと
- 道場難しい。ちらちら過去問見ながらやっているが定着しているかが心配
- railsコース長すぎーっ！！！！reactやりたい！！！！
### 学習時間
7h
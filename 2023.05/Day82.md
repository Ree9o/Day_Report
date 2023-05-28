# 取り組んだ課題一覧
個人的な追加教材
- オブジェクト指向設計実践ガイド
## わかったこと
- 継承
  - スーパークラスは抽象なメソッドのみを定義する（抽象的なスーパークラスを作成する）、具象的なメソッドはサブクラスの責務である（抽象→特化したオブジェクトであるべき）
  - initializeはそのままオーバーライドしない。superの下記忘れで誤爆する可能性があるため。突っ込む用のメソッド（フックメッセージ）定義する。
  例えば
 ``` ruby
    class Main
        def initialize(args = {})
            @name = args[:name]
        end
    end

    class Sub < Main
        def initialize(args)
            @any = args[:any]
        super(any)
        end
    end
```
とやるとsuperを必ず呼ばないといけないのでスーパークラスのinitializeの全容を把握しておく必要がある。それは依存を作っていることになる。
```ruby
    class Main
        def initialize(args = {})
            @name = args[:name]
            post_initialize(args)
        end

        def post_initialize(args)
            nil
        end
    end
    
    class Sub < Main
        #def initialize(args)
        #    @any = args[:any]
        #super(any)
        #end

        def post_initialize(args)
            @age = [:age]
        end
    end
```
とすることで、依存は排除することができる。
- 初期値を得るためにテンプレートメソッドパターンを用いる。
# 次やること

- オブジェクト指向設計実践ガイド 進

# 感じたこと
- initializeの依存のところは目からウロコだった。
- 他にも大事なところがあるがうまく言語化できていないので明日読み直したい。
- ちょっとずつオブジェクト指向プログラミングについて理解ができてきた気がしなくもない
### 学習時間

3h ほど
累計:256h

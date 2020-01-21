# portfolio-java
high and low game


package shimazaki.data;  //パッケージ宣言　クラスをまとめて管理する　　　　　　　　　クラスとは、プログラムを構成するための小さな単位のようなもので機能や働きを示す設計図。
//プロジェクトとは、プログラムを作成するときの1つの単位でプログラムに関する各種情報を管理する
import java.util.Scanner;//　import宣言　「あらかじめ用意されているクラス」を使いたい場合にimport宣言をすると「パッケージ名部分」を省略して書くことができる。
//　キーボードからの値を入力行うため   インポート文と呼ばれるもでキーボード入力を記述するために必要なもの
public class HighAndLow07 {  //cheack  　　　クラス宣言　クラスを自分で作成することをいう　　javaではプログラムを作成するときに必ずこのクラスを活用する

	public static void main(String[] args) {//　　　　mainメソッド　　javaプログラムは原則として必ずこの1文から処理が開始される。　(String[])メインメソッドの中の分が順番に表示される（string）
		// TODO 自動生成されたメソッド・スタブ
		Scanner sc = new Scanner(System.in);//　キーボード入力を促すメッセージの表示　　　　　　データ型 変数名2 = 変数名1.メソッド名;　　　キーボード入力のための準備を行っている　　メソッド名はnextLineとか
		//インデントは「字下げ」
		System.out.println("***************"); //命令文　　　処理される　　最後にセミコロンをつける
		System.out.println("* High & Low *");
		System.out.println("***************");

		/*　int型整数　　　float型、double型小数を扱う　　　char型1文字を扱う　　　　　　boolean型　論理地を扱う　「基本データ型」　　　　string型文字列を扱う　「参照型」	*/
		//　変数　データ値を保持しておく箱　　数値リテラル・文字列リテラル　　　　変数を変数に代入

		while(true) {//ループ文　　　　for繰り返しの回数があらかじめ決定できる場合for(式1 int i = 0 ;式2 i<3 ; 式3 i++ )　　　while文　指定された条件式が成立する間だけ同じ処理を繰り返す　while(条件式)
		System.out.println("   [問題表示]");


			int leftCard = (int)(Math.random()*9)+1; //cheak　math 何をしているのか　　random数字はなぜ。intに代入している


			System.out.println("*****   *****");// 算術演算子　四則演算　　　　
			System.out.println("*   *"  +  "   * * * ");//   +の意味は加算＆文字列の連結（結合）を意味している
			System.out.println("* "+leftCard +" *" + "   * * *  ");
			System.out.println("*   *" + "   * * *  ");
			System.out.println("*****   *****");

			//   ++a  インクリメント　　　--a　デクリメント　　　演算子

			System.out.print("Hogh or Low ? (h/l) > ");
				String select = sc.nextLine();//　　記述したデータ型の変数を宣言し、そこにキーボードで入力した値を代入している　　　データ型 変数名2 = 変数名1.メソッド名;

				if(select.equals("h")) {//　if文　　　文字列.equals(文字列)　文字列の比較　
					System.out.println("→Highを選択しました。");
				}else {
					System.out.println("→Lowを選択しました。");
				}

				System.out.println("   [結果表示]");

				int rightCard = (int)(Math.random()*9)+1;

				System.out.println("*****   *****");
				System.out.println("*   *"  +  "   *   * ");
				System.out.println("* "+leftCard +" *" + "   * "+ rightCard + " *  ");
				System.out.println("*   *" + "   *   *  "); // + 文字列
				System.out.println("*****   *****");
				String result = null;//　null判定　　結果はboolenで得られ、対象がnullの場合trueが得られます。

				if(leftCard<rightCard) {//  関係演算子　>  < ==など
					result = "h";
				}else if(leftCard>rightCard) {
					result = "l";
				} else {
					result = select;
				}

				if(select.equals(result)) {
					System.out.println("→You Win!");

				} else {
					System.out.println("→You Lose...");
					break;
				}

		}
		System.out.println("-- ゲーム終了 --");

	} //while文　
}



# extension Functions
~~~
java的專案有很多工具classes,例如StringUtils, ListUtils,AndroidUtils。主要原因是java沒有支援function,因此只能將一些工具加入至class的static functions。
~~~
	//原本android使用的訊息框架
	Toast.makeText(context, text, Toast.LENGTH_SHORT).show();
	
	
	//在AndroidUtils內加入static method
	public class AndroidUtils {

### 使用extension擴充Context的功能
	fun Context.toast(text: String) { //擴充Context的method
		Toast.makeText(this, text, LENGTH_LONG).show() 

### 更簡潔的使用
	

### 明確使用this
	fun Collection<Int>.dropPercent(percent: Double) = this.drop(floor(this.size * percent) 

### 可以省略使用this
	fun Collection<Int>.dropPercent(percent: Double) = drop(floor(size * percent))

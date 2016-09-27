# Util_Date&Time
 
 ![](./app/src/main/res/mipmap-xhdpi/ic_date.png "")
 ![](./app/src/main/res/mipmap-xhdpi/ic_time.png "") 
## apk
[Util-1.0.1-sample.apk](https://github.com/Sing1/Util/blob/master/app.apk)
## gradle:
```groovy
dependencies {
    ...
    compile 'sing.util:library:1.0.2'
}
```
## Maven:
```xml
<dependency>
  <groupId>sing.util</groupId>
  <artifactId>library</artifactId>
  <version>1.0.2</version>
  <type>pom</type>
</dependency>
```
## sample 
```JAVA    
/**
 * 设置时间 
 */ 
public void chooseTime(View v){
　　DateTimeUtil.getInstance().showTime(this, new DateTimeUtil.DataCallBack() {
　　　　@Override
　　　　public void getData(String date) {
　　　　　　textView.setText(date);
　　　　}
　　},-1, -1);// 默认小时、分钟，-1为当前时间
}
 

/**
 * 设置设置日期
 * @param v
 */
public void chooseDate(View v){
　　DateTimeUtil.getInstance().showDate(this, new DateTimeUtil.DataCallBack() {
　　　　@Override
　　　　public void getData(String date) {
　　　　　　textView.setText(date);
　　　　}
　　},-1,-1,-1);// 默认年、月、日,-1为当前日期
}

/**
 * 设置日期+时间
 * @param v
 */
public void chooseTimeDate(View v){
　　DateTimeUtil.getInstance().showDialogPicker(this, new DateTimeUtil.DataCallBack() {
　　　　@Override
　　　　public void getData(String date) {
　　　　　　textView.setText(date);
　　　　}
　　},-1, -1,-1,-1,-1);// 默认小时、分钟、年、月、日
}
```

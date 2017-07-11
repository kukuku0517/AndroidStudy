# 툴바와 프래그먼트 그리고 머티리얼디자인 살펴보기
## 툴바의 이해
[참고사이트1](https://developer.android.com/reference/android/support/v7/widget/Toolbar.html)<br>
[참고사이트2](https://guides.codepath.com/android/Using-the-App-Toolbar)<br>

### 기본 내용
 툴바는 액션바를 일반화하여 앱 레이아웃 내부에서 사용할 수 있도록 만든 것이다. 액션바는 액티비티의 창을 장식하는 컨트롤 장치중 하나지만 툴바는 여러 용도로 뷰 내부에 존재할 수 있다. 툴바를 액션바로 사용하려면 setSupportActionBar() 메소드를 사용하면 된다.

### 툴바의 특징
1. 네비게이션 버튼
2. 브랜드 로고 이미지
3. 제목 및 부제목
4. 하나 이상의 커스텀 뷰
5. 액션 메뉴 

### 툴바 생성
#### XML Code
```xml
<android.support.v7.widget.Toolbar
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:background="@color/colorPrimary">
	// 이미지뷰
    <ImageView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:src="@mipmap/ic_launcher_round"/>
	// 텍스트뷰
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="This is ToolBar"
        android:textColor="#ffffff"
        android:textSize="20sp"/>
</android.support.v7.widget.Toolbar>
```
![ToolBar](./Imgs/ToolBar.JPG)

### 툴바의 패딩
툴바는 기본적으로 양옆, 위아래에 Padding이 존재한다. 이를 없애주기 위해서 속성을 추가해주어야한다.
```xml
xmlns:app="http://schemas.android.com/apk/res-auto"
app:contentInsetStart="0dp"
app:contentInsetEnd="0dp"
```

### App bar로 사용하기
툴바는 앱바로 사용할 수 있다. 앱바로 사용하기 위해서 기본적인 속성을 추가해주어야 한다.

1. 매니페스트의 어플리케이션 속성을 추가해준다.
```xml
<application
    android:theme="@style/Theme.AppCompat.Light.NoActionBar"
    />
```
2. Activity에서 메소드를 호출한다.
```java
@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
    Toolbar toolbar = (Toolbar)findViewById(R.id.tool_bar);
    setSupportActionBar(toolbar);
}
```
![AppBar](./Imgs/AppBar.JPG)
#### App bar에서 사용가능한 메소드들
- getSupportActionBar().setDisplayShowTitleEnabled(false); // 타이틀 삭제
- getSupportActionBar().setDisplayUseLogoEnabled(true); // 로고 활성화
- getSupportActionBar().setLogo(resource); // 로고 설정

### 툴바의 부가 기능
#### Navigation Drawer와 함께 어울리기
- DrawerLayout
- ActionBarDrawerToggle
#### Menu와 함께 어울리기 
- setSupportActionBar()
- onCreateOptionsMenu()
- onOptionsItemSelected()
#### 앱바 숨기기
- 숨길 툴바 속성
```xml
app:layout_scrollFlags="scroll|enterAlways"
```
- 위치가 함께 옮겨질 뷰의 속성
```xml
app:layout_behavior="android.support.design.widget.AppBarLayout$ScrollingViewBehavior"
```
- 반드시 CoordinatorLayout안에 툴바와 옮겨질 뷰가 들어가 있어야 한다!

## 프래그먼트의 이해
[참조사이트](https://developer.android.com/guide/components/fragments.html?hl=ko)<br>

## 프래그먼트를 활용한 화면 구성
## CoordinatorLayout, CollapsingToolbarLayout
## 머티리얼 디자인의 이해
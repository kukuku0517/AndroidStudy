#안드로이드 뷰 컨테이너 살펴보기
- ## 스크롤뷰 ##
```xml
<ScrollView xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="wrap_content" >

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:orientation="vertical" >

        <TextView
            android:layout_width="match_parent"
            android:layout_height="200dip"
            android:background="#ff0000"
            android:gravity="center"
            android:text="#ff0000" />

        <TextView
            android:layout_width="match_parent"
            android:layout_height="200dip"
            android:background="#00ff00"
            android:gravity="center"
            android:text="#00ff00" />

        <TextView
            android:layout_width="match_parent"
            android:layout_height="200dip"
            android:background="#0000ff"
            android:gravity="center"
            android:text="#0000ff" />
    </LinearLayout>

</ScrollView>
```
![ScrollView](ScrollView.JPG)
- ## 수평 스크롤뷰 ##
```xml
<HorizontalScrollView xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent" >

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:orientation="horizontal" >

        <TextView
            android:layout_width="200dip"
            android:layout_height="match_parent"
            android:background="#ff0000"
            android:gravity="center"
            android:text="#ff0000" />

        <TextView
            android:layout_width="200dip"
            android:layout_height="match_parent"
            android:background="#00ff00"
            android:gravity="center"
            android:text="#00ff00" />

        <TextView
            android:layout_width="200dip"
            android:layout_height="match_parent"
            android:background="#0000ff"
            android:gravity="center"
            android:text="#0000ff" />
    </LinearLayout>

</HorizontalScrollView>
```
![HorizontalScrollView](HorizontalScrollView.JPG)
- ## 뷰페이저 ##
- ## 데이트피커 ##
- ## 타임피커 ##
- ## 리사이클러뷰 ##
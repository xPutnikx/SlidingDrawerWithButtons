SlidingDrawerWithButtons(<a href="https://play.google.com/store/apps/details?id=v.hudnitsky.demo.slider">Google Play Demo</a>)
========================
SlidingDrawerWithButtons is an Open Source Android project that allows developers to easily create applications with sliding drawers with some context if you close drawer. Feel free to use it all you want in your Android apps provided that you cite this project and include the license in your app.

If you are using SlidingDrawerWithButtons in your app and would like to be listed here, please let me know via Twitter!

Also, you can follow my on Twitter : https://twitter.com/VKhudnitsky.

XML Usage

If you decide to use SlidingMenu as a view, you can define it in your xml layouts like this:

 <v.hudnitsky.demo.slider.widget.MultiDirectionSlidingDrawerWithButtons
        android:layout_width="450dp"
        android:layout_height="fill_parent"
        android:orientation="vertical"
        android:layout_alignParentRight="true"
        xmlns:my="http://schemas.android.com/apk/res/v.hudnitsky.demo.slider"
        android:id="@+id/drawer_right"
        my:direction="rightToLeft"
        my:handle="@+id/slider"
        my:buttons="@+id/buttons"
        my:content="@+id/body">
        <RelativeLayout
            android:orientation="vertical"
            android:layout_width="40dp"
            android:layout_height="fill_parent"
            android:id="@+id/slider"
            android:focusable="false"
            android:clickable="false">

            <Button
                android:layout_width="60dp"
                android:layout_height="120dp"
                android:layout_centerVertical="true"
                android:id="@+id/button4"
                android:background="@drawable/sliding_drawer_handle_right" />
        </RelativeLayout>
        <LinearLayout
            android:layout_width="60dp"
            android:layout_height="wrap_content"
            android:orientation="vertical"
            android:layout_centerVertical="true"
            android:padding="10dp"
            android:background="@drawable/pattern1"
            android:id="@+id/buttons"
            android:layout_alignParentLeft="false"
            android:layout_marginLeft="0dp"
            android:layout_alignParentTop="false"
            android:layout_marginTop="0dp"
            android:focusable="false">

            <Button
                style="?android:attr/buttonStyleSmall"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="New Button"
                android:id="@+id/button"
                android:focusable="false"/>

            <Button
                style="?android:attr/buttonStyleSmall"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="New Button"
                android:id="@+id/button2"
                android:focusable="false"/>
        </LinearLayout>

        <RelativeLayout
            android:layout_width="400dp"
            android:layout_height="fill_parent"
            android:background="#9e9e9e"
            android:id="@+id/body"
            android:layout_toRightOf="@+id/all_buttons"
            android:orientation="horizontal"
            android:animateLayoutChanges="true">

            <include
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                layout="@layout/pen_content" />
        </RelativeLayout>

    </v.hudnitsky.demo.slider.widget.MultiDirectionSlidingDrawerWithButtons>
NOTE : you cannot use both behindOffset and behindWidth. You will get an exception if you try.
 <attr name="direction">
        <enum name="rightToLeft" value="0" />
        <enum name="bottomToTop" value="1" />
        <enum name="leftToRight" value="2" />
        <enum name="topToBottom" value="3" />
  </attr>

    <declare-styleable name="MultiDirectionSlidingDrawerWithButtons">
        <attr name="handle" format="reference" />
        <attr name="content" format="reference" />
        <attr name="buttons" format="reference" />
        <attr name="direction" />
        <attr name="bottomOffset" format="dimension"  />
        <attr name="topOffset" format="dimension"  />
        <attr name="allowSingleTap" format="boolean" />
        <attr name="animateOnClick" format="boolean" />
    </declare-styleable>
handle - a reference to the layout that you want to use as the above view of the SlidingDrawerWithButtons
content - a reference to the layout that you want to use as the behind view of the SlidingDrawerWithButtons
buttons - a reference to the layout that you want to use as other elements view of the SlidingDrawerWithButtons
direction - a direction open slidingdrawer

Your layouts have to be based on a viewgroup.
Developed By

Vladimir Hudnitsky

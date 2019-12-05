# 一些控件组

1、ChangeColorTextView (修改特定文字颜色)

     设置点击
     txt.setMovementMethod(LinkMovementMethod.getInstance());
     设置文本跟要变色的文字 颜色
     txt.setSpecifiedTextsColor(整段内容, 想要变色的文字, 想要变色的文字颜色);

2、CustomDatePicker（时间选择）

    设置点击
    txt.setMovementMethod(LinkMovementMethod.getInstance());
    设置文本跟要变色的文字 颜色
    txt.setSpecifiedTextsColor(整段内容, 想要变色的文字, 想要变色的文字颜色);

2、CustomDatePicker（时间选择）

      CustomDatePicker customDatePicker = new CustomDatePicker(context, 开始时间, 结束时间, 标题文本, 标题颜色,
                        确定文本, 确定文本颜色, 取消文本, 取消文本颜色, 当前时间,
                        new CustomDatePicker.OnPickListener() {
                            String t;

                            @Override
                            public void onPick(boolean set, @Nullable String time) {

                            }
                        });
3、InfiniteCirclePageIndicator（小红书指示器）

       配合ViewPager使用
       indicator.setCount(列表的size, 最大显示size, 选中位置);
       viewPager.addOnPageChangeListener(indicator);

 4、LabelsView（标签）
 

                   
     设置数据源
     labels.setLabels(list);
     设置点击监听
     labels.setOnLabelClickListener(new LabelsView.OnLabelClickListener() {
           @Override
           public void onLabelClick(TextView label, Object data, int position) {

         配合ViewPager使用
         indicator.setCount(列表的size, 最大显示size, 选中位置);
         viewPager.addOnPageChangeListener(indicator);

 4、LabelsView（标签）

            设置数据源
            labels.setLabels(list);
            设置点击监听
            labels.setOnLabelClickListener(new LabelsView.OnLabelClickListener() {
            @Override
            public void onLabelClick(TextView label, Object data, int position) {

                 }
                });
                
     <com.nhl_lib.view.weight.LabelsView xmlns:
        app="http://schemas.android.com/apk/res-auto"
        android:id="@+id/labels"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:minHeight="25dp"
        app:labelBackground="@drawable/xunme_label_bg"  //背景色（点击跟未点击）
        app:labelTextColor="@drawable/xunme_label_text_color"  //文字颜色（点击跟未点击）
        app:labelTextPaddingBottom="3dp"
        app:labelTextPaddingLeft="12dp"
        app:labelTextPaddingRight="12dp"
        android:layout_gravity="center"
        app:labelTextPaddingTop="3dp"
        app:labelTextSize="13sp"
        app:lineMargin="10dp"
        app:maxSelect="0"   //最大选择（默认为0）
        app:minSelect="1"   //最小选择
        app:selectType="MULTI"   //选中类型（单选多选）
        app:wordMargin="10dp" />

5、LastInputEditText（输入光标一直在最后）

     像EditText一样在布局文件中导入


6、CounterView(计数器)

    设置最大值
    cvCounter.setMaxValue(stock);
    设置回调
    cvCounter.setCallback(new IChangeCountCallback() {
            @Override
            public void change(int count) {

            }
        });

7、ShadowRelativeLayout (相对布局阴影、还有约束布局，线性布局)


        <com.nhl_lib.view.shadow.ShadowRelativeLayout
                android:id="@+id/sl_view_0"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:background="@color/white"
                app:l_radius="5dp"
                app:l_shadowAlpha="0.3"
                app:l_shadowElevation="5dp">

         </com.nhl_lib.view.shadow.ShadowRelativeLayout>

8、RxPermissions （获取权限）

        RxPermissions   rxPermissions = new RxPermissions(this);
        rxPermissions.request(需要获取的单个权限or多个权限).subscribe(new Observer<Boolean>() {
            @Override
            public void onSubscribe(Disposable d) {
            }
            @Override
            public void onNext(Boolean aBoolean) {
                if (aBoolean) {
                 //获取了权限
                } else {
                 //拒绝权限
                }
            }
            @Override
            public void onError(Throwable e) {

            }

            @Override
            public void onComplete() {

            }
        });

9、ImageViewRoundOval (实现圆形、圆角，椭圆等自定义图片)

             <view.tomato.com.common.weight.ImageViewRoundOval
                  android:id="@+id/igv_photo"
                  android:layout_width="match_parent"
                  android:layout_height="match_parent"
                  android:scaleType="centerCrop" />
               设置显示类型
               igv_head.setType(ImageViewRoundOval.TYPE_CIRCLE);


# Android_ratingbarview
###### a RatingBarView and you can set Image and count
###### 一个评分控件，可以设置图片和个数,并且总体评价可以为folat

![image](https://github.com/ysq1051838264/Android_ratingbarview/blob/master/1.jpg)
### Usage

#### In XML  Directly

    <com.ysq.android_ratingbarview.RatingBarView
        android:id="@+id/starView"
        bao:starImageSize = "22dp"
        bao:starCount = "7"
        bao:starEmpty = "@drawable/icon_star_empty"
        bao:starFill = "@drawable/icon_star_fill"
        android:layout_centerInParent="true"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content">
    </com.ysq.android_ratingbarview.RatingBarView>
    
#### In Java Code

        RatingBarView ratingBarView = (RatingBarView)findViewById(R.id.starView);
        ratingBarView.setmClickable(true);
        //you can set up view here or in XML

        //ratingBarView.setStarCount(5);
        //ratingBarView.setStarEmptyDrawable(...);
        //ratingBarView.setStarFillDrawable(...);
        //ratingBarView.setStarImageSize();

        //bind some data
        ratingBarView.setBindObject(1);
        ratingBarView.setOnRatingListener(new RatingBarView.OnRatingListener() {
            @Override
            public void onRating(Object bindObject,int RatingScore) {
                Toast.makeText(MainActivity.this ,"bindObject : "+bindObject,Toast.LENGTH_SHORT).show();
            }
        });




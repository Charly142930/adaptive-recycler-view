<img src="media/ic_app.png" height="100px" />

Adaptive Recycler View
=============

![Travis CI](https://img.shields.io/travis/fartem/adaptive-recycler-view)
![Open issues](https://img.shields.io/github/issues-raw/fartem/adaptive-recycler-view.svg?color=ff534a)

About
-------------

Library for creating RecyclerView with warning message of data availability.

Usage
-------------

### Code

Put `AdaptiveRecyclerView` and `AdaptiveMessageView` in same layout file.

__Configure `AdaptiveMessageView`:__

Java / Kotlin:
```java
adaptiveMessageView.setImage(messageImage);
adaptiveMessageView.setMessageText(messageText);
```

__`AdaptiveMessageView` mathods__:

* `setImage(imageResId: Int)` - set drawable for image from resource id;
* `setImage(drawable: Drawable)` - set drawable for image;
* `setMessageText(messageResId: Int)` - set text for message from resource id; 
* `setMessageText(message: String)` - set text for message.

__Configure `AdaptiveRecyclerView`:__

Java:
```java
adaptiveRecyclerView.setMessageView(adaptiveMessageView);
```

Kotlin:
```kotlin
adaptive_recycler_view.messageView = adaptive_message_view
```

__`AdaptiveRecyclerView` mathods__:

* `setMessageView(messageView: View)` - set message view.

### AdaptiveRecyclerView

Declaring as an AndroidX RecyclerView (Layout manager can be set up from code).

```xml
<com.smlnskgmail.jaman.adaptiverecyclerview.AdaptiveRecyclerView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        app:layoutManager="androidx.recyclerview.widget.LinearLayoutManager" />
```

__AdaptiveMessageView__

Must be declared in layout with AdaptiveRecyclerView. It can be customized with parameters (all available parameters contains in example with `arv`).
```xml
<com.smlnskgmail.jaman.adaptiverecyclerview.AdaptiveMessageView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        arv:message_image="@drawable/ic_error"
        arv:message_image_tint="@color/colorPrimary"
        arv:message_text="@string/text_message_list"
        arv:message_text_color="@color/colorPrimary" />
```

__`AdaptiveMessageView` parameters:__

* `message_image` - set custom image;
* `message_image_tint` - set tint for image (default or custom);
* `message_text` - set message text;
* `message_text_color` - set message text color.

__If you want to use default image or text, you can override dimension from the library:__

* `adaptive_message_view_text_margin_top` - distance between image and message, in dp;
* `adaptive_message_view_image_size` - image size, in dp;
* `adaptive_message_view_text_size` - message text size, in sp.

__Default strings keys for elements:__

* `adaptive_message_view_text` - message text;
* `adaptive_message_view_content_description` - image content description.

Gradle dependency
-------------



Contributors
-------------

* [@fartem](https://github.com/fartem) as Artem Fomchenkov
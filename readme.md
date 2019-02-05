# Cocos2d-x 2.2.6 support Android Studio IDE and cocos command

Tested with 3.8.1 console command, Android Studio 3.2.1.

## setup

1. copy `hello` folder to `cocos2d-x-2.2.6/project/`
2. copy `libcocos2dx` folder to `cocos2d-x-2.2.6/cocos2dx/platform/android`


## run with cocos command

cocos command version < 3.17
```
cocos run -p android --android-studio
```



# Debug C++

1.  NDK >= android-ndk-r13b

2.  Set Project's NDK![](misc/setting1.png)

    ![](misc/setting2.png)

3.  Android.mk

    ```makefile
    # !!!! dangerous, ONLY for debuging c++ with Android Studio
    ifeq ($(NDK_DEBUG),1)
      LOCAL_ALLOW_UNDEFINED_SYMBOLS := true
    endif
    # !!!! dangerous!!!!
    ```

<p>Support update 3rd libs via PayPal:
<br>  <a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&amp;hosted_button_id=P7H86JDPVCA3E" rel="nofollow"><img src="https://camo.githubusercontent.com/bce14c8e2e39ba0464551b34602b4c60c182526b/68747470733a2f2f7777772e70617970616c6f626a656374732e636f6d2f656e5f55532f692f62746e2f62746e5f646f6e6174655f4c472e676966" alt="PayPal" data-canonical-src="https://www.paypalobjects.com/en_US/i/btn/btn_donate_LG.gif" style="max-width:100%;"></a> $100, $500, $1000, others.</p>

ref to https://github.com/c0i/cocos2d-x-v2

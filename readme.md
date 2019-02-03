# Cocos2d-x 2.2.6 support Android Studio IDE and cocos command

Tested with 3.8.1 console command

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

    ​


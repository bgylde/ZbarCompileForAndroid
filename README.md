# ZbarCompileForAndroid
Compile zbar shared library with android ndk toolchain.

默认已经配置好ndk编译链环境(arm-linux-androideabi-gcc).

首先在libiconv-1.15.2执行make，生成libiconv.so，然后在ZBar-master中执行make命令，生成libzbar.so。

ps:如果android中的zbar文件路径与默认的不同，需要修改ZBar-master/java/zbarjni.c中的函数名，可以用jni命令生成相应的头文件，然后修改函数名。

## 相机内参标定

### 1. 执行python脚本生成 names.txt

修改 `export_path.py`中 `pic_paths` 为标定图片所在路径（注意：==* 路径最后要加上 ‘ / ’ *==），执行完成后会在 `export_path.py` 同级目录下生成 `names.txt`

### 2.新建目录并修改 `calib_intrinsic.cpp` 文件中的路径，

1. 在 `src` 同级目录下新建 `temp_and_result/drawChessboardCorners`   和 `temp_and_result/resultImages` 两个目录
2. 修改路径1：该文件 14 行路径
3. 修改路径2：该文件 15 行路径
4. 修改路径3：该文件 58行路径
5. 修改路径4：该文件 189行路径
6. 修改路径5：该文件 219行路径

### 3.编译c++程序

```bash
mkdir build && cd build
cmake ..
make -j
# 编译完成后会在 build 目录下生成 calib_intrinsic 可执行文件
# 并在 temp_and_result 目录下生成 中间结果以及 caliberation_result.txt
```


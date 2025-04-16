# GB22401 インタラクティブCG

https://kdb.tsukuba.ac.jp/syllabi/2024/GB22401/jpn

## Macでfltkをビルド
```bash
cd fltk
autoconf
CXXFLAGS="-Wno-c++11-narrowing -Wno-register" CC=clang CXX=clang++ ./configure --enable-threads --enable-shared
sed -i '' 's|<fp\.h>|<math.h>|g' png/pngpriv.h
sed -i '' 's|(int(\*)(\(const void\*,const void\*\)))sort)|(int(*)(const struct dirent**, const struct dirent**))sort)|g' src/filename_list.cxx
sed -i '' 's|friend Fl_Widget \*make_type_browser(int,int,int,int,const char \*l=0);|friend Fl_Widget \*make_type_browser(int,int,int,int,const char \*l);|g' fluid/Fl_Type.h
sed -i '' 's|\*bufptr++ = \*temp++);|\*bufptr++ = \*temp++\n              );|g' fluid/CodeEditor.cxx
make
```
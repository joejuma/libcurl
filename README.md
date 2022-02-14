# libcurl
Precompiled LibCURL

## How to Use
1. Download
2. Unzip into your project directory
3. Add the `include` file to the includes.
4. Add the `libs` file to the libs.
5. add the following to the linker, `libcurl_a.lib;Ws2_32.lib;Crypt32.lib;Wldap32.lib;Normaliz.lib`
6. Do `#include <curl/curl.h>` in whatever file you want to use it in.
7. You should be good!

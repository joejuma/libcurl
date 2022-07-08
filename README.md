# libcurl
This is a repo containing a precompiled version of the C++ cURL library, libcURL. This was built for both x86 and x64 projects in Visual Studio 2019 (VS version 16).

## How to Use
1. Download the *.zip file, and extract the `curl` folder inside wherever you want the curl dependencies to be in your project.
2. Open your project configuration in Visual Studio.
3. Add the `include` directory for your respective build in the C++ additional include directories section.
4. Add the `libs` directory for your respective build in the linker's additional directories section.
5. Also add the following to the linker, `Normaliz.lib;Ws2_32.lib;Wldap32.lib;Crypt32.lib;advapi32.lib;` in every config.
6. Then add either the `libcurl_a.lib` or `libcurl_a_debug.lib` dependency to the linker depending on your build.
7. Add `#define CURL_STATICLIB` right before the curl include, then add the curl include (`#include <curl/curl.h>`).
8. You should be all set to use curl now!

## Testing if it worked
Add the following boilerplate curl code to part of your program to test if everything is working.
```
CURL* curl = curl_easy_init();
if(curl)
{
    // Success
    curl_easy_cleanup(curl);
}
else
{
    // Failed.
};
```
If you compile this successfully, it should be all set. Additionally, feel free to test out by adding print-out statements where the `// Success` and `// Failed.` comments are in the above code.

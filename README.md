# Cheba_apis
api for cheba_apis.vercel.app random animal site
# main
```cpp
#include "Cheba_apis.h"
#include <iostream>

int main() {
   Cheba_apis api;
    auto animal = api.random_animal().then([](json::value result) {
        std::cout << result<< std::endl;
    });
    animal.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```

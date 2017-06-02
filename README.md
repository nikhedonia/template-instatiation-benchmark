# simple benchmark to compare code generation vs. template instatiations


```


g++ -std=c++14 main_tmpl.cpp -E > main_tmpl_pp.cpp
g++ -std=c++14 main.cpp -E > main.pp.cpp

time `for i in {1..100}; do  g++ -std=c++14 main.cpp;  done`
time `for i in {1..100}; do  g++ -std=c++14 main.pp.cpp;  done`
time `for i in {1..100}; do  g++ -std=c++14 main_tmpl.cpp;  done`
time `for i in {1..100}; do  g++ -std=c++14 main_tmpl.pp.cpp;  done`

```


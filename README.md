2 + 3


```python
print("Hello")

```

    Hello



```python
%lsmagic 
```




    Available line magics:
    %alias  %alias_magic  %autoawait  %autocall  %automagic  %autosave  %bookmark  %cat  %cd  %clear  %colors  %conda  %config  %connect_info  %cp  %debug  %dhist  %dirs  %doctest_mode  %ed  %edit  %env  %gui  %hist  %history  %killbgscripts  %ldir  %less  %lf  %lk  %ll  %load  %load_ext  %loadpy  %logoff  %logon  %logstart  %logstate  %logstop  %ls  %lsmagic  %lx  %macro  %magic  %man  %matplotlib  %mkdir  %more  %mv  %notebook  %page  %pastebin  %pdb  %pdef  %pdoc  %pfile  %pinfo  %pinfo2  %pip  %popd  %pprint  %precision  %prun  %psearch  %psource  %pushd  %pwd  %pycat  %pylab  %qtconsole  %quickref  %recall  %rehashx  %reload_ext  %rep  %rerun  %reset  %reset_selective  %rm  %rmdir  %run  %save  %sc  %set_env  %store  %sx  %system  %tb  %time  %timeit  %unalias  %unload_ext  %who  %who_ls  %whos  %xdel  %xmode
    
    Available cell magics:
    %%!  %%HTML  %%SVG  %%bash  %%capture  %%debug  %%file  %%html  %%javascript  %%js  %%latex  %%markdown  %%perl  %%prun  %%pypy  %%python  %%python2  %%python3  %%ruby  %%script  %%sh  %%svg  %%sx  %%system  %%time  %%timeit  %%writefile
    
    Automagic is ON, % prefix IS NOT needed for line magics.




```python
%automagic OFF
```

    
    Automagic is OFF, % prefix IS needed for line magics.



```python
d = {'US': 'USA', 'FR': 'Francr'}
res = 1 + 2
print(d)
res
```

    {'US': 'USA', 'FR': 'Francr'}





    3




```python
%page d
```


    {'FR': 'Francr', 'US': 'USA'}



```python
%whos
```

    Variable   Type    Data/Info
    ----------------------------
    d          dict    n=2
    res        int     3


#### Удаляет переменные, которые были определены пользователем 


```python
%reset_selective -f res
```


```python
%whos
```

    Variable   Type    Data/Info
    ----------------------------
    d          dict    n=2


#### Время выполнения программы. Альтернатива - %%time или %%timeit


```python
import time

start = time.time()

for i in range (100000):
    pass

time.time() - start
```




    0.005372285842895508




```python
%%time

for i in range (100000):
    pass
```

    CPU times: user 5.33 ms, sys: 0 ns, total: 5.33 ms
    Wall time: 5.34 ms


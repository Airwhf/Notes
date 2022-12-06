# PseudoNetCDF学习笔记

## Release Notes

### 2022年11月22日



## 官方教程更正

1. 通过`pnc.pncopen`打开GRIDDESC文件时，需要再后面添加`GRIDNAME`的关键字，如下代码中`GDNAM="12US1"`所示，否则会出现报错，包括`SDATE`和`TSTEP`等都可以直接写入参数中。

```python
import PseudoNetCDF as pnc
gf = pnc.pncopen('GRIDDESC', format='griddesc', GDNAM="12US1", SDATE=2016001, TSTEP=10000)
# gf.SDATE = 2016001
# gf.TSTEP = 10000
```




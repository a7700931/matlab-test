# Matlab 筆記
------
## 解決index排序
```
ds = tabularTextDatastore('largedump.txt'); 
largedump = table2array(readall(ds));

cutnum = repmat(1152,1,51);
largedumpc = mat2cell(largedump,cutnum);
largedumpr = cell2mat(cellfun(@sortrows,largedumpc,'Un',0));
```

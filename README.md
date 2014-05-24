Git 忽略規則範本<br />Git ignore rules template
================
如何使用<br />How to use
-------------------
Copy &lt;rule name&gt;.gitignore file to .gitignore and place it in the target directory to make effect.

If the file is named &lt;rule name&gt;**.template**.gitignore means that this template contains some rules needed to be manually copied from other files.  This is for simplifying design and maintain development-friendliness.

.gitignore 用途
----------------
避免git將不想add至staging area的檔案（如可由原始程式碼生成的檔案）add到staging area中。

.gitignore語法
--------------
* 可以使用 glob patterns  
[http://en.wikipedia.org/wiki/Glob_%28programming%29]
* 以「#」開頭的列為單行註解
* \*.so←不track副檔名為so的檔案
* !trackThis.so←即使有*.so也會track此檔案
* /FILE←只不track根目錄的FILE檔案
* build/←忽略build目錄下的所有檔案
* doc/*.txt←doc/a.txt會被忽略但是doc/a/b.txt則不會被忽略（那怎樣才能忽略呢？）

注意事項
----------------
* 後方的規則會覆蓋前方的規則，例如排除.gitignore檔案的排除的規則如果放在排除.*檔案的規則前則會無效。
* 規則不能用tab字元或是空白縮排...

授權條款<br />License
-------------------
The content from this project is licensed by CC-BY 3.0 or later versions.
However the combination of content from this project to any software project is not restricted.
# Reference Citation Guide / 参考文献引用方式

All references are maintained in `mlsys.bib`.

所有参考文献统一维护在 `mlsys.bib` 中。

## Adding Bibliography Entries / 添加文献条目

Add a BibTeX entry to `mlsys.bib`. Before adding, search for existing keys to avoid duplicates:

在 `mlsys.bib` 中添加 BibTeX 格式的条目，添加前请先检索是否已存在同名 key：

```bibtex
@inproceedings{cnn2015,
  title    = {CNN},
  author   = {xxx},
  year     = {2015},
  keywords = {xxx}
}
```

## In-text Citations / 正文引用

A space is required before the citation directive:

引用时前面需要有一个空格：

1. Single reference / 单篇参考文献
   ```
   This article references the paper :cite:`cnn2015`
   这篇文章参考了论文 :cite:`cnn2015`
   ```

2. Multiple references separated by commas / 多篇参考文献用逗号分隔
   ```
   This article references the papers :cite:`cnn2015,rnn2015`
   这篇文章参考了论文 :cite:`cnn2015,rnn2015`
   ```

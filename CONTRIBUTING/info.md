# Build & Environment Guide / 环境安装与编译指南

## Environment Setup / 环境安装

The book is deployed on GitHub using mdbook. We recommend installing mdbook via Rust's native package manager cargo.

机器学习系统书籍部署在GitHub是依赖于mdbook工具实现的。我们推荐使用rust的原生包管理器cargo安装mdbook。

```bash
# Install Rust toolchain to get cargo / 安装rust工具链，获取cargo
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
cargo install mdbook
```

## Building HTML / 编译HTML版本

Clone the [openmlsys-zh](https://github.com/openmlsys/openmlsys-zh) repository first. All build commands should be run from the repository root.

在编译前先下载[openmlsys-zh](https://github.com/openmlsys/openmlsys-zh) ， 所有的编译命令都在这个文件目录内执行。

```bash
git clone https://github.com/openmlsys/openmlsys-zh.git
cd openmlsys-zh
```

Build HTML using mdbook. Please use the build scripts to ensure the homepage is correctly merged into the book.

使用mdbook工具编译HTML。 请尽量使用build脚本进行编译，保证首页正确合并到书籍中去。

```bash
sh build_mdbook_v1.sh
sh build_mdbook_v2.sh
```

Build outputs are placed in `.mdbook-v2/book` (English) and `.mdbook-v2-zh/book` (Chinese). The `tools/assemble_docs_publish_tree.py` script assembles the final bilingual publication tree, which is then copied to openmlsys.github.io for deployment.

生成的html会在`.mdbook-v2/book`或者`.mdbook-v2-zh/book`下。此时我们可以使用`tools/assemble_docs_publish_tree.py`组装最终的双语发布版本，然后将其拷贝至openmlsys.github.io的docs发布。

For the detailed deployment workflow, see `.github/workflows/update_docs.yml`.

具体工作流可以参考`.github/workflows/update_docs.yml`

## Style Guide / 样式规范

Please follow the project [style guide](style.md) when contributing.

贡献请遵照本教程的[样式规范](style.md)。

## Terminology / 中英文术语对照

Please refer to the [terminology guide](terminology.md) for translations.

翻译请参照[中英文术语对照](terminology.md)。

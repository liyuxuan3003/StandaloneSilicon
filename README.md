# StandaloneSilicon

基于`standalone`的独立图件文档类，支持中文。

StandaloneSilicon的命名遵守"功能+同首字母元素名"的规则，Silicon为第14号元素硅（Si）。

推荐搭配Minimus使用：https://github.com/liyuxuan3003/Minimus。

## 引入方式

StandaloneSilicon以Git子模块的形式引入项目

```bash
git submodule add git@github.com:liyuxuan3003/StandaloneSilicon.git standalone-silicon
```

在主文件顶层指定输入路径

```latex
\makeatletter\def\input@path{{standalone-silicon}}\makeatother
```

使用文档类

```latex
\documentclass{standalone-silicon}
```

## 最小示例

搭配Minimus的完整图件示例

```latex
\makeatletter\def\input@path{{minimus}{standalone-silicon}}\makeatother

\documentclass{standalone-silicon}

\usepackage{minimus-text}
\usepackage{minimus-math}
\usepackage{minimus-tikz}

\begin{document}
\begin{tikzpicture}
    \draw[->] (0,0) -- (2,1);
    \node at (1,0.5) {$x$};
\end{tikzpicture}
\end{document}
```

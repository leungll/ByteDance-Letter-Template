<!--
 * @Author: Lili Liang
 * @Date: 2024-05-19 21:22:15
 * @LastEditors: Lili Liang
 * @LastEditTime: 2024-05-24 00:23:18
 * @Description: Please set description
-->
# ByteDance-Letter-Template
- **ByteDance's recommendation letter template**.
- **Language**: [English](README.md), [简体中文](README_zh.md).

![Author](https://img.shields.io/badge/Author-Lili_Liang-red)
![GitHub last commit](https://img.shields.io/github/last-commit/leungll/ByteDance-Letter-Template?color=yellow)
![GitHub repo size](https://img.shields.io/github/repo-size/leungll/ByteDance-Letter-Template)
![Static Badge](https://img.shields.io/badge/language-latex-orange)
![GitHub License](https://img.shields.io/github/license/leungll/ByteDance-Letter-Template?color=green)

## 前言
当在申研/申博时，如果我们在企业实习或全职工作，通常需要主管为我们写一封推荐信。就我的个人经历而言，鲜少有公司会提供正式的信件模板给申请人，一般都是申请人或推荐人自己制作推荐信模板用于申请。

因此我开源了一个适用于大多数公司使用的推荐信模板 [ByteDance-Letter-Template](https://github.com/leungll/ByteDance-Letter-Template)，此模板以**字节跳动**为例。另外，您也可以将其改编成其他公司的推荐信模板，例如腾讯、阿里巴巴、拼多多、美团等公司。

## 示例
![ByteDance-Letter](https://cdn.jsdelivr.net/gh/leungll/MyImgHosting/img/ByteDance-Letter.png) | ![Tencent-Letter](https://cdn.jsdelivr.net/gh/leungll/MyImgHosting/img/Tencent-Letter.png) | ![Meituan-Letter](https://cdn.jsdelivr.net/gh/leungll/MyImgHosting/img/Meituan-Letter.png)
---|---|---

## 特性
- **无需了解太多的 [Latex](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes) 语法即可使用该模板**
- 支持使用 [Overleaf](https://www.overleaf.com/latex/templates/bytedance-letter-template/pfspzqjqjrhm) 在线编译，无需安装 [TexLive](https://tug.org/texlive) 本地环境
- 一个简单的模板，可进一步定制或扩展
- 将推荐信内容和模板框架进行分离
- 支持在生成的 PDF 中添加超链接，例如电子邮件或 URL
- 支持添加脚注

## 项目结构
```
.
├── LICENSE                     \\ repo license
├── README.md                   \\ readme in English
├── README_zh.md                \\ readme in Chinese
├── letterContent.tex           \\ main content of the letter, isolates from the template frame
├── main.pdf                    \\ letter pdf generated after latex compilation
├── main.tex                    \\ template frame
├── pic                         \\ folder where pictures are stored
│   ├── Alibaba_Logo.png
│   ├── ByteDance_Logo.png
│   ├── ByteDance_Logo_Bg.png
│   ├── Meituan_Logo.png
│   ├── Pinduoduo_Logo.png
│   ├── Tencent_Logo.png
│   └── signature.png
└── sample                      \\ sample
    ├── ByteDance.png
    ├── Meituan.png
    └── Tencent.png
```

## 如何使用
### `main.tex`
- 修改推荐信地址
    ```
    \hphantom{AA}Block B, Building T2 \\ % Change your address
    \hphantom{AA}School of Information Science and Technology \\
    \hphantom{AA}Shenzhen Bay Innovation Technology Center \\
    \hphantom{AA}3156 Keyuan South Road, Nanshan District \\
    \hphantom{AA}Shenzhen, P. R. China, 518054 \\
    ```

- 修改推荐信落款
    ```
    Sincerely yours,

    \includegraphics[width=2in]{pic/signature.png} % Please sign your name

    xxx, Tech Lead Manager \\ % Change your personal information
    Department of Product RD and Infrastructure \\
    ByteDance \\
    Phone: (86) 10-xxxx-xxx \\ 
    Email: \href{mailto:xxx@bytedance.com}{xxx@bytedance.com} \\
    Website: \url{https://www.bytedance.com/en} \\
    ```

- 修改推荐信 Logo
    ```
    pic/ByteDance_Logo_Bg.png % you may need to adjust the transparency of your picture.
    pic/ByteDance_Logo.png
    ```

### `letterContent.tex` 
> 此文件为推荐信的主内容
- 编辑你的内容
- 注意使用 `\\` 进行换行

## 如何编译
### 方式 1 ：在线编译
- 打开 [Overleaf](https://www.overleaf.com/latex/templates/bytedance-letter-template/pfspzqjqjrhm) 链接
- `Open as Template`
- 编辑你的内容
- 编译
- 下载 PDF

### 方式 2 ：本地编译
- 安装 Tex 本地环境: https://www.latex-project.org/get
- 下载此项目: `git clone https://github.com/leungll/ByteDance-Letter-Template.git`
- 运行: `pdflatex main`

## 参考
- [THU Letter of Recommendation Template](https://www.overleaf.com/latex/templates/thu-letter-of-recommendation-template/ghjfgfhykprk)
- [Learn LaTeX in 30 minutes](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes)
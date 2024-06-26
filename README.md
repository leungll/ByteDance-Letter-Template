<!--
 * @Author: Lili Liang
 * @Date: 2024-05-19 21:22:15
 * @LastEditors: Lili Liang
 * @LastEditTime: 2024-05-24 13:53:58
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

## Introduction
When applying for graduate/doctoral studies, if we are doing an internship or working full-time in industry, we usually need a letter of recommendation from our supervisor. In my experience, companies rarely provide formal letter templates for study abroad applications, and applicants or recommenders usually make them themselves. 

Therefore, I open-sourced the project [ByteDance-Letter-Template](https://github.com/leungll/ByteDance-Letter-Template) which is suitable for most companies, taking **ByteDance** as an example. In addition, you can adapt it into a recommendation letter template for other companies, such as <u>Tencent</u>, <u>Alibaba</u>, <u>Pinduoduo</u>, <u>Meituan</u>, etc.

## Demo
![ByteDance-Letter](https://cdn.jsdelivr.net/gh/leungll/MyImgHosting/img/ByteDance-Letter.png) | ![Tencent-Letter](https://cdn.jsdelivr.net/gh/leungll/MyImgHosting/img/Tencent-Letter.png) | ![Meituan-Letter](https://cdn.jsdelivr.net/gh/leungll/MyImgHosting/img/Meituan-Letter.png)
---|---|---

## Features
- **You DO NOT NEED to know too much [Latex](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes) syntax to use it**.
- Support online compilation using [Overleaf](https://www.overleaf.com/latex/templates/bytedance-letter-template/pfspzqjqjrhm), without the need to install the [TexLive](https://tug.org/texlive) environment locally.
- A simple template that can be further customized or extended.
- Separate the letter's main content from the template frame.
- Support adding hyperlinks in generated PDF, such as email or url.
- Support for footnote markers.

## File layout
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

## Usage
### `main.tex`
- Change the address of the letter
    ```
    \hphantom{AA}Block B, Building T2 \\ % Change your address
    \hphantom{AA}School of Information Science and Technology \\
    \hphantom{AA}Shenzhen Bay Innovation Technology Center \\
    \hphantom{AA}3156 Keyuan South Road, Nanshan District \\
    \hphantom{AA}Shenzhen, P. R. China, 518054 \\
    ```

- Change the signature of the letter
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

- Change the logo of the letter
    ```
    pic/ByteDance_Logo_Bg.png % you may need to adjust the transparency of your picture.
    pic/ByteDance_Logo.png
    ```

### `letterContent.tex` 
> Main content of the letter.
- Edit your content.
- Note the use of `\\` for line breaks.

## How to compile
### Method 1: Online Compilation
- Open [Overleaf](https://www.overleaf.com/latex/templates/bytedance-letter-template/pfspzqjqjrhm) link
- `Open as Template`
- Edit your content
- Compile
- Download PDF

### Method 2: Local Compilation
- Install the Tex local environment: https://www.latex-project.org/get
- Download this repo: `git clone https://github.com/leungll/ByteDance-Letter-Template.git`
- Run: `pdflatex main`

## Reference
- [THU Letter of Recommendation Template](https://www.overleaf.com/latex/templates/thu-letter-of-recommendation-template/ghjfgfhykprk)
- [Learn LaTeX in 30 minutes](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes)

---
**This project needs a star ⭐ from you ❤️.**

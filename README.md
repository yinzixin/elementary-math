# 更新包管理器
sudo apt update

# 安装 Pandoc
sudo apt install pandoc

# 安装 LaTeX 和 xelatex 引擎
sudo apt install texlive-xetex texlive-latex-extra

# 安装中文支持（提供 xeCJK，否则中文长行不会自动换行，会冲出页边距）
sudo apt install texlive-lang-chinese

# 安装中文字体
sudo apt install fonts-noto-cjk fonts-noto-cjk-extra

# 验证安装
pandoc --version
pdflatex --version
fc-list | grep "Noto Sans CJK"

# 完成后使用
pandoc input.md -o output.pdf --pdf-engine=xelatex -V mainfont="Noto Sans CJK SC"

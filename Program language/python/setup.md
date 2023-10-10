1. 安装python
```shell
sudo pacman -S python
```
2. 创建虚拟环境
```shell
# 为python虚拟环境创建目录，{/path/to/pyenv}是虚拟环境所在的目录
mkdir {/path/to/pyenv}
# 创建python虚拟环境
python -m venv {/path/to/pyenv}
# 激活虚拟环境（zsh）
source {/path/to/pyenv}/bin/activate
```
成功后显示(pyenv)$
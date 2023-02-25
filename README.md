# set-up-guide

### pyenv
```
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(pyenv init -)"' >> ~/.zshrc
source ~/.zshrc

pyenv install --list

```

インストール、切り替えが必要なら<br>
```
pyenv install 3.xx.x
pyenv local 3.xx.x
```


### poetry
基本的にフォルダ作成してから〜の流れ.
```
poetry init
python -m venv .venv
poetry add numpy
poetry remove numpy
```

こんなエラーが出ることがある.
```
current python version (3.10.10) is not allowed by the project (^3.11). please change python executable via the "env use" command. pyenv
```
この場合はエラー文に書いてある通り
```
poetry env use 3.xx.x
```
とアップデートする.

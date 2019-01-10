## 覆盖率

python-cov

```
pytest.mark.parametrize 参数化
```

```
import pytest
from zpin import Pinyin

p = Pinyin()


@pytest.mark.parametrize("ch,splits,tone_mark,convert,resp",[
    ("上下","-",None,"lower","shang-xia"),
    ("伤", "","numbers","capitalize","Shang1"),
    ("shang1s", "","numbers","capitalize","shang1s"),
    ("进退:6", " ","marks","upper","JÌN TUÌ :6"),

])
def test_getpinyin(ch,splits,tone_mark,convert,resp):
    assert p.get_pinyin(chars=ch,splitter=splits,tone_marks=tone_mark,convert=convert) == resp


@pytest.mark.parametrize("resp",[
    ("ni-hao"),
])
def test_getpinyin_default(resp):
    assert p.get_pinyin() == resp

@pytest.mark.parametrize("ch,resp",[
    ("上","S"),
    ("上-","S-"),

])
def test_getinitial(ch,resp):
    print(p.get_initial(ch))
    assert p.get_initial(ch) == resp

@pytest.mark.parametrize("resp",[
    ("N"),
])
def test_getinitial_default(resp):
    assert p.get_initial() == resp

@pytest.mark.parametrize("ch,splits,resp",[
    ("上下","-","S-X"),
    ("上下"," ","S X"),
    ("上下s","","SXs"),
])
def test_getinitials(ch,splits,resp):
    assert p.get_initials(chars=ch,splitter=splits) == resp


@pytest.mark.parametrize("resp",[
    ("N-H"),

])
def test_getinitials_default(resp):
    assert p.get_initials() == resp
```

```
---------- coverage: platform darwin, python 3.6.5-final-0 -----------
Name                  Stmts   Miss  Cover
-----------------------------------------
zpin/__init__.py         82      5    94%
zpin/test_pinyin.py      16      0   100%
-----------------------------------------
TOTAL                    98      5    95%
```




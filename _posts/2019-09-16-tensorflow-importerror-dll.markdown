---
layout: post
title: "Tensorflow ImportError: DLL load failed hatası çözümü"
lang: tr
tags: ["tensorflow", "yapay zeka", "hata", "ipucu", "python"]
categories: ["tip&tricks"]
---

<h3>Python Tensorflow train sırasında tImportError: DLL load failed hatası</h3>

```bash
python retrain.py --img --image_dir=D:\path\to
Traceback (most recent call last):
  File "retrain.py", line 132, in <module>
    import tensorflow as tf
  File "C:\path\to\AppData\Local\Programs\Python\Python36\lib\site-packages\tensorflow\__init__.py", line 22, in <module>
    from tensorflow.python import pywrap_tensorflow  # pylint: disable=unused-import
  File "C:\path\to\AppData\Local\Programs\Python\Python36\lib\site-packages\tensorflow\python\__init__.py", line 52, in <module>
    from tensorflow.core.framework.graph_pb2 import *
  File "C:\path\to\AppData\Local\Programs\Python\Python36\lib\site-packages\tensorflow\core\framework\graph_pb2.py", line 6, in <module>
    from google.protobuf import descriptor as _descriptor
  File "C:\path\emtorek\AppData\Local\Programs\Python\Python36\lib\site-packages\google\protobuf\descriptor.py", line 47, in <module>
    from google.protobuf.pyext import _message
ImportError: DLL load failed: Belirtilen yordam bulunamadı.
```

<h2>Çözümü</h2>

Yukarıdaki şekilde bir hata alıyorsanız. Çözümü aslında gayet basit. Google'ın aracı olan `protobuf` ın sürümünü düşürecekseniz. Bunun için terminale yazmanız gereken komut gayet basit:

```python
pip install protobuf==3.6.0
```
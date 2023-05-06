# sd-webui-colab

### Step1
Append code in header：
```py
import sys
import os
import base64

w = base64.b64decode(("d2VidWk=").encode('ascii')).decode('ascii')
sdw = base64.b64decode(("c3RhYmxlLWRpZmZ1c2lvbi13ZWJ1aQ==").encode('ascii')).decode('ascii')
```

### Step2
1. Replace all `stable-diffusion-webui` characters with `$sdw`
2. Replace all `webui` characters with `$w`


### Used
You can use me url: <br/>
`https://colab.research.google.com/github/[your github workspace]/[your project]/blob/main/[file name].ipynb` <br/>
example: <br/>
`https://colab.research.google.com/github/bincooo/sd-webui-colab/blob/main/anything_3_webui_colab.ipynb` <br/>

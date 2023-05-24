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
1. Replace all `stable-diffusion-webui` characters with `{sdw}`
2. Replace all `webui` characters with `{w}`

[civitai](https://civitai.com)

### Used
You can use me url: <br/>
`https://colab.research.google.com/github/[your github workspace]/[your project]/blob/main/[file name].ipynb` <br/>
example: <br/>
`https://colab.research.google.com/github/bincooo/sd-webui-colab/blob/main/anything_3_webui_colab.ipynb` <br/>



### frp
Append code in header：
```shell
#@title 🚀 `Launch web UI`
#@markdown ** frp client setting **
key = "" #@param {type:"string"}
servAddr = "" #@param {type:"string"}
!wget https://github.com/fatedier/frp/releases/download/v0.48.0/frp_0.48.0_linux_amd64.tar.gz
!tar -zxvf frp_0.48.0_linux_amd64.tar.gz
!sed -i -e 's/server_addr = 127.0.0.1/server_addr = '{servAddr}'/g' /content/frp_0.48.0_linux_amd64/frpc.ini
!echo -e '\n[web]\ntype = http\nlocal_ip = 127.0.0.1\nlocal_port = 7860\ncustom_domains = '{key}'.domain.com' >> /content/frp_0.48.0_linux_amd64/frpc.ini
!nohup /content/frp_0.48.0_linux_amd64/frpc -c /content/frp_0.48.0_linux_amd64/frpc.ini > /dev/null 2>&1 &
#========
```

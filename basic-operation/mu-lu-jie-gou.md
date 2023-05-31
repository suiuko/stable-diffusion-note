# 目录结构

#### 模型存放

在根目录下 `/models/stable-diffusion` 存放，在这可以被启动器直接识别。

当然您可以在 `/models` 直接创建一个新的文件夹，将下载的目录保存到该文件夹下，但是需要在UI设置中添加模型同步，最后模型会被复制到 `/models/stable-diffusion` 下。

#### Lora存放

在根目录下 `/models/Lora` 存放，同时在此也可以被启动器直接识别。推荐这样操作。

### 照片/视频输出文件夹

`/outputs` 文件夹中为照片的输出文件夹，其中有不同种类的输出文件夹。

最常用的是文生图和图生图，输出的文件夹为 `/outputs/txt2img-images` 和 `/outputs/img2img-images` ，同时如果您添加了其他功能插件，在 /outputs 中会新增功能文件夹。

For instance, 我添加了`infinite zooms` 这个插件，在输出时会自动添加 `/infinite-zooms` 这个文件夹，所以在使用的过程中要注意输出文件夹的目录。


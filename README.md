
# Open Color MATLAB

[![View Open-Color-MATLAB on File Exchange](https://www.mathworks.com/matlabcentral/images/matlab-file-exchange.svg)](https://ww2.mathworks.cn/matlabcentral/fileexchange/180594-open-color-matlab)
[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=cuixing158/Open-Color-MATLAB&file=README.mlx)

This repository provides minimalist RGB color definitions from [Open Color](https://yeun.github.io/open-color/), making it easy to use color themes when plotting graphics in MATLAB.

本仓库提供来自[Open color](https://yeun.github.io/open-color/) 的简约 RGB 颜色定义，方便在MATLAB中使用绘制图形颜色主题。

Happy plotting! :tada::tada::tada:

## Usage

Directly load the 'colormapData.mat' color theme data into your MATLAB workspace.

直接在你MATLAB工作空间中加载“colormapData.mat”颜色主题数据。

```matlab
load colormapData.mat
```

> [!NOTE]
> This contains a dictionary that includes all the color theme data, where each color is represented by a 256x3 [color mapping array](https://www.mathworks.com/help/matlab/ref/colormap.html#burd3gs-5). The data range is [0,1].

```text
d =
  dictionary (string --> cell) with 13 entries:
    "Gray"   --> {256×3 double}
    "Red"    --> {256×3 double}
    "Pink"   --> {256×3 double}
    "Grape"  --> {256×3 double}
    "Violet" --> {256×3 double}
    "Indigo" --> {256×3 double}
    "Blue"   --> {256×3 double}
    "Cyan"   --> {256×3 double}
    "Teal"   --> {256×3 double}
    "Green"  --> {256×3 double}
    "Lime"   --> {256×3 double}
    "Yellow" --> {256×3 double}
    "Orange" --> {256×3 double}
```

## Requirements

[MathWorks Products](http://www.mathworks.com)

- MATLAB R2022b or later

## Examples

Create a matrix of data. Then create a heatmap of the matrix values, draw the theme colors one by one.

创建一个数据矩阵，然后绘制矩阵值的热图，一个一个地绘制主题颜色。

```matlab
load colormapData.mat
cdata = rand(10);

keyNames = keys(d);
for idx = 1:numEntries(d)
    figure;
    heatmap(cdata);

    cmap = d(keyNames(idx));
    colormap(cmap{:})
    title("Color Theme:"+keyNames(idx));
end
```

![figure_0.png](README_media/figure_0.png)

![figure_1.png](README_media/figure_1.png)

![figure_2.png](README_media/figure_2.png)

![figure_3.png](README_media/figure_3.png)

![figure_4.png](README_media/figure_4.png)

![figure_5.png](README_media/figure_5.png)

![figure_6.png](README_media/figure_6.png)

![figure_7.png](README_media/figure_7.png)

![figure_8.png](README_media/figure_8.png)

![figure_9.png](README_media/figure_9.png)

![figure_10.png](README_media/figure_10.png)

![figure_11.png](README_media/figure_11.png)

![figure_12.png](README_media/figure_12.png)

## Color Themes

![colors](README_media/makeColorMaps-03-30-2025_10_18_AM.png)

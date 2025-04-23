---
author: Blake John
tags:
  - problem
  - bug
---
# 01 图像绘制

## 1.1 `plot` 图像显示不全 #solved #bug 

**descriptions :** 

在使用 octave 进行绘图的时候，会有图像显示不全的情况出现。

![](imgs/incompleted_graph.png)

这个问题主要是由于 octave 使用的图像展示工具有bug导致的。在新版 octave 中，默认使用 `qt` 作为支持，来展示图像，但是该支持仍有问题。因此我们需要更换用于显示图像的工具。

**Solution : ** 

我们只需要通过 `graphics_toolkit()` 函数将展示工具替换成 `gnuplot` 即可 : 

```octave
>> graphics_toolkit("gnuplot")
```

若显示计算机中没有 `gnuplot` 可以使用，就去下载 :

```bash
sudo pacman -S gnuplot
```

设置好工具之后(新安装的 `gnuplot` 可能需要重启一下 octave 才能找到)，我们重新绘图，就可以发现问题已经解决了 : 

![](imgs/full_graph.png)

# 02 函数

## 2.1 函数与文件名不匹配 #solved #problem 

### information

```text
warning: function name 'draw_rect' does not agree with function filename 'D:\oc
tave\chapter1\fibonacci_visualization.m'
error: 'point' undefined near line 4, column 9
error: called from
    fibonacci_visualization at line 4 column 7
```

这个错误信息表明你在 Octave 中遇到了两个问题：

1. **函数名与文件名不匹配**：
   - 错误信息 `warning: function name 'draw_rect' does not agree with function filename 'D:\octave\chapter1\fibonacci_visualization.m'` 表示你定义了一个名为 `draw_rect` 的函数，但该函数所在的文件名是 `fibonacci_visualization.m`。在 Octave 中，如果一个文件包含一个函数，那么文件名应该与函数名一致。

2. **未定义的变量**：
   - 错误信息 `error: 'point' undefined near line 4, column 9` 表示在代码的第 4 行，尝试使用了一个未定义的变量 `point`。

### 解决方法

#### 1. 修复函数名与文件名不匹配的问题
- 如果你有一个名为 `draw_rect` 的函数，那么应该将文件名改为 `draw_rect.m`。
- 如果你希望文件 `fibonacci_visualization.m` 包含多个函数，那么可以将 `draw_rect` 定义为该文件中的一个子函数或私有函数。

#### 2. 修复未定义的变量问题
- 检查代码中第 4 行使用 `point` 变量的地方，确保在使用它之前已经正确定义了该变量。

### 示例修复

假设你的 `fibonacci_visualization.m` 文件中包含一个主函数和一个子函数 `draw_rect`，以下是可能的修复方式：

```octave
% fibonacci_visualization.m

% 主函数
function fibonacci_visualization()
    % 定义变量 point
    point = [0, 0];  % 示例定义，根据实际需求修改
    
    % 调用子函数 draw_rect
    draw_rect(point);
endfunction

% 子函数 draw_rect
function draw_rect(point)
    % 使用 point 变量绘制矩形
    % 示例代码，根据实际需求修改
    rectangle('Position', [point(1), point(2), 1, 1], 'EdgeColor', 'r');
endfunction
```

### 总结
- 确保函数名与文件名一致。
- 在使用变量之前正确定义它。
- 如果有多个函数，可以将它们定义在同一个文件中，其中一个是主函数，其他是子函数。

通过以上修复，应该可以解决你遇到的错误。

# 03 Matlab

## 3.1 Linux 上界面太小 #solved 

我们只需要调节 Matlab 的缩放即可 : 

```Matlab
s = settings; s.matlab.desktop.DisplayScaleFactor; s.matlab.desktop.DisplayScaleFactor.PersonalValue = 2.0;
```

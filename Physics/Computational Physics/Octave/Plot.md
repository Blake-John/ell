# 01 `mesh` 样式

在 Octave 中，使用 `mesh` 函数绘图时，可以通过设置属性来调整样式，例如颜色、线条样式等。以下是一个示例代码，展示了如何设置 `mesh` 图的样式：

```octave
[x, y] = meshgrid(-3:0.1:3, -3:0.1:3);
z = sin(sqrt(x.^2 + y.^2)) ./ sqrt(x.^2 + y.^2);

mesh(x, y, z, 'EdgeColor', 'none', 'FaceColor', 'interp');
xlabel('X轴');
ylabel('Y轴');
zlabel('Z轴');
title('使用 mesh 绘制的三维图');
```

### 说明
- `'EdgeColor', 'none'`：设置网格线颜色为无，即去掉网格线。
- `'FaceColor', 'interp'`：设置曲面颜色为插值着色，使表面看起来更加平滑。

通过这些设置，可以调整 `mesh` 图的外观，使其更符合需求。

# 02 函数绘制

在Octave中，`ezplot`和`fplot`都是用于绘制函数图像的函数，但它们在使用上有一些区别：

## 2.1 区别

1. **输入参数类型不同**：
   - `ezplot`可以接受字符串、符号表达式或函数句柄作为输入，而`fplot`主要接受函数句柄、内联函数或字符串形式的函数名。
   - `ezplot`在绘制隐函数和参数方程时更为方便，因为它可以直接处理这些类型的函数表达式。

2. **绘图方式不同**：
   - `fplot`会自动调整x坐标的取点，以更好地呈现函数的特征，尤其适合绘制连续且明确指定函数表达式的图形。
   - `ezplot`则会根据默认或指定的区间来绘制函数图像，无需用户手动准备数据。

3. **适用场景不同**：
   - `fplot`更适合绘制显式函数（形如y=f(x)）的图像，且在处理连续函数时能更好地捕捉曲线的细节。
   - `ezplot`除了可以绘制显式函数外，还可以绘制隐函数（形如f(x,y)=0）和参数方程定义的曲线，使用起来更加灵活。

## 2.2 用法

###  `ezplot`用法

```octave
ezplot(f) % 绘制显函数f(x)在默认区间[-2π, 2π]的图像
ezplot(f, [min, max]) % 指定x轴区间
ezplot(f, [xmin, xmax, ymin, ymax]) % 指定x和y轴区间
ezplot(fx, fy) % 绘制参数方程x=fx(t), y=fy(t)的图像，默认t在[0, 2π]
ezplot(fx, fy, [tmin, tmax]) % 指定参数t的区间
```

### `fplot`用法

```octave
fplot(fn, limits) % 绘制函数fn在区间limits内的图像
fplot(..., tol) % 指定相对容差tol来控制绘图精度
fplot(..., n) % 指定最小取样点数n
fplot(..., fmt) % 指定绘图的线条样式
```

### 示例

```octave
% 使用ezplot绘制显函数
ezplot('x^2', [-5, 5])

% 使用ezplot绘制隐函数
ezplot('x^2 + y^2 - 4', [-3, 3, -3, 3])

% 使用ezplot绘制参数方程
ezplot('sin(t)', 'cos(t)', [0, 2*pi])

% 使用fplot绘制显函数
fplot(@(x) x.^2, [-5, 5])

% 使用fplot绘制多个函数
fplot(@(x) [sin(x), cos(x)], [0, 2*pi])
```

对于 `ezplot` 来说，除了直接输入表达式，我们也可以使用符号工具箱来设置符号表达式，例如 : 

```Octave
syms x y;
eq = x^2 + y^2 == 3;
ezplot(eq);
```

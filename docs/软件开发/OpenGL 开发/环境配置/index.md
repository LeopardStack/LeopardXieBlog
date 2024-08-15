# 一、各种环境的配置

# 1.freeglut 的配置

在 VisualStudio2022 IDE 下结合 freeglut-3.2.2 进行开发

freeglut-3.2.2 下载地址：[https://freeglut.sourceforge.net/](https://freeglut.sourceforge.net/)

![Untitled](%E4%B8%80%E3%80%81%E5%90%84%E7%A7%8D%E7%8E%AF%E5%A2%83%E7%9A%84%E9%85%8D%E7%BD%AE%203639af0f452945359eba5eb7b83239a3/Untitled.png)

下载下来后，直接解压，然后利用 CMake 工具，将其编译成为 VisualStudio2022 工程

![Untitled](%E4%B8%80%E3%80%81%E5%90%84%E7%A7%8D%E7%8E%AF%E5%A2%83%E7%9A%84%E9%85%8D%E7%BD%AE%203639af0f452945359eba5eb7b83239a3/Untitled%201.png)

打开项目后，记得选择上面的两个属性为 release 和 x86，并且右击 ALL_BUILD 进行生成

![Untitled](%E4%B8%80%E3%80%81%E5%90%84%E7%A7%8D%E7%8E%AF%E5%A2%83%E7%9A%84%E9%85%8D%E7%BD%AE%203639af0f452945359eba5eb7b83239a3/Untitled%202.png)

新建一个  VS2022 空项目，然后右击项目属性

![Untitled](%E4%B8%80%E3%80%81%E5%90%84%E7%A7%8D%E7%8E%AF%E5%A2%83%E7%9A%84%E9%85%8D%E7%BD%AE%203639af0f452945359eba5eb7b83239a3/Untitled%203.png)

将 freeglut 源码中的 include 文件夹包含到 C/C++ 的常规里的附加包含目录

![Untitled](%E4%B8%80%E3%80%81%E5%90%84%E7%A7%8D%E7%8E%AF%E5%A2%83%E7%9A%84%E9%85%8D%E7%BD%AE%203639af0f452945359eba5eb7b83239a3/Untitled%204.png)

将上面生成的 release 文件夹包含到连接器的常规的附加库目录

![Untitled](%E4%B8%80%E3%80%81%E5%90%84%E7%A7%8D%E7%8E%AF%E5%A2%83%E7%9A%84%E9%85%8D%E7%BD%AE%203639af0f452945359eba5eb7b83239a3/Untitled%205.png)

将上面生成的 release 文件夹里的 freeglut.lib 包含到连接器输入中的附件依赖项

![Untitled](%E4%B8%80%E3%80%81%E5%90%84%E7%A7%8D%E7%8E%AF%E5%A2%83%E7%9A%84%E9%85%8D%E7%BD%AE%203639af0f452945359eba5eb7b83239a3/Untitled%206.png)

右击打开项目的文件夹

![Untitled](%E4%B8%80%E3%80%81%E5%90%84%E7%A7%8D%E7%8E%AF%E5%A2%83%E7%9A%84%E9%85%8D%E7%BD%AE%203639af0f452945359eba5eb7b83239a3/Untitled%207.png)

将上面工程 build 中的 bin 目录下的 release 文件夹中的 freeglut.dll 包含到项目的文件夹中

![Untitled](%E4%B8%80%E3%80%81%E5%90%84%E7%A7%8D%E7%8E%AF%E5%A2%83%E7%9A%84%E9%85%8D%E7%BD%AE%203639af0f452945359eba5eb7b83239a3/Untitled%208.png)

![Untitled](%E4%B8%80%E3%80%81%E5%90%84%E7%A7%8D%E7%8E%AF%E5%A2%83%E7%9A%84%E9%85%8D%E7%BD%AE%203639af0f452945359eba5eb7b83239a3/Untitled%209.png)

```java

#define NDEBUG
#include "gl/glut.h"

void redraw()
{
	glClear(GL_COLOR_BUFFER_BIT);
	glBegin(GL_TRIANGLES);
	//glColor3f(1, 0, 0);
	glColor3f(0.0, 0.0, 1.0);
	glVertex3f(-0.5, 0, 0.5);

	//开始画1
	//
	glColor3f(1.0, 0, 0);
	glVertex3f(0.5, 0.0, 0.5);

	glColor3f(0.0, 1.0, 0);
	glVertex3f(0, 0.8, 0.5);
	//2

	glEnd(); // GL_QUADS
	glutSwapBuffers();
}

int main(int argc, char* argv[])
{
	glutInit(&argc, argv);
	glutInitDisplayMode(GLUT_RGBA | GLUT_DOUBLE);
	int windowHandle
		= glutCreateWindow("Simple GLUT App");

	glutDisplayFunc(redraw);

	glutMainLoop();

	return 0;
}
```

将上述代码粘贴到 VS2022 项目中你所建立的 cpp 文件

![Untitled](%E4%B8%80%E3%80%81%E5%90%84%E7%A7%8D%E7%8E%AF%E5%A2%83%E7%9A%84%E9%85%8D%E7%BD%AE%203639af0f452945359eba5eb7b83239a3/Untitled%2010.png)

点击执行就可以生成一个三角形

![Untitled](%E4%B8%80%E3%80%81%E5%90%84%E7%A7%8D%E7%8E%AF%E5%A2%83%E7%9A%84%E9%85%8D%E7%BD%AE%203639af0f452945359eba5eb7b83239a3/Untitled%2011.png)

注意：以上所有事项都必须一步步全部执行到位，否则都会出现异常、各种报错

eg.找不到 freeglut.dll 

![Untitled](%E4%B8%80%E3%80%81%E5%90%84%E7%A7%8D%E7%8E%AF%E5%A2%83%E7%9A%84%E9%85%8D%E7%BD%AE%203639af0f452945359eba5eb7b83239a3/Untitled%2012.png)

这种就是没有将 dll 放入项目文件夹中
# 七、异常机制、 File 类和 IO 流

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%201.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%202.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%203.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%204.png)

```
import java.io.File;
import java.io.FileFilter;
import java.io.IOException;
import java.text.SimpleDateFormat;
import java.util.Date;

public class FileTest {
    public static void main(String[] args) throws IOException {
        // 构造 File 类型对象与 D:\MyProject\JavaExercises\DocTest\DocTest\a.txt 关联
        File f1 = new File("D:\\MyProject\\JavaExercises\\DocTest\\DocTest\\a.txt");

        if(f1.exists()){
            System.out.println("'文件的名称是：" + f1.getName());
            System.out.println("文件的大小是：" + f1.length());
            Date d1 = new Date(f1.lastModified());
            SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
            System.out.println("文件的最后一次修改时间： " + sdf.format(d1));

            System.out.println("文件的绝对路径信息是：" + f1.getAbsolutePath());
            System.out.println(f1.delete()? "文件删除成功" : "文件删除失败");
        }else{
            System.out.println(f1.createNewFile() ? "文件创建成功" : "文件创建失败!");
        }

        System.out.println("-----------------------------------------------------");
        File f2 = new File("D:\\MyProject\\JavaExercises\\DocTest\\DocTest\\src\\T2");
        if(f2.exists()){
            System.out.println("目录名称是：" + f2.getName());
            System.out.println(f2.delete() ? "目录删除成功" : "目录删除失败");
        }else{
            System.out.println(f2.mkdir() ? "目录创建成功" : "目录创建失败！");
        }

        System.out.println("-------------------------------------------------------------");
        File f3 = new File("D:\\MyProject\\JavaExercises\\DocTest\\DocTest\\src\\T1");
        File[] fileArray = f3.listFiles();
        for(File tf: fileArray){
            String name = tf.getName();
            System.out.println(name);

            if(tf.isDirectory()){
                System.out.println("[" + name + "]");
            }
        }

        System.out.println("-------------------------------------------------------------");

//        FileFilter fileFilter = new FileFilter() {
//            @Override
//            public boolean accept(File pathname) {
//                return pathname.getName().endsWith(".java");
//            }
//        };

        FileFilter fileFilter = (File pathname) ->{return pathname.getName().
                endsWith(".java");};

        File[] fileArray2 = f3.listFiles(fileFilter);
        for(File tf: fileArray2){
            System.out.println(tf);
        }
    }
}

```

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%205.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%206.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%207.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%208.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%209.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%2010.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%2011.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%2012.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%2013.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%2014.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%2015.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%2016.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%2017.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%2018.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%2019.png)

![Untitled](%E4%B8%83%E3%80%81%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E3%80%81%20File%20%E7%B1%BB%E5%92%8C%20IO%20%E6%B5%81%20a55a217a24a04f9298acef232283cbda/Untitled%2020.png)
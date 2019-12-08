# exp-5
实验目的：<br>
====
分析学生选课系统<br>
使用GUI窗体及其组件设计窗体界面<br>
完成学生选课过程业务逻辑编程<br>
基于文件保存并读取数据<br>
处理异常<br>

二、要求:<br>
======
1、	设计GUI窗体，支持学生注册、课程新加、学生选课、学生退课、打印学生选课列表等操作。<br>
2、	基于事件模型对业务逻辑编程，实现在界面上支持上述操作。<br>
3、	针对操作过程中可能会出现的各种异常，做异常处理。<br>
4、	基于输入/输出编程，支持学生、课程、教师等数据的读写操作。<br>

流程图<br>
====

![Image text](https://github.com/IvanZima/exp-5/blob/master/%E6%B5%81%E7%A8%8B%E5%9B%BE.PNG)
   
核心代码<br>
=====
     
     
     public Index() {
		setTitle("Index");
		setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		setBounds(150, 150, 550, 400);
		contentPane = new JPanel();
	contentPane.setBorder(new EmptyBorder(5, 5, 5, 5));
		setContentPane(contentPane);
		contentPane.setLayout(null);
		JButton btnNewButton = new JButton("Exit");
		btnNewButton.setBounds(0, 107, 97, 23);
		contentPane.add(btnNewButton);
		btnNewButton.addActionListener(new ActionListener(){
			public void actionPerformed(ActionEvent e) {
				Exit exit = new Exit();
				exit.setVisible(true);
			}
		});
		JButton btnNewButton_2 = new JButton("创建");
		btnNewButton_2.setBounds(533, 107, 97, 23);
		contentPane.add(btnNewButton_2);
		btnNewButton_2.addActionListener(new ActionListener(){
			public void actionPerformed(ActionEvent e) {
				Create create = new Create();
				create.setVisible(true); 
			}
		});
		JButton btnNewButton_1 = new JButton("选择");
		btnNewButton_1.setBounds(339, 107, 97, 23);
		contentPane.add(btnNewButton_1);
		btnNewButton_1.addActionListener(new ActionListener(){
			public void actionPerformed(ActionEvent e) {
				Chose chose = new Chose();
				chose.setVisible(true); 
			}
		});
		JButton btnNewButton_3 = new JButton("预览");
		btnNewButton_3.setBounds(175, 107, 97, 23);
		contentPane.add(btnNewButton_3);
		btnNewButton_3.addActionListener(new ActionListener(){
			public void actionPerformed(ActionEvent e) {
				Print print = new Print();
				print.setVisible(true);
			}
		});
	}


通过GUI编程完成主界面的设计。

			    FileWriter writer;
		        try {
		            writer = new FileWriter("C:\\Users\\46975\\Desktop\\java实验\\exp5\\T.txt",true);
		            writer.append(s6); 
		            writer.flush();
		            writer.close();
		        } catch (IOException e1) {
		            e1.printStackTrace();
		        }
按照编号姓名地点时间评分的格式写入指定的txt文件并且通过try catch 语句防止程序崩溃。



	       try {
			  BufferedReader br = new BufferedReader(new FileReader("C:\\Users\\46975\\Desktop\\java实验\\exp5\\T.txt"));
			    String Student_num = br.readLine();
			    br.close();
			    writer = new FileWriter("C:\\Users\\46975\\Desktop\\java实验\\exp5" + Student_num +".txt",true);		                    writer.append(chosen); 
			    writer.close();
	           } catch (IOException e1) {
			            e1.printStackTrace();
			        }
选择课程部分读取文件并显示并且通过try catch 语句防止程序崩溃。

程序截图<br>
=========

![Image text](https://github.com/IvanZima/exp-5/blob/master/%E6%B3%A8%E5%86%8C.PNG)

![Image text](https://github.com/IvanZima/exp-5/blob/master/%E4%B8%BB%E7%95%8C%E9%9D%A2PNG.PNG)

![Image text](https://github.com/IvanZima/exp-5/blob/master/%E6%89%93%E5%8D%B0.png)

![Image text](https://github.com/IvanZima/exp-5/blob/master/%E5%AD%A6%E7%94%9F%E6%B3%A8%E5%86%8C.PNG)

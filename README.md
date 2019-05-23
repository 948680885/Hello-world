# Hello-world
第一次进来学习
public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		int[][] array = new int[5][5];//第一个5是指5个班，第二个班是指每个班由5个人

		//循环录入每个班级的学员成绩
		//外层循环：班
		for(int i = 0; i<array.length; i++){
			System.out.println("——————————请输入第"+(i+1)+"个班的成绩——————————");
			//内层循环：当前班的每个人
			for(int j = 0 ; j<array[i].length; j++){
				System.out.println("请输入第"+(j+1)+"个同学的成绩：");
				array[i][j] = input.nextInt();
			}
		}
		//计算各个班分别的总成绩
		System.out.println("**********成绩统计******************");
		int sum = 0;
		//外层循环：班
		for(int i = 0; i<array.length; i++){
			System.out.println("这是第"+(i+1)+"个班，");
			sum=0;//每个班进来统计总成绩前，需要将sum清零
			//内层循环：当前班的每个人
			for(int j = 0 ; j<array[i].length; j++){
				sum+=array[i][j];
			}
			System.out.println("这个班的总成绩是"+sum );
		}
	}

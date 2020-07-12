一、本质
分治和回溯，本质上就是递归，是递归的一个细分类。可以理解为分治和回溯，就是一种特殊的递归，或者是较为复杂的递归。

本质上就是找重复性以及分解问题，和最后组合每个子问题的结果，都是这一个思路。

碰到一个题目，就会找到他的重复性：
1. 最优重复性：动态规划
2. 最近重复性：根据重复性的构造和分解，便有分治和回溯。

二、分治（Divide & Conquer）

递归状态树
分治的思想：本质是递归，在递归状态树的时候，对一个问题会化解成好几个子问题，

代码模板：
def divide_conquer(problem, param1, param2, ...):
    # recursion terminator 终止条件
    if problem is None:
        print_result
        return
    # prepare data  处理当前层逻辑
    data = prepare_data(problem)
    subproblems = split_problem(problem, data)
    # conquer subproblems  调用函数下探到下一层，解决更细节的子问题
    subresult1 = self.divide_conquer(subproblems[0], p1, ...)
    subresult2 = self.divide_conquer(subproblems[1], p1, ...)
    subresult3 = self.divide_conquer(subproblems[2], p1, ...)
    ...
    # process and generate the final result
    result = process_result(subresult1, subresult2, subresult3, ...)

    # revert the current level states
    # 与泛型递归不同就是在drill down与revert state中间加了一步
    # ---> 就是把drill down得到的子结果要合并在一起，返回回去。
    
三、回溯（Backtracking）
可以理解为递归的一种问题，不断地在每一层去试，每一层有不同的办法，类似于一个一个去试，看这个方法是否可行。最典型的应用是八皇后问题、数独。

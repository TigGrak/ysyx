# [F5 支持数列求和的简单处理器](https://ysyx.oscc.cc/docs/2407/f/5.html)

## 题目
1.[实现取指功能](https://ysyx.oscc.cc/docs/2407/f/5.html#%E5%8F%96%E6%8C%87)
>通过多路选择器实现一个ROM, 并在其中存放数列求和的指令序列, 然后通过PC寄存器取出指令. 你需要根据你的理解来确定ROM的规格.

可能的解法：[F5_Implement_fetch_function.circ](F5_Implement_fetch_function.circ)


<br>

2.[实现GPR及其写入功能](https://ysyx.oscc.cc/docs/2407/f/5.html#%E6%89%A7%E8%A1%8C)
>在寄存器的基础上搭建一个RAM, 从而实现GPR的写入功能. 你需要根据你的理解来确定RAM的规格.

可能的解法：[F5_Implement_GPR.circ](F5_Implement_GPR.circ)

<br>

3.[实现仅支持li指令的sCPU](https://ysyx.oscc.cc/docs/2407/f/5.html#%E6%9B%B4%E6%96%B0pc)
>根据上文, 用数字电路实现`li`的指令周期涉及的各个部件, 并将它们连接起来. 实现后, 尝试让sCPU执行数列求和程序中的前几条`li`指令, 并观察电路中GPR的状态是否与ISA的状态一致.

可能的解法：[F5_Implement_sCPU_supporting_only_li_instruction.circ](F5_Implement_sCPU_supporting_only_li_instruction.circ)


<br>

4.[添加add指令](https://ysyx.oscc.cc/docs/2407/f/5.html#%E5%AE%9E%E7%8E%B0%E5%AE%8C%E6%95%B4%E7%9A%84scpu)
>根据上文, 在sCPU中添加`add`指令. 实现后, 尝试让sCPU继续执行数列求和程序中的几条`add`指令, 并观察电路中GPR的状态是否与ISA的状态一致.

可能的解法：[F5_Implement_addAbner0_function.circ](F5_Implement_addAbner0_function.circ)(已提前实现`bner0`指令)

<br>

5.[添加bner0指令](https://ysyx.oscc.cc/docs/2407/f/5.html#%E5%AE%9E%E7%8E%B0%E5%AE%8C%E6%95%B4%E7%9A%84scpu)
>根据上文, 在sCPU中添加`bner0`指令. 实现后, 尝试让sCPU执行完整的数列求和程序, 如果你的实现正确, 你应该能看到PC最终为`7`, 且在某GPR中存放求和结果`55`.

可能的解法：[F5_Implement_addAbner0_function.circ](F5_Implement_addAbner0_function.circ)


<br>

5.[计算10以内的奇数之和](https://ysyx.oscc.cc/docs/2407/f/5.html#%E9%87%8D%E6%96%B0%E5%AE%A1%E8%A7%86cpu)
>编写一段指令序列, 计算10以内的奇数之和, 即`1+3+5+7+9`. 然后尝试用你设计的sCPU指令这段指令序列, 检查运行结果是否符合预期.

完成后, 你对计算机的"存储程序"思想有什么认识?

可能的解法：[F5_Implement_sumodd10_function.circ](F5_Implement_sumodd10_function.circ)

<br>

6.[添加新指令](https://ysyx.oscc.cc/docs/2407/f/5.html#%E9%87%8D%E6%96%B0%E5%AE%A1%E8%A7%86cpu)
>尝试为sISA添加一条新指令`out rs`, 执行该指令后, 会将`R[rs]`以十六进制的形式输出到七段数码管. 你可以自行决定这条指令的编码.

然后, 在sCPU中实现`out`指令, 并修改数列求和程序, 使得在计算出结果后, 能在七段数码管中显示计算结果.

可能的解法：[F5_Implement_outrs_function.circ](F5_Implement_outrs_function.circ)



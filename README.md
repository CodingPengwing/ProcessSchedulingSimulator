# Process Scheduling Simulator #

This program is a solution to project 1 of COMP30023 Computer Systems, University
of Melbourne. The specifications can be found in the repo.

This program is a simulation of a process scheduler in a CPU, based on the 
shortest-time-remaining process scheduling algorithm.. The program takes 2 inputs 
through command line: -f _filename_ -p _processors_

This tells the program where to read input from and how many processors in the
CPU it should simulate. The program then reads the input file line by line,
where each line represents a process and consists of a space-separated tuple 
- (_time-arrived_, _process-id_, _execution-time_, _parallelisable_)

Based on these parameters, the program should simulate a real life process
scheduler and show when a process is started, which processor is it running
on, and how many processes overall are remaining. At the end of the simulation
the program outputs 3 general statistics: 
- Average turnaround time
- Maximum and average overhead
- Total makespan

Run instructions:
- make

Then use the following run commands to see the output for each test input file.

RUN COMMANDS:
- ./allocate -p 1 -f testcases/task1/input/test_p1_n_1.txt
- ./allocate -p 1 -f testcases/task1/input/test_p1_n_2.txt
- ./allocate -p 2 -f testcases/task2/input/test_p2_n_1.txt
- ./allocate -p 2 -f testcases/task2/input/test_p2_n_2.txt
- ./allocate -p 2 -f testcases/task3/input/test_p2_p_1.txt
- ./allocate -p 2 -f testcases/task3/input/test_p2_p_2.txt
- ./allocate -p 4 -f testcases/task4/input/test_p4_n_1.txt
- ./allocate -p 4 -f testcases/task4/input/test_p4_n_2.txt
- ./allocate -p 4 -f testcases/task5/input/test_p4_p_1.txt
- ./allocate -p 4 -f testcases/task5/input/test_p4_p_2.txt
- ./allocate -p 1 -f testcases/task6/input/test_p1_n_1.txt
- ./allocate -p 4 -f testcases/task6/input/test_p4_p_2.txt
- ./allocate -p 2 -f testcases/task7/test_chal_p2_n.txt -c
- ./allocate -p 2 -f testcases/task7/test_chal_p2_p.txt -c
- ./allocate -p 3 -f testcases/task7/test_chal_p3_p.txt -c
- ./allocate -p 4 -f testcases/task7/test_chal_p4_n.txt -c
- ./allocate -p 4 -f testcases/task7/test_chal_p4_p.txt -c
- ./allocate -p 5 -f testcases/task7/test_chal_p5_n.txt -c
- ./allocate -p 5 -f testcases/task7/test_chal_p5_p.txt -c
- ./allocate -p 6 -f testcases/task7/test_chal_p6_n_equal.txt -c
- ./allocate -p 6 -f testcases/task7/test_chal_p6_p_equal.txt -c

Some expected output files were provided as part of the project, running the 
following commands will compare the output of the program to the expected outputs.
This uses a diff command, thus if the output is the same, nothing will be printed.

COMPARE TO EXPECTED OUTPUTS:
- ./allocate -p 1 -f testcases/task1/input/test_p1_n_1.txt | diff - testcases/task1/output/test_p1_n_1.out
- ./allocate -p 1 -f testcases/task1/input/test_p1_n_2.txt | diff - testcases/task1/output/test_p1_n_2.out
- ./allocate -p 2 -f testcases/task2/input/test_p2_n_1.txt | diff - testcases/task2/output/test_p2_n_1.out
- ./allocate -p 2 -f testcases/task2/input/test_p2_n_2.txt | diff - testcases/task2/output/test_p2_n_2.out
- ./allocate -p 2 -f testcases/task3/input/test_p2_p_1.txt | diff - testcases/task3/output/test_p2_p_1.out
- ./allocate -p 2 -f testcases/task3/input/test_p2_p_2.txt | diff - testcases/task3/output/test_p2_p_2.out
- ./allocate -p 4 -f testcases/task4/input/test_p4_n_1.txt | diff - testcases/task4/output/test_p4_n_1.out
- ./allocate -p 4 -f testcases/task4/input/test_p4_n_2.txt | diff - testcases/task4/output/test_p4_n_2.out
- ./allocate -p 4 -f testcases/task5/input/test_p4_p_1.txt | diff - testcases/task5/output/test_p4_p_1.out
- ./allocate -p 4 -f testcases/task5/input/test_p4_p_2.txt | diff - testcases/task5/output/test_p4_p_2.out
- ./allocate -p 1 -f testcases/task6/input/test_p1_n_1.txt | diff - testcases/task6/output/test_p1_n_1.out
- ./allocate -p 4 -f testcases/task6/input/test_p4_p_2.txt | diff - testcases/task6/output/test_p4_p_2.out

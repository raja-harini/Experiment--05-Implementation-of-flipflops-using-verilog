# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
/* write all the steps invloved */



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: HARINI R
RegisterNumber:  23000779
*/
![CODE SRFPFP](https://github.com/raja-harini/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037372/a161d7b9-f02c-4754-9be7-fec1acec8c4b)
![WAVE FORM SRFPFP](https://github.com/raja-harini/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037372/65a076fb-7729-47b9-aa27-9027176b2ff6)
![CODE DFPFP](https://github.com/raja-harini/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037372/9a711212-9f45-4bd7-9a47-6d765dd4360e)
![WAVE FORM DFPFP](https://github.com/raja-harini/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037372/fe39c500-509b-45d3-a8ee-f35357729eb2)
![CODE JKFPFP](https://github.com/raja-harini/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037372/c4eee5c1-cca7-4a63-8a9f-9506176e3681)
![WAVE FORM JKFPFP](https://github.com/raja-harini/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037372/cab86fc7-e10f-4d89-acab-76eec67ba7da)
![CODE TFPFP](https://github.com/raja-harini/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037372/78297c04-116b-4206-b48d-6c66fc8803d2)
![WAVE FORM TFPFP](https://github.com/raja-harini/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037372/ac238bb1-fc64-418b-aa11-1cd2a9d04208)

### RTL LOGIC FOR FLIPFLOPS 
![LOGIC DIAGRAM SRFPFP](https://github.com/raja-harini/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037372/9403d6eb-98b7-4a56-a2b7-a6dc65aa8d42)
![LOGIC DIAGRAM DFPFP](https://github.com/raja-harini/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037372/ea13d760-9934-41e2-b8da-d78a76b958c6)
![LOGIC DIAGRAM JKFPFP](https://github.com/raja-harini/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037372/b0c1424c-b694-4060-90c7-5db6c9ae5a9b)
![LOGIC DIAGRAM TFPFP](https://github.com/raja-harini/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037372/82f9b95c-45a7-47f5-b47e-d47aabcd69be)

### TIMING DIGRAMS FOR FLIP FLOPS 
![TIMING DIAGRAM SRFPFP](https://github.com/raja-harini/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037372/80ce7031-3411-49e7-abb8-791c7a1f264f)
![TIMING DIAGRAM DFPFP](https://github.com/raja-harini/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037372/349e1014-2bdf-48e8-b031-e783829e52e9)
![TIMING DIAGRAM JKFPFP](https://github.com/raja-harini/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037372/f07afcf3-cbef-4350-a97c-1d8ace575cb9)
![TIMING DIAGRAM  TFPFP](https://github.com/raja-harini/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037372/2fcf4029-484c-4fe5-aaf0-d32fff458372)

### RESULTS 

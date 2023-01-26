# Full-Adder-Design
Full Adder using two half adder in verilog code.


module full_adder(Clr,A,B,Cin,Sum,Carry);  
input Clr,A,B,Cin;
output Sum,Carry;
wire w1,w2,w3,w4,w5,w6;
and and1(w1,A,Clr);
and and2(w2,B,Clr);
and and3(w3,Cin,Clr);
half_adder hf1(Clr,w1,w2,w4,w5);
half_adder hf2(Clr,w3,w4,Sum,w6);
or or1(Carry,w5,w6);
endmodule

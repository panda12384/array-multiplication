module halfadd(a,b,s,c);
input a,b;
output s,c;
assign s=a^b;
assign c=a&b;
endmodule

module fulladd(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum= a^b^c;
assign carry=(a&b)|(b&c)|(a&c);
endmodule

module arraymul(m,n,z);
input [3:0]m,n;
output [7:0]z;
wire signed p[3:0][3:0];
wire [10:0]d;
wire [5:0]s;
genvar g;
generate
for(g=0; g<4 ; g=g+1)
begin
 and a0(p[g][0],m[g],n[0]);
 and a1(p[g][1],m[g],n[1]);
 and a2(p[g][2],m[g],n[2]);
 and a3(p[g][3],m[g],n[3]);
 end
 endgenerate
 assign z[0]=p[0][0];
 //row 1
 halfadd h0(p[0][1],p[1][0],z[1],d[0]);
 halfadd h1(p[1][1],p[2][0],s[0],d[1]);
 halfadd h2(p[2][1],p[3][0],s[2],d[2]);
 //row 2
 fulladd f0(p[0][2],s[0],d[0],z[2],d[3]);
 fulladd f1(p[1][2],s[1],d[1],s[2],d[4]);
 fulladd f2(p[2][2],p[3][1],d[2],s[3],d[5]);
 //row 3
 fulladd f3(p[0][3],s[2],d[3],z[3],d[6]);
 fulladd f4(p[1][3],s[3],d[4],s[4],d[7]);
 fulladd f5(p[2][3],p[3][2],d[5],s[5],d[8]);
 //row 4
halfadd h3(d[6],s[4],d[9],z[4]);
fulladd h6(d[7],s[5],d[9],z[5],d[10]);
fulladd h7(d[10],d[8],p[3][3],z[6],z[7]);

endmodule
 
 
 
 

 
 


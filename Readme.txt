PROJECT : Encryption and decryption using Hill cipher
CREATED BY: Gaurav Lahoti
Date : 4/3/11

Salient Features :
1.) Supports 89 characters. Alongwith encrypting huge number of day to day characters and alphabets, another thing worth mentioning is the number 89. It is a prime number, hence, we don't have to see for the key matrix determinant and modulous having a common factor except 1 and 89 as it renders the Key matrix useless. The characters supported are :
A-Z : 26
a-z : 26
0-9 : 10
!@#$%^&*()-=_+[]{};:,./<>? : 26 (NOT INCLUDED are: ~`'"\|)
Space: 1
TOTAL : 89
Although, the support has been created for 97 characters, I am using only 89 because line feed, carriage return and " create some problems while parsing the data.
(Mapping is given at the end of this file)


2.) The program can invert any nxn matrix, provided it is invertible. Therefore, your can have any nxn matrix as the key but it is recommended to not have very large matrices as it may put a lot of additional load on the server.


3.) The algorithm for decryption is only valid for character set having the prime number of elements. As the calculation of inverse has been done only for prime numbers. For non primes, the inverse would be wrong, giving us a wrong result.


4.) The encryption is done for all the keys. The decryption is done only for keys which are invertible.


5.) A 3x3 key can be entered quickly in the 3x3 matrix. But if you want a nxn matrix where n>1, use the commandline. The key in the commandline can be entered as:
45 3 2 3 6 2;3 2 3 53 2 3;5 2 7 8 5 2;2 7 8 9 1 5;3 5 2 7 8 5;3 3 4 3 8 9
This is a invertible 6x6 matrix. The guidelines are:
1.) Start with a number. This number is K(1,1) of the matrix.
2.) Enter the values row wise i.e. 1st row, then 2nd etc..
3.) Leave a space between elements of the same row.
4.) Put a semicolon when you want to enter data for a new row.
5.) Put only square matrices as the program will flag error if the key is not a square matrix.
6.) If data is entered in commandline, it will override the data written in 3x3 matrix.


6.) One on One Mapping:
No.		Character
/ <--> 0
0 <--> 1
1 <--> 2
2 <--> 3
3 <--> 4
4 <--> 5
5 <--> 6
6 <--> 7
7 <--> 8
8 <--> 9
9 <--> 10
A <--> 11
B <--> 12
C <--> 13
D <--> 14
E <--> 15
F <--> 16
G <--> 17
H <--> 18
I <--> 19
J <--> 20
K <--> 21
L <--> 22
M <--> 23
N <--> 24
O <--> 25
P <--> 26
Q <--> 27
R <--> 28
S <--> 29
T <--> 30
U <--> 31
V <--> 32
W <--> 33
X <--> 34
Y <--> 35
Z <--> 36
a <--> 37
b <--> 38
c <--> 39
d <--> 40
e <--> 41
f <--> 42
g <--> 43
h <--> 44
i <--> 45
j <--> 46
k <--> 47
l <--> 48
m <--> 49
n <--> 50
o <--> 51
p <--> 52
q <--> 53
r <--> 54
s <--> 55
t <--> 56
u <--> 57
v <--> 58
w <--> 59
x <--> 60
y <--> 61
z <--> 62
, <--> 63
  <--> 64
! <--> 65
@ <--> 66
# <--> 67
$ <--> 68
% <--> 69
^ <--> 70
& <--> 71
* <--> 72
( <--> 73
) <--> 74
- <--> 75
= <--> 76
_ <--> 77
+ <--> 78
[ <--> 79
] <--> 80
? <--> 81
{ <--> 82
} <--> 83
< <--> 84
; <--> 85
. <--> 86
: <--> 87
> <--> 88 <--- Values till will be used in the program (As total_char = 89)
~ <--> 89
\' <--> 90
` <--> 91
| <--> 92
\" <--> 93
\\ <--> 94
\n <--> 95
\r <--> 96
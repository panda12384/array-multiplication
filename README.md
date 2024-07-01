**ARRAY MULTIPLICATION**

# ![Array_Us](https://github.com/panda12384/HDL/assets/160568759/9d1383f6-3d49-44b4-9bc6-c80a7f232ab1)


An array multiplier is a digital combinational circuit used to multiply two binary numbers by employing an array of full and half adders. This array is used for nearly simultaneously adding the various product terms involved. An array of AND gates is used before the Adder array to form the various product terms.

Checking the bits of the multiplier one at a time and forming partial products is a sequential operation that requires a sequence of add and shift micro-operations. The multiplication of two binary numbers can be done with one micro-operation employing a combinational circuit that forms the product bits all at once. This is a fast way of multiplying two numbers since all it takes is the time for the signals to propagate through the gates that form the multiplication array. However, an array multiplier requires a large number of gates, and for this reason, it was not economical until the development of integrated circuits.

![4-by-4-multiplication-1](https://github.com/panda12384/HDL/assets/160568759/07e2c89c-066f-43a7-9ede-e29250541cfd)

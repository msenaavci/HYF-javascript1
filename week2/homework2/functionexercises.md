[problem 1]

http://www.pythontutor.com/javascript.html#code=%7B%20%20%20//%201%0A%20%20function%20f%28param_1,%20param_2,%20param_3%29%20%7B%0A%20%20%20%20var%20result%20%3D%20param_3%20%2B%20param_1%20%2B%20param_2%3B%0A%20%20%20%20return%20result%3B%0A%20%20%7D%3B%0A%0A%20%20//%20set%20values%20in%20the%20args%20to%20pass%20the%20assert%0A%20%20let%20arg_1%20%3D%20%22y%22,%20arg_2%20%3D%20%22x%22,%20arg_3%20%3D%20%22z%22%3B%0A%20%20let%20return_val%20%3D%20f%28arg_1,%20arg_2,%20arg_3%29%3B%0A%0A%20%20console.assert%28return_val%20%3D%3D%3D%20%22zyx%22,%20%221%3A%20return_val%20%3D%3D%3D%20%22%20%2B%20return_val%29%3B%0A%7D&curInstr=4&mode=display&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D

[problem 2]

http://www.pythontutor.com/javascript.html#code=%7B%20%20//%202%0A%20%20function%20f%28param_1,%20param_2,%20param_3%29%20%7B%0A%20%20%20%20var%20result%20%3D%20param_3%20%2B%20param_1%20%2B%20param_2%3B%0A%20%20%20%20return%20result%3B%0A%20%20%7D%3B%0A%0A%20%20//%20set%20values%20in%20the%20args%20to%20pass%20the%20assert%0A%20%20let%20arg_1%20%3D%20%22x%22,%20arg_2%20%3D%20%22z%22,%20arg_3%20%3D%20%22y%22%3B%0A%20%20let%20return_val%20%3D%20f%28arg_1,%20arg_2,%20arg_3%29%3B%0A%0A%20%20console.assert%28return_val%20%3D%3D%3D%20%22yxz%22,%20%222%3A%20return_val%20%3D%3D%3D%20%22%20%2B%20return_val%29%3B%0A%7D&curInstr=5&mode=display&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D

[problem 3]

http://www.pythontutor.com/javascript.html#code=%7B%20%20//%203%0A%20%20function%20f%28param_1,%20param_2,%20param_3%29%20%7B%0A%20%20%20%20var%20_%20%3D%20param_2%3B%0A%20%20%20%20param_2%20%3D%20param_1%3B%0A%20%20%20%20param_1%20%3D%20_%3B%0A%20%20%20%20var%20result%20%3D%20param_3%20%2B%20param_1%20%2B%20param_2%3B%0A%20%20%20%20return%20result%3B%0A%20%20%7D%3B%0A%0A%20%20//%20set%20values%20in%20the%20args%20to%20pass%20the%20assert%0A%20%20let%20arg_1%20%3D%20%22z%22,%20arg_2%20%3D%20%22x%22,%20arg_3%20%3D%20%22y%22%3B%0A%20%20let%20return_val%20%3D%20f%28arg_1,%20arg_2,%20arg_3%29%3B%0A%0A%20%20console.assert%28return_val%20%3D%3D%3D%20%22yxz%22,%20%223%3A%20return_val%20%3D%3D%3D%20%22%20%2B%20return_val%29%3B%0A%7D%0A&curInstr=9&mode=display&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D

[problem 4]

http://www.pythontutor.com/javascript.html#code=%7B%20%20//%204%0A%20%20function%20f%28param_1,%20param_2,%20param_3%29%20%7B%0A%20%20%20%20var%20_%20%3D%20param_2%3B%0A%20%20%20%20param_2%20%3D%20param_3%3B%0A%20%20%20%20param_3%20%3D%20_%3B%0A%20%20%20%20var%20result%20%3D%20param_3%20%2B%20param_1%20%2B%20param_2%3B%0A%20%20%20%20return%20result%3B%0A%20%20%7D%3B%0A%0A%20%20//%20set%20values%20in%20the%20args%20to%20pass%20the%20assert%0A%20%20let%20arg_1%20%3D%20%22y%22,%20arg_2%20%3D%20%22x%22,%20arg_3%20%3D%20%22z%22%3B%0A%20%20let%20return_val%20%3D%20f%28arg_1,%20arg_2,%20arg_3%29%3B%0A%0A%20%20console.assert%28return_val%20%3D%3D%3D%20%22xyz%22,%20%224%3A%20return_val%20%3D%3D%3D%20%22%20%2B%20return_val%29%3B%0A%7D&curInstr=9&mode=display&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D

[problem 5]

http://www.pythontutor.com/javascript.html#code=%7B%20%20//%205%0A%20%20%20function%20f%28param_1,%20param_2,%20param_3%29%20%7B%0A%20%20%20%20var%20result%20%3D%20param_3%20%2B%20param_1%20%2B%20param_2%3B%0A%20%20%20%20return%20result%3B%0A%20%20%20%7D%3B%0A%0A%20%20%20let%20x%20%3D%20%22x%22,%20y%20%3D%20%22y%22,%20z%20%3D%20%22z%22%3B%0A%20%20%20let%20return_val%20%3D%20f%28y,z,x%29%3B%0A%0A%20%20%20console.assert%28return_val%20%3D%3D%3D%20%22xyz%22,%20%225%3A%20return_val%20%3D%3D%3D%20%22%20%2B%20return_val%29%3B%0A%7D&curInstr=6&mode=display&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D

[problem 6]

http://www.pythontutor.com/javascript.html#code=%7B%20%20//%206%0A%20%20%20function%20f%28param_1,%20param_2,%20param_3%29%20%7B%0A%20%20%20%20var%20result%20%3D%20param_2%20%2B%20param_1%20%2B%20param_3%3B%0A%20%20%20%20return%20result%3B%0A%20%20%20%7D%3B%0A%0A%20%20%20let%20x%20%3D%20%22x%22,%20y%20%3D%20%22y%22,%20z%20%3D%20%22z%22%3B%0A%20%20%20let%20return_val%20%3D%20f%28z,x,y%29%3B%0A%0A%20%20%20console.assert%28return_val%20%3D%3D%3D%20%22xzy%22,%20%226%3A%20return_val%20%3D%3D%3D%20%22%20%2B%20return_val%29%3B%0A%7D&curInstr=6&mode=display&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D

[problem 7]

http://www.pythontutor.com/javascript.html#code=%7B%20%20//%207%0A%20%20%20function%20f%28param_1,%20param_2,%20param_3%29%20%7B%0A%20%20%20%20var%20result%20%3D%20param_3%20%2B%20param_1%20%2B%20param_2%3B%0A%20%20%20%20return%20result%3B%0A%20%20%20%7D%3B%0A%0A%20%20%20let%20arg_1%20%3D%20%22z%22,%20arg_2%20%3D%20%22y%22,%20arg_3%20%3D%20%22x%22%3B%0A%20%20%20let%20return_val%20%3D%20f%28arg_1,%20arg_2,%20arg_3%29%3B%0A%0A%20%20%20console.assert%28return_val%20%3D%3D%3D%20%22xzy%22,%20%227%3A%20return_val%20%3D%3D%3D%20%22%20%2B%20return_val%29%3B%0A%7D%0A&curInstr=6&mode=display&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D

[problem 8]

http://www.pythontutor.com/javascript.html#code=%7B%20%20//%208%0A%20%20%20function%20f%28param_1,%20param_2,%20param_3%29%20%7B%0A%20%20%20%20var%20result%20%3D%20param_2%20%2B%20param_3%20%2B%20param_1%3B%0A%20%20%20%20return%20result%3B%0A%20%20%20%7D%3B%0A%0A%20%20%20let%20arg_1%20%3D%20%22z%22,%20arg_2%20%3D%20%22y%22,%20arg_3%20%3D%20%22x%22%3B%0A%20%20%20let%20return_val%20%3D%20f%28arg_1,%20arg_2,%20arg_3%29%3B%0A%0A%20%20%20console.assert%28return_val%20%3D%3D%3D%20%22yxz%22,%20%228%3A%20return_val%20%3D%3D%3D%20%22%20%2B%20return_val%29%3B%0A%7D&curInstr=6&mode=display&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D



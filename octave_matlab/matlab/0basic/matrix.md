```matlab
# create
## create sequence a : [1, 9], step=2
a = [1 : 2 : 9]
## create array a with [[1,2,3], [4, 5, 2], [3, 2, 7]]
a = [1 2 3 ; 4 5 2 ; 3 2 7]

# evaluate the transposed matrix of a  | save to b
b = a'

# cp matrix a, convert into a col_vec | save to c
c = a(:)

# evaluate the inverse matrix of a | save to d
d = inv(a)

# create a (row = 10,col = 5, dim = 3) zeros matrix e
e = zeros(10, 5, 3)

# create a (2, 4) ones_matrix f
f = ones(2, 4)

# random
## overwrite the dim1 of matrix e with a (10, 5) random_array whose elements in [0, 1)
e(:,:,1) = rand(10, 5)

## overwite the dim2 of matrix e with a (10, 5) random_array whose elements uniformly distribute in [0, 5)
e(:,:,2) = randi(5,10,5) 

## overwite the dim3 of matrix e with a (10, 5) random_array whose elements in [0,5) and follows standard normal distribution
e(:,:,3) = randn(5, 10)

# operation
## element operation
A + B
A - B
A .* B
A ./ B
## matrix operation
A * B
A / B	# equivalent to A * inv(B)

# index
A = magic(5)
B = A(2, 3)	## cp A[2, 3] to B
C = A(3, :)	## cp row3 of array A to C
D = A(:, 4)	## cp col4 of array A to D
[m, n] = find(A > 20)	## save [row_index, col_index] of elements > 20 from matrix A to [m, n]
```
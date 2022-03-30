# -
摘抄于网上资料
![image](https://user-images.githubusercontent.com/92030898/160863176-e9976785-4741-4b54-a062-2765d1e13a9a.png)
![image](https://user-images.githubusercontent.com/92030898/160863324-ab1ff310-bde4-4f3a-9f6f-2fb439c29d0c.png)
![image](https://user-images.githubusercontent.com/92030898/160863374-47874431-bde7-4486-aca3-10d83ca31910.png)
![image](https://user-images.githubusercontent.com/92030898/160863429-66bec600-b91f-4242-820c-f9ae4f8dea27.png)
![image](https://user-images.githubusercontent.com/92030898/160863524-412892f0-06bf-47af-8e7f-e405bbd97f04.png)
![image](https://user-images.githubusercontent.com/92030898/160863583-27624ded-70fd-4484-bd4e-a639c6ff6941.png)
# Create a figure with 3x1 subplot and activate the top subplot
plt.subplot(3, 1, 1)
plt.plot(tv['super_bowl'], tv['avg_us_viewers'], color='#648FFF')
plt.title('Average Number of US Viewers')

# Activate the middle subplot
plt.subplot(3, 1, 2)
plt.plot(tv['super_bowl'], tv['rating_household'], color='#DC267F')
plt.title('Household Rating')

# Activate the bottom subplot
plt.subplot(3, 1, 3)
plt.plot(tv['super_bowl'], tv['ad_cost'], color='#FFB000')
plt.title('Ad Cost')
plt.xlabel('SUPER BOWL')

# Improve the spacing between subplots
plt.tight_layout()
![image](https://user-images.githubusercontent.com/92030898/160863653-e49dbdfd-0226-45fb-838f-369db57b0ad6.png)
![image](https://user-images.githubusercontent.com/92030898/160864381-dfb889ee-bb63-4209-a527-52fae65542b2.png)
import numpy as np

t1 = np.array([1, 2, 3])
print("t1 =", end=" ")
print(t1)
print(type(t1))
print("="*30)

t2 = np.array(range(10))
print("t2 =", end = " ")
print(t2)
print(type(t2))
print("="*30)

t3 = np.arange(10)
print("t3 =", end = " ")
print(t3)
print(type(t3))

t1 = [1 2 3]
<class 'numpy.ndarray'>
==============================
t2 = [0 1 2 3 4 5 6 7 8 9]
<class 'numpy.ndarray'>
==============================
t3 = [0 1 2 3 4 5 6 7 8 9]
<class 'numpy.ndarray'>
![image](https://user-images.githubusercontent.com/92030898/160864714-7348b3c1-2363-43a2-93f3-195ef2f1afb4.png)
t4 = np.array(range(10), dtype="i1")
print("t4 = ", t4)
print(t4.dtype)
print("="*50)

t5 = t4.astype("bool")
print("t5 =", end = " ")
print(t5)
print(t5.dtype)
**t4 =  [0 1 2 3 4 5 6 7 8 9]
int8
==================================================
t5 = [False  True  True  True  True  True  True  True  True  True]
bool
**
![image](https://user-images.githubusercontent.com/92030898/160865226-3f1e5aad-b795-4529-8649-fffafb0959a1.png)
import random as rd

randArray = np.array([rd.random() for i in range(6)])
print("randArray =", end=" ")
print(randArray)

roundedRandArray = np.round(randArray, 2)
print("roundedRandArray =", end=" ")
print(roundedRandArray)

randArray = [0.37565108 0.62705101 0.69833369 0.39981917 0.39699408 0.62154934]
roundedRandArray = [0.38 0.63 0.7  0.4  0.4  0.62]
![image](https://user-images.githubusercontent.com/92030898/160865558-4558f68b-5b2d-4f91-8da7-8f795b299ccb.png)
![image](https://user-images.githubusercontent.com/92030898/160866802-e341bb8f-dbc3-4e0f-8bf7-0b2bd57e608a.png)
t3 = t2.reshape((2, 5))
print("t3 = ", t3)

print("t3.flatten() = ", t3.flatten())


t3 = [0 1 2 3 4 5 6 7 8 9]
t3 =  [[0 1 2 3 4]
 [5 6 7 8 9]]
t3.flatten() =  [0 1 2 3 4 5 6 7 8 9]
![image](https://user-images.githubusercontent.com/92030898/160867167-1c4cfa05-b535-4dba-a792-d9564314f343.png)
A = np.array([
    [1, -5, 12, 9],
    [6, -1, -5, 3],
    [0, 12, 32, 8]])
print("="*10, " Get row, col ", "="*10)
# 1.取行，例如取第二行
print("A[1] = \n", A[1])
# 2.取列，例如取第一列
print("\n A[:,0] = \n", A[:,0])
# 3.取连续的多列，例如取第 3-4 列
print("\n A[:, 2:4] = \n", A[:, 2:4])
# 4.取间断的多列，例如取第 1, 3, 4 列
print("\n A[:, [0, 2, 3]] = \n", A[:, [0, 2, 3]])

print("="*10, " Get elements ", "="*10)
# 5.指定索引取得多个元素,例如取得 A[1, 1], A[1, 3], A[2, 1]
print("res = \n", A[[1, 1, 2], [1, 3, 1]])
#######
A = np.array([
    [1, -5, 12, 9],
    [6, -1, -5, 3],
    [0, 12, 32, 8]])
==========  Get row, col  ==========
# 1.取行，例如取第二行
A[1] = 
 [ 6 -1 -5  3]
# 2.取列，例如取第一列
 A[:,0] = 
 [1 6 0]
# 3.取连续的多列，例如取第 3-4 列
 A[:, 2:4] = 
 [[12  9]
 [-5  3]
 [32  8]]
# 4.取间断的多列，例如取第 1, 3, 4 列
 A[:, [0, 2, 3]] = 
 [[ 1 12  9]
 [ 6 -5  3]
 [ 0 32  8]]
==========  Get elements  ==========
# 5.指定索引取得多个元素,例如取得 A[1, 1], A[1, 3], A[2, 1]
res = 
 [-1  3 12]
 ![image](https://user-images.githubusercontent.com/92030898/160868862-39b46ad7-b13f-4c64-975a-b68280bcaafd.png)
print("A = \n", A)
A_vert = np.vstack((A, A))
print("\n A_vert =\n", A_vert)
A_horizon = np.hstack((A, A))
print("\n A_horizon = \n", A_horizon)
*******
A = 
 [[ 1 -5 12  9]
 [ 6 -1 -5  3]
 [ 0 12 32  8]]

 A_vert =
 [[ 1 -5 12  9]
 [ 6 -1 -5  3]
 [ 0 12 32  8]
 [ 1 -5 12  9]
 [ 6 -1 -5  3]
 [ 0 12 32  8]]

 A_horizon = 
 [[ 1 -5 12  9  1 -5 12  9]
 [ 6 -1 -5  3  6 -1 -5  3]
 [ 0 12 32  8  0 12 32  8]]
# 1. A.shape == B.shape
print("***************** A.shape == B.shape *****************")
A = np.arange(0, 10).reshape((2, 5))
B = np.arange(10, 20).reshape(2, 5)
print("A = ", A); print()
print("B = ", B); print()
print("A + B = ", A+B); print()
print("A * B = ", A*B)

# 2. col(A) == col(B) && row(A) == 1
print("***************** col(A) == col(B) && row(A) == 1 *****************")
A = np.arange(0, 5)
print("A = ", A);print()
print("B = ", B); print()
print("A + B = ", A+B); print()
print("A * B = ", A*B)

#3. row(A) == row(B) && col(A) != 1
print("***************** row(A) == row(B) && col(A) != 1 *****************")
A = np.arange(6).reshape(3, 2)
B = np.arange(12).reshape(3, 4)
print("A = ", A);print()
print("B = ", B); 
print('''
ERROR: A+B
ERROR: A*B
'''
)
********************************* A.shape == B.shape *****************
A =  [[0 1 2 3 4]
 [5 6 7 8 9]]

B =  [[10 11 12 13 14]
 [15 16 17 18 19]]

A + B =  [[10 12 14 16 18]
 [20 22 24 26 28]]

A * B =  [[  0  11  24  39  56]
 [ 75  96 119 144 171]]
***************** col(A) == col(B) && row(A) == 1 *****************
A =  [0 1 2 3 4]

B =  [[10 11 12 13 14]
 [15 16 17 18 19]]

A + B =  [[10 12 14 16 18]
 [15 17 19 21 23]]

A * B =  [[ 0 11 24 39 56]
 [ 0 16 34 54 76]]
***************** row(A) == row(B) && col(A) != 1 *****************
A =  [[0 1]
 [2 3]
 [4 5]]

B =  [[ 0  1  2  3]
 [ 4  5  6  7]
 [ 8  9 10 11]]

ERROR: A+B
ERROR: A*B
![image](https://user-images.githubusercontent.com/92030898/160871099-82f867f5-ad82-4723-975d-ab9bc7da53db.png)
A = np.array([
    [rd.randint(0, 10) for i in range(10)],
    [rd.randint(0, 10) for i in range(10)],
    [rd.randint(0, 10) for i in range(10)]])
print("*"*20, " Before setting elements=5 ", "*"*20)
print("A = \n", A)

print("*"*20, " After  setting elements=5 ", "*"*20)
A[A>5] = 5
print("A = \n", A)
********************  Before setting elements=5  ********************
A = 
 [[ 0  2  5  5  1  4  5  7  9  9]
 [ 9  4  2  4 10  0  0  4  4  1]
 [ 6  3  5  8  1  0  8  3  0  9]]
********************  After  setting elements=5  ********************
A = 
 [[0 2 5 5 1 4 5 5 5 5]
 [5 4 2 4 5 0 0 4 4 1]
 [5 3 5 5 1 0 5 3 0 5]]
![image](https://user-images.githubusercontent.com/92030898/160872067-98d68a25-5199-44ec-8776-194b4e48348d.png)
![image](https://user-images.githubusercontent.com/92030898/160872187-b026a830-afc5-4fb1-a1bb-b4cad4f643a7.png)
![image](https://user-images.githubusercontent.com/92030898/160872233-1e7f5a0d-8d3b-4307-8c46-5c50595d03d9.png)
print("A = \n", A)
# 1.计算每一列的和
print("A.sum(axis=0) = \n", A.sum(axis=0))
# 2.计算每一列的平均值并取整
print("A.mean(axis=0) = \n", A.mean(axis=0).astype("i1"))
**A = 
 [[4 5 2 5 1 4 5 5 5 2]
 [0 5 5 3 4 5 2 1 5 5]
 [0 5 5 5 5 5 1 1 3 2]]
A.sum(axis=0) = 
 [ 4 15 12 13 10 14  8  7 13  9]
A.mean(axis=0) = 
 [1 5 4 4 3 4 2 2 4 3]
**
![image](https://user-images.githubusercontent.com/92030898/160873196-afc59101-d1e8-4cd6-9073-dde9c774ed8b.png)
![image](https://user-images.githubusercontent.com/92030898/160873574-c1666854-e72d-4233-9faa-aa12b360b146.png)

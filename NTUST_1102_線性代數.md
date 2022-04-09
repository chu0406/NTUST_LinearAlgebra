# NTUST_1102_線性代數
## 1.1 System of Linear Equation
### m*n linear system
- no solution：inconsistent
    - 平行線![](https://i.imgur.com/e0nKtJp.png =250x)
- 至少一個解：consistent
    - 一交點![](https://i.imgur.com/CLMzCwn.png =250x)
- The set of all solutions -> solution set
    - 重合線![](https://i.imgur.com/YFxYbP0.png =250x)
### Equivalent System
- 定義：如果兩個 linear system 具有相同數目的未知數，並且有相同的解(必須是一樣的集合)。那我們說這兩個 system Equivalent(相等)。
- Example:
     ![](https://i.imgur.com/jIdzmyb.png =500x)
- 可以在系統上使用以下操作得到 Equivalent system：
    - 任兩個方程式的書寫順序交換(intercharged)
    - 等式的兩邊都可以乘以相同的非零實數
    - 一個方程的倍數可以➕/➖到另一個方程(added/subtracted)
### Strict triangular form
- 定義：如果在一個 system 中，第 k 個等式的前 k - 1 個變數的係數都是 0，而第 k 個變數的係數不為 0。那就稱這個形式為 strict triangular form。
- 基本上這個 system 看起來類似倒三角形
- Example:
    - ![](https://i.imgur.com/9ern6wU.png =250x)
- How to solve?
    - back substitution (反向替換)
### Elementary row operations
1. 交換(interchange)兩個row
2. ✖️一個非零的真數(real number)
3. 用另一row的倍數替換一row。
## 1.2 Row Echelon Form
### Row echelon form (REF)
- 有以下性質者被稱為REF：
    1. 每行row的首個非零元素為1
    2. 若第k個row不全由0組成，則row k+1的前導0的數量>row k
    3. 如果存在row全為零的行，則位於有非零row之下
- Note
    - 若REF含有[0 0 0...0|1]形式的增廣(augmented)矩陣則為inconsistent
    - 除上以外者皆為consistent
    - 若有一system為++consistent++以及REF中非零的row是++strictly triangular system++，則此系統有唯一解
- REF examples:
    - ![](https://i.imgur.com/jvApyyq.png =80x)、![](https://i.imgur.com/gA1txQ1.png =80x)、![](https://i.imgur.com/qB3r2qN.png =110x)
- ++NOT++ REF examples:
    - ![](https://i.imgur.com/IyTjnPF.png =80x)、![](https://i.imgur.com/LGWn6zx.png =100x)、![](https://i.imgur.com/89f6uiw.png =70x)
- Gaussian elimination (高斯消去法)
    - 使用Elementary row operations將線性系統轉換成REF
### Overdetermined System
- 定義：如果一線性系統中，方程式數量m > 未知數n ，則稱由 m 個方程和 n 個未知數組成的線性系統是overdetermined的。(m>n)
- overdetermined system 通常是(but not always) inconsistent.
- Examples:
    - ![](https://i.imgur.com/26bGffP.png =180x)
     Sol:
         ![](https://i.imgur.com/EGkTIQg.png =200x)
 ### Underdetermined Systems
- 定義：如果一線性系統中，方程式數量m < 未知數n ，則稱由 m 個方程和 n 個未知數組成的線性系統是underdetermined的。(m<n)
- consistent的underdetermined system會有無限多組解
- Examples:
    - ![](https://i.imgur.com/NdSzd8y.png =200x)
    Sol:
    ![](https://i.imgur.com/FQybkv9.png =250x)
    
    - ![](https://i.imgur.com/vcdG04o.jpg =300x)
    Sol: 
    ![](https://i.imgur.com/yTweW9U.png =220x)![](https://i.imgur.com/pFJi1P7.png =331x)
### Reduced Row Echelon Form (RREF)
- 有以下性質者為RREF
    1. 是REF
    2. 第一個非零是其column中唯一的非零。
- RREF examples:![](https://i.imgur.com/mODeSDB.png =60x)、![](https://i.imgur.com/6sOj9zk.png =100x)、![](https://i.imgur.com/svADj6V.png =110x)、![](https://i.imgur.com/aUdOCCF.png =110x)
- Gauss-Jordan reduction
    - 使用Elementary row operations講線性系統轉換成RREF
    - Example:
     ![](https://i.imgur.com/0ZNFVFq.png =250x)
     Sol:
     ![](https://i.imgur.com/Wbzlbqk.png =150x)->![](https://i.imgur.com/UxLZRem.png =120x)->![](https://i.imgur.com/aGAZZsl.png =120x)--->![](https://i.imgur.com/H8IIJnX.png =190x)->![](https://i.imgur.com/khek1gp.png =120x)->![](https://i.imgur.com/oOZBUsC.png =190x)
### Homogeneous Systems
 - 定義：一系統如果右手邊的常數都為零，則為homogeneous
 - 必定是consistent，因為有trivial solution(0,0,...,0)
### Theorem 1.2.1
- 若有ㄧm*n的線性homogeneous system，if n > m 有nontrivial solotion
## 1.3 Matrix Algebra Matrix Notation
### Vector 
- Row vector:a 1*n matrix,e.g.,![](https://i.imgur.com/5DNsMom.png =100x)
- Column vector:an n*1 matrix,e.g.,![](https://i.imgur.com/3Utn6R8.png =40x)
- n*1 matrix 真數的集合又稱為Euclidean n-space 、 $R^n$.
- 若有一m*n matrix A
    - 第i個row vector:![](https://i.imgur.com/yZ0HCKJ.png =30x), ![](https://i.imgur.com/UzkeVD6.png =350x)
    - 第j個column vector:![](https://i.imgur.com/plqBgsr.png =30x), ![](https://i.imgur.com/DkPpeYq.png =270x)
    - matrix A 可用其row & column vector來表示:![](https://i.imgur.com/mPuF8da.png =270x) 
### Equality
- 定義：兩個m*n 矩陣Ａ、Ｂ，若$a_{ij} = b_{ij}$，則A＝B (equal)
### Scalar Multiplication
- 定義：A是一m*n矩陣，$\alpha$是一純量(scalar)，$\alpha$A = $\alpha a_{ij}$
### Matrix Addition
- 定義：有兩個m*n矩陣 A = ($a_{ij}$), B = ($b_{ij}$),A+B = $a_{ij}+b_{ij}$
- $A - B = A + (-1)B$
- $O$為一全為零之矩陣，則：
    - $O$的加法：$A+O=O+A=A$
    - $A+(-1)A=O=(-1)A+A$
- $-A=(-1)A$
### Matrix Multiplication and Linear Systems
- ++Case1++ ：一方程有數個未知數
    - 一線性方程有n個未知：$a_1 x_1+a_2 x_2+...+a_n x_n=b$
    - 設 $A=[a_1,a_2,...a_n]$, $x=\left[\begin{array}{c}x_1  \\x_2  \\.\\.\\x_n  \\\end{array}\right]$
    - scalar product(純量乘積）$Ax = a_1x_1+a_2x_2+...+a_nx_n=b$
- ++Case2++：Ｍ個方程有Ｎ個未知數
    - 考慮一個Ｍ＊Ｎ線性系統：
         ![](https://i.imgur.com/xK2bR3E.png =300x)
    - 表示成矩陣系統 Ax=b：
         ![](https://i.imgur.com/pJHR8HB.png =350x)
    - 定義一個product Ax:
         ![](https://i.imgur.com/I1Igl4u.png =300x)
    - 則在Ax中，第i個entry為：
         ![](https://i.imgur.com/b0FhUgt.png =240x)
    - 同時也是 row向量 A 與 column向量 x 的乘積
     ![](https://i.imgur.com/rl7AoOZ.png =100x)
    - Ex:![](https://i.imgur.com/hnZzUnr.png =200x)![](https://i.imgur.com/Vxg5fya.png =200x)
- Linear combination
    - 定義：若在$R^n$有向量$a_1,a_2,...a_n$和純量$c_1,c_2,...c_n$，則sum = $c_1a_1+c_2a_2+...+c_na_n$
    - 也稱為是向量$a_1,a_2,...a_n$的linear combination(線性組合)
    - Ax是column vector跟A的線性組合:$Ax=x_1a_1+x_2a_2+...+x_na_n$
    - 若Ａ是一個Ｍ*Ｎ矩陣以及x是$R^n$的一個向量，則$Ax=x_1a_1+x_2a_2+...+x_na_n$
### Theorem 1.3.1 :Consistency Theorem for Linear Systems
- 一線性系統Ax=b是consistent iff b，可寫為是A的column vector線性組合
- Ex:![](https://i.imgur.com/MU5sq1b.png =100x)
![](https://i.imgur.com/WPjIdKu.png =250x)
### Matrix Multiplication 
- 若矩陣Ａ的column數量 ＝ Ｂ的row的數量，則Ａ、Ｂ可相乘
- Product $AB=A(b_1,b_2,...,b_n)=(Ab_1,Ab_2,...,Ab_n)$
- 定義：若$A=(a_{ij})$為m*n矩陣，$B=(b_{ij})$為n\*r矩陣
     ，Product $AB=C=(c_{ij})$為m\*r矩陣
     ![](https://i.imgur.com/pfvahkA.png =170x)
- Ex:![](https://i.imgur.com/sVqKZYn.png =250x)![](https://i.imgur.com/FSG3orB.png =270x)
- 矩陣乘法不遵守交換律(commutative)：==$AB\neq BA$==
### The Transpose of a Matrix（轉置矩陣）
- 定義：m\*n矩陣Ａ以及n\*m矩陣Ｂ的關係為
  $b_{ji}=a_{ij},for\ j=1,...,n$& $i=1,...,m$
  Transpose A表示為$A^T$
- Ex:![](https://i.imgur.com/O9v8Vok.png =250x)![](https://i.imgur.com/HvXFVJK.png =250x)
### Symmetric 對稱
- $n*n$ 矩陣$A$ , $A^T=A$
##  1.4 Matrix Algebra Algebraic Rules Theorem 1.4.1
- 有matrices $A,B\ and\ C$，scalars $\alpha , \beta$:
    -  $A+B=B+A$
    -  $(A+B)+C=A+(B+C)$
    -  $(AB)C = A(BC)$
    -  $A(B + C) = AB + AC$
    -  $(A + B)C = AC + BC$
    -  $(αβ)A = α(βA)$
    -  $α(AB)=(αA)B=A(αB)$
    -  $(α + β)A = αA + βA$
    -  $α(A+B) = αA + αB$
###  The Identity Matrix
- identity matrix $I$與$n*n$矩陣Ａ做乘法：$IA=AI=A$
- $I=\left[\begin{array}{ccc} 1 & 0 & 0 \\0 & 1 & 0\\ 0 & 0 & 1 \\ \end{array}\right]$ is a 3*3 identity matrix 
- identity 與任一矩陣Ａ相乘，結果還是Ａ
### Matrix Inversion
- 定義：如果存在一個滿足 $AB = BA = I$的矩陣 B，則稱一個 n*n 矩陣 A 是nonsingular(非奇異的)或invertible(可逆的)。矩陣 B 稱為 A 的multiplicative inverse
- 對一實數a，若存在b使得ab=1，則稱a有multiplicative inverse
- 任一非零數a有一multiplicative inverse $b=\frac{1}{a}$
- 若B和C都是A的multiplicative inverse$(BA = AB = I\ and\ CA = AC = I)$，則：$B = BI = B(AC) = (BA)C = IC = C$
- 一矩陣++最多只有一個++multiplicative inverse
- The inverse of A 寫為 $A^{-1}$
- EX:$A=\left[\begin{array}{cc} 2 & 4  \\3 & 1 \\  \end{array}\right]$ and $B=\left[\begin{array}{cc} -\frac{1}{10} & \frac{2}{5}  \\\frac{3}{10} & -\frac{1}{5} \\  \end{array}\right]$為彼此的inverse,則![](https://i.imgur.com/hkC7L94.png =210x)and![](https://i.imgur.com/PhmMXTq.png =210x)
  Hint:相乘為identity
- Ex:$A=\left[\begin{array}{cc} 1 & 0  \\0 & 0 \\  \end{array}\right]$沒有inverse
    設![](https://i.imgur.com/CGLhkdo.png =140x)，則![](https://i.imgur.com/fjDEW2V.png =280x)
- 若n*n矩陣沒有multiplicative inverse，可稱為singular
### Theorem 1.4.2
- 若矩陣$Ａ$、$Ｂ$都是nonsingular(可逆的)，則$AB$也會是nonsingular，以及 ==$AB^{-1}=B^{-1}A^{-1}$==
- 若 $A_1A_2...A_k$ 都是可逆的n*n矩陣，則：$(A_1A_2...A_k)^{-1}=A_k^{-1}...A_2^{-1}A_1^{-1}$
### The Transpose of Matrix
- 規則：
    - $(A^T)^T=A$
    - $(\alpha A)^T=A^T+B^T$
    - $(A+B)^T=A^T+B^T$
    - $(AB)^T=B^TA^T$
- EX:![](https://i.imgur.com/uVDp30a.png =220x)
    - ![](https://i.imgur.com/udJ5zAH.png =280x)
    - ![](https://i.imgur.com/WWxc4mq.png =140x)
    - ![](https://i.imgur.com/WFytYhn.png =300x)
### Symmetric Matrices and Networks
- 一矩陣Ａ，若$A^T=A$，則稱Ａ是symmetric(對稱的)
- 一種解決此問題的方法與networks相關，call $graph\ theory$
### Theorem 1.4.3 
- 如果A是一個graph的 n*n adjacency matrix並由$a_{ij}^{(k)}$表示 $A^k$的 $(i, j)$項，則 $a_{ij}^{(k)}=$從 $Vi$ 到 $Vj$ 的$length\ k$的步行次數。
## 1.5 Elementary Matrices Equivalent Systems
- 給定一m*n線性系統$Ax=b$，兩邊同乘一nonsingular m\*m 矩陣Ｍ：$MAx=Mb$
- 若 $\hat{x}$ 是 $MAx=Mb$ 的解，則
    - $MA\hat{x}=Mb$
    - $M^{-1}(MA\hat{x})=M^{-1}(Mb$)
    - $A\hat{x}=b$
- 同時 $\hat{x}$ 也是 $Ax=b$ 的解
- --->$Ax=b$ 跟 $MAx=Mb$ 是 ++equivalent++
### Elementary Matrices
- 對identity matrix $I$進行一次基本行運算得到的矩陣稱為elementary matrix(基本矩陣)。
    - $Type\ I$:是通過交換兩個row得到的矩陣。
        - EX:![](https://i.imgur.com/NWOK5OE.png =100x)
        ![](https://i.imgur.com/scRBvL6.png =360x)![](https://i.imgur.com/6SbWdR9.png =360x)
    - $Type\ II$:將$I$的row乘以一非零常數
    - $Type\ III$:是通過將一row的倍數與另一行相加從$I$獲得的矩陣
        - Ex:![](https://i.imgur.com/25zTVPD.png =100x)
        ![](https://i.imgur.com/NXhmZFE.png =400x)
        ![](https://i.imgur.com/c1wNNkY.png =360x)
- If A is an n × r matrix, premultiplying A by E has the effect of performing that same row operation on A.
- If B is an m × n matrix, postmultiplying B by E is equivalent to performing that same column operation on B.
### Theorem 1.5.1
- 若 $E$ 為一elementary matrix，且 $E$ 為nonsingular、$E^{-1}$ 也是同類型的elementary matrix
- 證明：
    - $Type\ I$:
        - $EE=I\ =>\ E^{-1}=E$
    - $Type\ II$:
        - ![](https://i.imgur.com/q9fLEiX.png =250x)，![](https://i.imgur.com/IKImk3P.png =250x)
    - $Type\ III$:
        - ![](https://i.imgur.com/Zm1eAzP.png =250x)，![](https://i.imgur.com/3iKbyly.png =270x)
### Theorem 1.5.2 Equivalent Conditions for Nonsingularity
- A是一個m*n矩陣，以下為equivalent:
    - A是nonsingular
    - $Ax=0$ 有trivial solution ０
    - A is row equivalent to $I$
### Corollary 1.5.3
- n 個未知數中，n 個線性方程組$Ax=b$ ，當$A$是nonsingular，有唯一解
    - 證明：若Ａ是nonsingular，$\hat{x}$是$Ax=b$的解
      則$A\hat{x}=b$
      $=>A^{-1}(A\hat{x})=A^{-1}b$
      所以，$\hat{x}=A^{-1}b$
      ![](https://i.imgur.com/Vm6JNlt.png =400x)
- 如果 A 是nonsingular，Arow equivalent to $I$，所以存在初等矩陣 $E_1, E_2, ..., E_k$ 使得
![](https://i.imgur.com/HO7tM2U.png)
- 將nonsingular matrix A 轉換為 $I$ 的同一系列基本行操作會將 I 轉換為$A^{-1}$。 也就是說，增廣矩陣 $(A | I)$ 的RREF(簡化行梯形形式)將是 $(I | A^{–1})$。    
    - EX：Compute $A^{-1}$ if ![](https://i.imgur.com/WxFVREi.png =130x)
      - ![](https://i.imgur.com/FSfRblx.png)  ，  ![](https://i.imgur.com/2U9fsZH.png)
    - EX：Solve the system:
        $x_1+4x_2+3x_3\ \ =12$
        $-x_1-2x_2\ \ \ \ \ \ \ \ \ \ =-12$
        $2x_1+2x_2+3x_3\ =8$
###  Diagonal and Triangular Matrices
- 一n*n 矩陣Ａ，若$a_{ij}=0\ for\ i>j$ 為 **upper triangular**（上三角）
    - e.g.,![](https://i.imgur.com/if6E9gD.png =80x)
- 一n*n 矩陣Ａ，若$a_{ij}=0\ for\ i<j$ 為 **lower triangular**（下三角）
    - e.g.,![](https://i.imgur.com/V7bKIR8.png =80x)
- upper / lower triangular $=>$triangular
- 一n*n 矩陣Ａ，若$a_{ij}=0\ whenever\ i\neq j$ 為 **diagnal**
    - e.g.,![](https://i.imgur.com/VLbirQM.png)
- **diagonal 同時是 upper triangular 和 lower triangular**
###  Triangular Factorization
- 如果僅用 row operation $III$可以將 n×n 矩陣 A 簡化為嚴格的上三角形式，則可以用matrix factorization（矩陣分解）來表示簡化過程。
- EX:
  ![](https://i.imgur.com/sGeQUWj.png)
        ![](https://i.imgur.com/vhmYUI0.png)  ($=>unit $lower\ triangular$)
    ![](https://i.imgur.com/4id0Pm9.png)
    - 將矩陣 A 分解為 unit lower triangular 矩陣 L 乘以 strictly upper triangular 矩陣 U 的乘積通常稱為 $LU\ factorization$(LU 分解)。
    - Why LU factorization works?
    - Since $E_3E_2E_1A=U$,where
    - ![](https://i.imgur.com/XRwMBqK.png =350x)          $=>A=E_1^{-1}E_2^{-1}E_3^{-1}U$![](https://i.imgur.com/esU0IxR.png =400x)$=L$
## 1.6 Partitioned Matrices
- 矩陣可以劃分為小的submatrices(子矩陣)（稱為**block**）
    - e.g.,![](https://i.imgur.com/KuTKoVh.png =360x)
- 如果 A 是 m * n 矩陣，B 是 n * r，它已被劃分為columns $(b_1, b_2, ..., b_r)$，則 A 乘 B 的block multiplication:$AB = A (b_1, b_2, ..., b_r) = (Ab_1, Ab_2, . . ., Ab_r)$
- In particular,$(a_1, a_2, ..., a_n) = A = AI = (Ae_1, Ae_2, ..., Ae_n)$
    - Ex:![](https://i.imgur.com/K00ANTc.png)![](https://i.imgur.com/oKROqPY.png)
      hence, ![](https://i.imgur.com/jwezYTf.png)
    - Ex:![](https://i.imgur.com/HjtXZ35.png)![](https://i.imgur.com/kyrKnky.png)![](https://i.imgur.com/LmLPmNs.png)
### Block Multiplication
- 如果 A 是 m * n 矩陣，B 是 n * r 矩陣，考慮下面4種cases:
    - $Case\ 1$
        - $B=(B_1,B_2)$,$B_1$為 n * t 矩陣,$B_2$為  n*(r-t)矩陣
        - 則：$AB=A(b_1,...,b_t,b_{t+1},...,b_r)=(Ab_1,...,Ab_t,Ab_{t+1},...,Ab_r)=(A(b_1,...,b_t),A(b_{t+1},...,b_r))=(AB_1,AB_2)$
        - Thus, **$A(B_1,B_2)=(AB_1,AB_2)$**
    - $Case\ 2$
        - $A=\begin{bmatrix}A_1\\A_2\end{bmatrix}$, $A_1$為一 k*n 矩陣, $A_2$為一 (m-k)*n 矩陣
        - ![](https://i.imgur.com/cKQmSOo.png)
        - Thus, ![](https://i.imgur.com/ZvcLTJU.png)
    - $Case\ 3$
        - $A=[A_1,A_2]$, $B=\begin{bmatrix}B_1\\B_2\end{bmatrix}$, $A_1$為一 m*s 矩陣, $A_2$為一 m*(n-s) 矩陣, $B_1$為一 s*r 矩陣, $B_2$為一 (n-s)*r 矩陣, 若$C=AB$,則![](https://i.imgur.com/kqt6jpi.png =280x)
        - Thus, $c_{ij}$ 為$A_1B_1$跟$A_2B_2$中$(i,j)$的和，因此![](https://i.imgur.com/8Xp08Uj.png =260x)
    - $Case\ 4$
        - Let $A$ and $B$ 被分割成：![](https://i.imgur.com/DEahBzW.png =300x)
        - Let ![](https://i.imgur.com/XCL6Ewn.png =400x)
        - 則：![](https://i.imgur.com/XQi7HoW.png =260x)
        - And, ![](https://i.imgur.com/fWqLNnb.png =430x)![](https://i.imgur.com/1NALDhn.png =420x)
        - 因此，![](https://i.imgur.com/EAPcaTq.png =420x)
- 綜上所述，如果block具有適當的dimensions，則block multiplication可以以與普通矩陣乘法相同的方式進行
    - ![](https://i.imgur.com/qNlek4V.png =340x)![](https://i.imgur.com/LGk2Jge.png =250x)![](https://i.imgur.com/1HSZlkN.png =200x)
###  Outer Product Expansions
- 給定 $R^n$ 中的兩個向量 $x$ 和 $y$，scalar product或inner product(內積)定義為matrix product $x^Ty$，即row vector（1 × n 矩陣）乘以column vector（n × 1 矩陣）的乘積 並產生一個 1 × 1 矩陣或簡單的scalar
    - ![](https://i.imgur.com/iqXc36E.png =400x)
- outer product(外積)定義：matrix product $xy^T$，它是 n×1 矩陣乘以 1×n 矩陣的乘積，得到一個 n × n 矩陣：
    - ![](https://i.imgur.com/zMHGDdU.png =360x)
- EX:
    - ![](https://i.imgur.com/7g2hlxf.png =160x)![](https://i.imgur.com/5y8A6X0.png =300x)
- 設$X$為m\*n矩陣，$Y$為k*n矩陣，X與Y的outer product expansion(外積展開)為matrix product$XY^T$。 $XY^T$ 可以通過將 X 劃分為columns和 $Y^T$ 劃分為rows來計算，然後執行block multiplication：
    ![](https://i.imgur.com/5c41CAI.png =450x)
- Ex:
    - 給定![](https://i.imgur.com/6VKmMQA.png =200x)![](https://i.imgur.com/hcXEZUX.png =400x)![](https://i.imgur.com/oLyI49g.png =190x)
## 2.1 The Determinant of a Matrix
- n*n 矩陣 $A$ 的行列式 $det(A)$ 將告訴我們矩陣是否是nonsingular的（它的逆矩陣是否存在）。
- $Case\ 1$
    - 如果 $A = [a]$ 是一個 1*1 矩陣，那麼 A 將有一個multiplicative inverse iff a ≠ 0（即 det(A) ≠ 0）
    - 定義$det(A)=a$
    - $det(A)\neq0=>$$A$是nonsingular
- $Case\ 2$
    - 設$A=\begin{bmatrix} a_{11} & a_{12} \\ a_{21} & a_{22}\end{bmatrix}$，由Theorem 1.5.2,若$A$  row equivalent to $I$, 則$A$是nonsingular
    1. 若$a_{11}\neq0$![](https://i.imgur.com/EEvu8gO.png)$A$ is row equivalent to $I$ iff ==$a_{11}a_{22}-a_{21}a_{12}\neq0$==
    2. 若$a_{11}=0$
        ![](https://i.imgur.com/VH1TAiA.png =120x)
        交換$A$的兩個row，我們得到$A'$ is row equivalent to $I$ iff $a_{21}a_{12}\neq0$  ($a_{21}\neq0$ and $a_{12}\neq0$)
        定義：==$det(A)=a_{11}a_{22}-a_{21}a_{22}$==
- $Case\ 3$ - 3*3 Matrices
        $A=\begin{bmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23}\\ a_{31}  & a_{32} & a_{33}\end{bmatrix}$
    - 若$a_{11}\neq0$
        - $\begin{bmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23}\\ a_{31}  & a_{32} & a_{33}\end{bmatrix}=>\begin{bmatrix} a_{11} & a_{12} & a_{13} \\ 0 & \frac{a_{11}a_{22}-a_{21}a_{12}}{a_{11}} & \frac{a_{11}a_{22}-a_{21}a_{12}}{a_{11}}\\ 0  & \frac{a_{11}a_{32}-a_{31}a_{12}}{a_{11}} & \frac{a_{11}a_{33}-a_{31}a_{13}}{a_{11}}\end{bmatrix}$
        - iff ![](https://i.imgur.com/6rMbPMR.png =290x)$=>a_{11}a_{22}a_{33} – a_{11}a_{23}a_{32} – a_{12}a_{21}a_{33}+ a_{12}a_{23}a_{31} + a_{13}a_{21}a_{32} – a_{13}a_{22}a_{31} ≠ 0$
        - $det(A)=a_{11}a_{22}a_{33} – a_{11}a_{23}a_{31} – a_{13}a_{21}a_{32}+ a_{12}a_{21}a_{33} + a_{13}a_{22}a_{31} – a_{13}a_{22}a_{31}$$=a_{11}(a_{22}a_{33}-a_{32}a_{23})-a_{12}(a_{21}a_{33}-a_{31}a_{23})+a_{13}(a_{21}a_{32}-a_{31}a_{22})$==$=a_{11}det(M_{11})-a_{12}det(M_{12})+a_{13}det(M_{13})$==
          where, $M_{11}=\begin{bmatrix} a_{22} & a_{23} \\ a_{32}  & a_{33} \end{bmatrix}$, $M_{12}=\begin{bmatrix} a_{21} & a_{23} \\ a_{31}  & a_{33} \end{bmatrix}$, $M_{13}=\begin{bmatrix} a_{21} & a_{22} \\ a_{31}  & a_{32} \end{bmatrix}$
### cofactor
- 令 $A = (a_{ij})$ 是一個 n * n 矩陣。 令$M_{ij}$ 為從$A$ 中刪除包含$a_{ij}$ 的行和列得到的(n – 1) × (n – 1) 矩陣。 $M_{ij}$ 的行列式稱為 $a_{ij}$ 的 minor。 我們定義 $a_{ij}$ 的 cofactor $A_{ij}$ 為 ==$A_{ij}=(-1)^{i+j}det(M_{ij})$==
- EX:
    - $A=\begin{bmatrix} a_{11} & a_{12} \\ a_{21}  & a_{22} \end{bmatrix}$
    - $det(A)=a_{11}(a_{22})-a_{12}(a_{21})=a_{11}A_{11}+a_{12}A_{12}\ \ (n=2)$
        - 該方程稱為 $det(A)$ 沿 $A$ 的 first row 的 cofactor expansion
    - $det(A)$
      $=a_{11}(a_{22})-a_{21}(a_{12})$
      $=a_{21}(-a_{12})+a_{22}(a_{11})$
      $=a_{21}A_{21}+a_{22}A_{22}$ --->(2nd row)
      $=a_{11}(a_{22})+a_{21}(-a_{12})$
      $=a_{11}A_{11}+a_{21}A_{21}$--->(1st column)
      $=a_{12}(-a_{21})+a_{22}(a_{11})$
      $=a_{12}A_{12}+a_{22}A_{22}$--->(2nd column)
- EX:
    - if $A=\begin{bmatrix} 3 & 5&4 \\ 3  & 1&2\\ 5&4&6 \end{bmatrix}$
    - $det(A)=a_{11}A_{11}+a_{12}A_{12}+a_{13}A_{13}$
      $=$![](https://i.imgur.com/h3FZjYt.png =200x)
      $=(-4)-5(8)+4(7)=-16$
### determinant, scalar
- n * n 矩陣 A 的行列式，表示為 det(A)，是與矩陣 A 關聯的scalar，其歸納定義如下：![](https://i.imgur.com/7fxZ2SN.png =360x)
  where,$A_{1j} = (–1)^{1+j} det(M_{1j}),\ j=1,2,...,n$ 是與 A 的first row中關聯的cofactors
### Theorem 2.1.1
- 如果 A 是 n*n 矩陣(n≥2)，則 det(A) 可以表示為 A 的任何row或column的cofactor expansion
- $det(A)=a_{i1}A_{i1}+a_{i2}A_{i2}+...+a_{in}A_{in} = a_{1j}A_{1j}+a_{2j}A_{2j}+...+a_{nj}A_{nj}$
  for $i,j=1,2,...,n$
- 可以沿著包含最多零的行或列執行cofactor expansion
    - Ex:
        - ![](https://i.imgur.com/KaXaoin.png =130x),![](https://i.imgur.com/Z1uVIAQ.png =420x)$=(-2)3(-2)=12$
### Theorem 2.1.2
- 如果 A 是 n*n 矩陣，則 $det(A^T) = det(A)$
- Ex:
    - ![](https://i.imgur.com/TLE4MTZ.png =300x)
### Theorem 2.1.3
- 如果 A 是 n*n triangular matrix(三角矩陣)，則 $det(A) = A$ 的對角線元素的乘積。
- Ex:
    - ![](https://i.imgur.com/0YSJ9mg.png =120x)
### Theorem 2.1.4
- 令 A 為 n*n 矩陣。
    - (i) 如果 A 有一行或一列完全為零，則 det(A) = 0
    - (ii) 如果 A 有兩個相同的行或兩個相同的列，則 det(A) = 0
- Ex:
    - ![](https://i.imgur.com/ml8IJKX.png =100x) , ![](https://i.imgur.com/XxZ3Ca0.png =360x)
:::info
以上為期中考範圍
:::









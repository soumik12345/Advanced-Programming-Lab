
```
Q1. Create a matrix taking a vector of numbers as input:
    c(3:14), nrows = 4
    
    Perform the following operations:
    1. elements are arranged sequentiallyby row
    2. elements are arranged sequentiallyby column
    3. define column and row names
    4. access the element at 3rd column and 1st row
    5. access the element at 2nd column and 4th row
    6. access only 2nd row
    7. access only 3rd column


Q2. Create two 2x3 matrices and perform the following operations:
    1. Add the matrices
    2. Subtract the matrices
    3. Multiply the matrices
    4. Divide the matrices
```


```R
# 1.1
x = matrix(c(3 : 14), nrow = 4, byrow = TRUE)
x
```


<table>
<tbody>
	<tr><td> 3</td><td> 4</td><td> 5</td></tr>
	<tr><td> 6</td><td> 7</td><td> 8</td></tr>
	<tr><td> 9</td><td>10</td><td>11</td></tr>
	<tr><td>12</td><td>13</td><td>14</td></tr>
</tbody>
</table>




```R
# 1.2
x = matrix(c(3 : 14), nrow = 4, byrow = FALSE)
x
```


<table>
<tbody>
	<tr><td>3 </td><td> 7</td><td>11</td></tr>
	<tr><td>4 </td><td> 8</td><td>12</td></tr>
	<tr><td>5 </td><td> 9</td><td>13</td></tr>
	<tr><td>6 </td><td>10</td><td>14</td></tr>
</tbody>
</table>




```R
# 1.3
rownames(x) = c("row1", "row2", "row3", "row4")
colnames(x) = c("col1", "col2", "col3")
x
```


<table>
<thead><tr><th></th><th scope=col>col1</th><th scope=col>col2</th><th scope=col>col3</th></tr></thead>
<tbody>
	<tr><th scope=row>row1</th><td>3 </td><td> 7</td><td>11</td></tr>
	<tr><th scope=row>row2</th><td>4 </td><td> 8</td><td>12</td></tr>
	<tr><th scope=row>row3</th><td>5 </td><td> 9</td><td>13</td></tr>
	<tr><th scope=row>row4</th><td>6 </td><td>10</td><td>14</td></tr>
</tbody>
</table>




```R
# 1.4
x[1, 3]
```


11



```R
# 1.5
x[4, 2]
```


10



```R
# 1.6
x[2,]
```


<dl class=dl-horizontal>
	<dt>col1</dt>
		<dd>4</dd>
	<dt>col2</dt>
		<dd>8</dd>
	<dt>col3</dt>
		<dd>12</dd>
</dl>




```R
# 1.7
x[,3]
```


<dl class=dl-horizontal>
	<dt>row1</dt>
		<dd>11</dd>
	<dt>row2</dt>
		<dd>12</dd>
	<dt>row3</dt>
		<dd>13</dd>
	<dt>row4</dt>
		<dd>14</dd>
</dl>




```R
# 2
a = matrix(c(1 : 6), nrow = 2, byrow = TRUE)
b = matrix(c(6 : 11), nrow = 2, byrow = TRUE)
```


```R
a
```


<table>
<tbody>
	<tr><td>1</td><td>2</td><td>3</td></tr>
	<tr><td>4</td><td>5</td><td>6</td></tr>
</tbody>
</table>




```R
b
```


<table>
<tbody>
	<tr><td>6 </td><td> 7</td><td> 8</td></tr>
	<tr><td>9 </td><td>10</td><td>11</td></tr>
</tbody>
</table>




```R
# 2.1
a + b
```


<table>
<tbody>
	<tr><td> 7</td><td> 9</td><td>11</td></tr>
	<tr><td>13</td><td>15</td><td>17</td></tr>
</tbody>
</table>




```R
# 2.2
a - b
```


<table>
<tbody>
	<tr><td>-5</td><td>-5</td><td>-5</td></tr>
	<tr><td>-5</td><td>-5</td><td>-5</td></tr>
</tbody>
</table>




```R
# 2.3
# a %*% t(b)
a * b
```


<table>
<tbody>
	<tr><td> 6</td><td>14</td><td>24</td></tr>
	<tr><td>36</td><td>50</td><td>66</td></tr>
</tbody>
</table>




```R
# 2.4
a / b
```


<table>
<tbody>
	<tr><td>0.1666667</td><td>0.2857143</td><td>0.3750000</td></tr>
	<tr><td>0.4444444</td><td>0.5000000</td><td>0.5454545</td></tr>
</tbody>
</table>




```R

```

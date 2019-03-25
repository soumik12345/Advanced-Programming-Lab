
## List Examples


```R
list_data = list("Red", "Green", c(21, 32, 11), TRUE, 51.23, 119.1)
list_data
```


<ol>
	<li>'Red'</li>
	<li>'Green'</li>
	<li><ol class=list-inline>
	<li>21</li>
	<li>32</li>
	<li>11</li>
</ol>
</li>
	<li>TRUE</li>
	<li>51.23</li>
	<li>119.1</li>
</ol>




```R
list_data = list(c("Jan", "Feb", "March"), matrix(c(3, 9, 5, 1, -2, 8), nrow = 2), list("green", 1, 2, 4))
list_data
```


<ol>
	<li><ol class=list-inline>
	<li>'Jan'</li>
	<li>'Feb'</li>
	<li>'March'</li>
</ol>
</li>
	<li><table>
<tbody>
	<tr><td>3 </td><td>5 </td><td>-2</td></tr>
	<tr><td>9 </td><td>1 </td><td> 8</td></tr>
</tbody>
</table>
</li>
	<li><ol>
	<li>'green'</li>
	<li>1</li>
	<li>2</li>
	<li>4</li>
</ol>
</li>
</ol>




```R
list_data[1]
```


<ol>
	<li><ol class=list-inline>
	<li>'Jan'</li>
	<li>'Feb'</li>
	<li>'March'</li>
</ol>
</li>
</ol>




```R
list_data[4] = "New Element"
list_data
```


<ol>
	<li><ol class=list-inline>
	<li>'Jan'</li>
	<li>'Feb'</li>
	<li>'March'</li>
</ol>
</li>
	<li><table>
<tbody>
	<tr><td>3 </td><td>5 </td><td>-2</td></tr>
	<tr><td>9 </td><td>1 </td><td> 8</td></tr>
</tbody>
</table>
</li>
	<li><ol>
	<li>'green'</li>
	<li>1</li>
	<li>2</li>
	<li>4</li>
</ol>
</li>
	<li>'New Element'</li>
</ol>




```R
list_data[4] = NULL
list_data
```


<ol>
	<li><ol class=list-inline>
	<li>'Jan'</li>
	<li>'Feb'</li>
	<li>'March'</li>
</ol>
</li>
	<li><table>
<tbody>
	<tr><td>3 </td><td>5 </td><td>-2</td></tr>
	<tr><td>9 </td><td>1 </td><td> 8</td></tr>
</tbody>
</table>
</li>
	<li><ol>
	<li>'green'</li>
	<li>1</li>
	<li>2</li>
	<li>4</li>
</ol>
</li>
</ol>




```R
list_1 = list(1, 2, 3)
list_2 = list("Sun", "Mon", "Tue")

merged_list = c(list_1, list_2)
merged_list
```


<ol>
	<li>1</li>
	<li>2</li>
	<li>3</li>
	<li>'Sun'</li>
	<li>'Mon'</li>
	<li>'Tue'</li>
</ol>




```R
list_3 = list(1 : 5)
vec_3 = unlist(list_3)
vec_3
```


<ol class=list-inline>
	<li>1</li>
	<li>2</li>
	<li>3</li>
	<li>4</li>
	<li>5</li>
</ol>



## Arrays


```R
vec_1 = c(5, 9, 3)
vec_2 = c(10, 11, 12, 13, 14, 15)
result = array(c(vec_1, vec_2), dim = c(3, 3, 2))
result
```


<ol class=list-inline>
	<li>5</li>
	<li>9</li>
	<li>3</li>
	<li>10</li>
	<li>11</li>
	<li>12</li>
	<li>13</li>
	<li>14</li>
	<li>15</li>
	<li>5</li>
	<li>9</li>
	<li>3</li>
	<li>10</li>
	<li>11</li>
	<li>12</li>
	<li>13</li>
	<li>14</li>
	<li>15</li>
</ol>




```R
vec_1 = c(5, 9, 3)
vec_2 = c(10, 11, 12, 13, 14, 15)
col_names = c("Col1", "Col2", "Col3")
row_names = c("Row1", "Row2", "Row3")
mat_names = c("Mat1", "Mat2")


```


```R
# Third row of second matrix
result[3, , 2]
```


<ol class=list-inline>
	<li>3</li>
	<li>12</li>
	<li>15</li>
</ol>




```R
# element in 1st row and 3rd col of 1st matrix
result[1, 3, 1]
```


13



```R
# Create 2 vectors of different lengths and take theses vectors as input to the array
vec_1 = c(5, 9, 3)
vec_2 = c(10, 11, 12, 13, 14, 15)
vec_3 = c(9, 1, 0)
vec_4 = c(6, 0, 11, 3, 14, 1, 2, 6, 9)
array_1 = array(c(vec_1, vec_2), dim = c(3, 3, 2))
array_2 = array(c(vec_3, vec_4), dim = c(3, 3, 2))
```


```R
array_1
```


<ol class=list-inline>
	<li>5</li>
	<li>9</li>
	<li>3</li>
	<li>10</li>
	<li>11</li>
	<li>12</li>
	<li>13</li>
	<li>14</li>
	<li>15</li>
	<li>5</li>
	<li>9</li>
	<li>3</li>
	<li>10</li>
	<li>11</li>
	<li>12</li>
	<li>13</li>
	<li>14</li>
	<li>15</li>
</ol>




```R
array_2
```


<ol class=list-inline>
	<li>9</li>
	<li>1</li>
	<li>0</li>
	<li>6</li>
	<li>0</li>
	<li>11</li>
	<li>3</li>
	<li>14</li>
	<li>1</li>
	<li>2</li>
	<li>6</li>
	<li>9</li>
	<li>9</li>
	<li>1</li>
	<li>0</li>
	<li>6</li>
	<li>0</li>
	<li>11</li>
</ol>




```R
result = apply(array_1, c(1), sum)
result
```


<ol class=list-inline>
	<li>56</li>
	<li>68</li>
	<li>60</li>
</ol>



## Data Frames


```R
BMI = data.frame(gender = c("Male", "Male", "Female"),
                 height = c(152, 171.5, 165),
                 weight = c(81, 98, 78),
                 age = c(42, 38, 26))
BMI
```


<table>
<thead><tr><th scope=col>gender</th><th scope=col>height</th><th scope=col>weight</th><th scope=col>age</th></tr></thead>
<tbody>
	<tr><td>Male  </td><td>152.0 </td><td>81    </td><td>42    </td></tr>
	<tr><td>Male  </td><td>171.5 </td><td>98    </td><td>38    </td></tr>
	<tr><td>Female</td><td>165.0 </td><td>78    </td><td>26    </td></tr>
</tbody>
</table>




```R
BMI["age"]
```


<table>
<thead><tr><th scope=col>age</th></tr></thead>
<tbody>
	<tr><td>42</td></tr>
	<tr><td>38</td></tr>
	<tr><td>26</td></tr>
</tbody>
</table>




```R
BMI[, "gender"]
```


<ol class=list-inline>
	<li>Male</li>
	<li>Male</li>
	<li>Female</li>
</ol>




```R
BMI[, 2]
```


<ol class=list-inline>
	<li>152</li>
	<li>171.5</li>
	<li>165</li>
</ol>




```R
BMI["gender" == "Male"]
```






```R

```

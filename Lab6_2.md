
### Questions

```
1. Write an R-script to create a list with different data types of data set. Now display each data set
   seperately according to the data type

2. Write an R-script to create a list having vector, matrix and a list. Now display only the second data
   set of the list.

3. Write an R-script to add a new data set to the previous list and also remove the 2nd data set from the
   list.

4. Write an R-script to create two lists: one containing integers from 1 to 5 another containing names of
   5 months. Now merge the 2 lists and display the merged list.
   
5. Create a data frame to specify data on students given below:
   Roll, Name, Department, Course, Year of Joining
   - Write a function to print names of all students who joined in a particular year.
   - Write a function to print name of student with given roll.

6. Write an R-script to create an array having 3 dimensions. Now retrieve the elements of 2nd row and 3rd
   matrix.

7. Write an R-script to create an array having 3 dimensions. Now calculate the sum of the rows accross
   the matrix.
```


```R
# Q1
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
# Q2
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
# Q3
list_data = list("Red", "Green", c(21, 32, 11), TRUE, 51.23, 119.1)
list_data[7] = "New Element"
list_data[2] = NULL
list_data
```


<ol>
	<li>'Red'</li>
	<li><ol class=list-inline>
	<li>21</li>
	<li>32</li>
	<li>11</li>
</ol>
</li>
	<li>TRUE</li>
	<li>51.23</li>
	<li>119.1</li>
	<li>'New Element'</li>
</ol>




```R
# Q4
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
# Q5
data_frame = data.frame(roll = c(1605234, 1605235, 1605236),
                        name = c("Tousif", "Soumik", "Soumyadip"),
                        gender = c("Male", "Male", "Payra"),
                        department = c("CSE", "ETC", "MCH"),
                        course = c("APLAB", "CDLAB", "CGLAB"),
                        year_of_joining = c(2016, 2017, 2018))
data_frame
```


<table>
<thead><tr><th scope=col>roll</th><th scope=col>name</th><th scope=col>gender</th><th scope=col>department</th><th scope=col>course</th><th scope=col>year_of_joining</th></tr></thead>
<tbody>
	<tr><td>1605234  </td><td>Tousif   </td><td>Male     </td><td>CSE      </td><td>APLAB    </td><td>2016     </td></tr>
	<tr><td>1605235  </td><td>Soumik   </td><td>Male     </td><td>ETC      </td><td>CDLAB    </td><td>2017     </td></tr>
	<tr><td>1605236  </td><td>Soumyadip</td><td>Payra    </td><td>MCH      </td><td>CGLAB    </td><td>2018     </td></tr>
</tbody>
</table>




```R
func_1 <- function(data_frame, year) {
    frame = subset(data_frame, year_of_joining == year)
    return (frame['name'])
}

func_1(data_frame, 2016)
```


<table>
<thead><tr><th scope=col>name</th></tr></thead>
<tbody>
	<tr><td>Tousif</td></tr>
</tbody>
</table>




```R
func_2 <- function(data_frame, given_roll) {
    frame = subset(data_frame, roll == given_roll)
    return (frame["name"])
}

func_1(data_frame, 1605234)
```


<table>
<thead><tr><th scope=col>name</th></tr></thead>
<tbody>
</tbody>
</table>




```R
# Q6
vec_1 = c(5, 9, 3)
vec_2 = c(10, 11, 12, 13, 14, 15)
array_1 = array(c(vec_1, vec_2), dim = c(3, 3, 3))
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
# Q7
vec_1 = c(5, 9, 3)
vec_2 = c(10, 11, 12, 13, 14, 15)
array_2 = array(c(vec_1, vec_2), dim = c(3, 3, 3))
rowSums(array_2)
```


<ol class=list-inline>
	<li>84</li>
	<li>102</li>
	<li>90</li>
</ol>



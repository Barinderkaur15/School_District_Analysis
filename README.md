# School_District_Analysis
Analysis using Anaconda and Jupyter
As per the direction provided by the  authority , the grades of the ninth graders at  Thomas High School for math and reading have been changed and replaced by NAN( Not a Number ) . We use NAN method to mask the grades from the calculation . 
Adding NAN TO the Data set has affected analysis the following way : 


A total of 461 rows were affected and values for these entries under reading and math were changed to NAN 


######•	** How is the district summary affected? **
When the scores  were present in data set  we were getting the following result :
Total Schools	Total Students	Total Budget	Average Math Score	Average Reading Score	% Passing Math	% Passing Reading	% Overall Passing
0	15	39170	24649428	78.985371	81.87784	74.980853	85.805463	80.393158
After  masking  : 
	Total Schools	Total Students	Total Budget	Average Math Score	Average Reading Score	% Passing Math	% Passing Reading	% Overall Passing
0	15	39170	24649428	78.930533	81.855796	73.880521	84.651519	79.26602

As seen above the result changes like 0.03 for math and 0.20 for reading , which is so small that once we format our result the number were rounded to the same digits .


•	### How is the school summary affected?
The school summary is based on Per school performance ,  to calculate this we use group function which divides the dataset based on preschool , performs the function and regroups the summary again .The only difference which is noticed by masking the scores are in Thomas high data set 

###•	How does removing the ninth graders’ math and reading scores affect Thomas High School’s performance, relative to the other schools?

For  Thomas high masking the reading and math score affects the overall school summary in the following way : The average math score and reading score both changed , np.nan decreases passing math  %  by 26 .9% and reading  by 26.8 % and in turn reduces  overall passing by  26.9 %

###•	How does removing the ninth-grade scores affect the Math and Reading Scores by Grade, Scores by School Spending, Scores by School Size, and Scores by School Type? 

1: For Thomas high earlier math_score_by_grade for 9th graders is equal to 83.59 but after adding NaN the result is 
Thomas High School	NaN	83.087886	83.498795	83.497041
Which effects the overall gradings 

2 :The spending range per students also get affected : 
There is variation in the $630-644 bin , the overall passing percentage decreases by  almost 6 % in this case .Which in turn effects the spending  range student summary 
3: From this analysis we can say that Thomas high school is a medium size school as masking the math and reading scores affects the medium size bin :
Earlier it was : 
Medium (1000-2000)	83.4	83.9	94	97	95
After replacing the value 
Medium (1000-2000)	83.361201	83.873869	88.327523	91.261628	89.794576

4:Similarly Thomas High  bing a charter decreases the overall % Passing Math,% Passing Reading and 
% Overall Passing

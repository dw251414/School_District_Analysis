# School_District_Analysis
Using Python and the Pandas library to analyze school district data and showcase trends in school performance.

Analysis available in the Jupyter Notebook - **PyCitySchools_Challenge.ipynb**

### Background

The grades of the ninth graders at THS, "Thomas High School", have been changed. While administrators do not know the full extent of this academic dishonesty, they want to uphold the standards of state testing and have turned to you for help.
After assessing the situation with the school superintendent and Maria, you decide the best approach is to:
- Replace the ninth-grade math and reading scores from THS.
- Keep all other data associated with the ninth-grade students and THS intact.

### Objectives

The goals of this challenge are for you to:
- Filter DataFrames using logical operators.
- Replace the incorrect values with NaN.
- Explain how your PyCitySchools analysis changes after you handle the incorrect data.  

### Results

- Create a duplicate of PyCitySchools.ipynb and rename it PyCitySchools_Challenge.ipynb.
- Correct the students' names so there are no professional prefixes or suffixes.
- Replace the reading and math scores for ninth graders at THS with NaN.
- Merge the clean student data with the school dataset.
- After replacing the reading and math scores, complete the following steps and answer the questions

    - Questions 
        - **How is the district summary affected?**
            - **Initial Data**
            - Average Math Score, Average Reading Score, % Passing Math, % Passing Reading, % Overall Passing
            - 79.0, 81.9, 75, 86, 65
            - **Post-Cleanup**
            - Average Math Score, Average Reading Score, % Passing Math, % Passing Reading, % Overall Passing
            - 78.9, 81.9, 74, 85, 64
            - **Summary:** 
            - Minor downward change in district averages
        - **How is the school summary affected?**
            - **Initial Data** 
            - THS % Overall Passing = 91, 2nd place
            - **Post-Cleanup**
            - % Overall Passing = 65, 8th place
            - **Summary:** 
            - Overall ranking order change due to change in THS' ranking
        - **How does replacing the ninth graders’ math and reading scores affect THS' performance, relative to the other schools?**
            - **Summary:** 
            - THS' ranking adjusted from 2nd to 8th, while the % Overall Passing decreased from 91% to 65%.
        - **How does replacing the ninth-grade scores affect the following?**
            - **Math and Reading Scores by Grade**
                - THS 9th grade math/reading scores set to "nan" = 0
                - Totals for passing math/reading across grades dwindle, while 9th grade scores = failing
                - Average scores are not significantly affected by discariding 9th grade scores
                - Number of students with a math grade:
                  - **Initial Data** 
                  - THS: 1635
                  - **Post-Cleanup**
                  - THS: 1174
                -  passing percentage is reduced as Total number of students (denominator) remains unchanged, but total passing value (numerator) is reduced by the number of removed 9th grade scores.
            - **Scores by School Spending**
                - THS is in the spending bucket "$630-644"
                - Removing 9th grade scores reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for spending bucket "$630-644" --
                  - **Initial Data**
                  -  73, 84, 63
                  - **Post-Cleanup**
                  -  67, 77, 56
            - **Scores by School Size**
                - THS is in the "Medium (1000-2000)" size bucket
                - Removing 9th grade scores reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for size bucket "Medium (1000-2000)" --
                  - **Initial Data**
                  -  94, 97, 91 
                  - **Post-Cleanup**
                  -  88, 91, 85
            - **Scores by School Type**
                - THS is in the "CHARTER" type bucket
                - Removing 9th grade scores reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for type bucket "CHARTER" --
                  - **Initial Data**
                  -  94, 97, 90 
                  - **Post-Cleanup**
                  -  90, 93,	87


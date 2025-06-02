# Debugging-AI

This repository is dedicated to providing resources and tools to help users debug, troubleshoot, and streamline their R code and workflow development.

## Debugging

Chances are, you have already had to debug code - nobody's perfect! Therefore, knowing how to spot mistakes is one of the most critical aspects of coding.

### **Debugging techniques**

Below is a collection of common techniques and best practices for debugging R code:

-   Debugging Guide From Hadley Wickham - <https://adv-r.hadley.nz/debugging.html>

-   Debugging Guide from Data Flair - <https://data-flair.training/blogs/debugging-in-r-programming/>

-   Debugging Zine (paid, but very cool). - <https://wizardzines.com/zines/debugging-guide/>

-   The first few paragraphs of this useful rant about working directories - <https://www.tidyverse.org/blog/2017/12/workflow-vs-script/>

### **Error codes and solutions**

Here is a list of some common R error messages and their explanations, along with solutions to fix them:

-   `Error: object 'x' not found` - This means that R cannot find the object 'x' in the current environment. The solution is to check the spelling (and case!) of the object, and make sure it has been defined and that the variable exists in your environment.

-   `Error in if (x) { : missing value where TRUE/FALSE needed` - This means that the if (or any conditional) statement is trying to evaluate a missing value. The solution is to check the values passed to the if (or any conditional) statement and ensure that they are not missing.

-   `Error in x[y] : object of type 'closure' is not subsettable` - This means that the object being indexed is a function, not a vector or data frame. The solution is to check the object being indexed and make sure it is a vector or data frame, or use the appropriate function to extract the desired information.

-   `Error in library(x) : there is no package called 'x'` - This means that the R interpreter cannot find the specified package. The solution is to check the spelling and case of the package name and make sure it is installed on your system.

-   `Error in file(file, ifelse(append, "a", "w")) : cannot open the connection` - This means that R cannot open the specified file. The solution is to check the file path and permissions, and make sure that the file is accessible by R.

-   `Error: unexpected symbol in:"x <- c(1, 2, 3) +` - This means that there is an unexpected symbol, such as a typo, in the R code. The solution is to check the code for typos and correct them, most commonly this is a missing comma or parentheses; or, you are providing the wrong arguments to a function call.

-   `Warning: In x + y : longer object length is not a multiple of shorter object length` - This means that the vectors being added have different lengths, and R is recycling the shorter vector to match the length of the longer vector. This can cause unexpected results and it is recommended to check the lengths of the vectors and make sure they match before performing any operations.

-   `Error in parse(text = x) : <text>:1:0: unexpected end of input` - This means that there is a problem with the R code being parsed, often due to a missing parenthesis or bracket. The solution is to check the code for any missing or extra characters and correct them.

-   `Warning: NAs introduced by coercion` - This means that R is introducing missing values (NA) due to a type coercion. This can happen when trying to combine different types of data, such as characters and numerics. The solution is to check the data types of the variables and make sure they are compatible before performing any operations.

-   `Error in x[y == z] : invalid subscript type 'list'` - This means that the script used to index the object 'x' is not a valid type, such as a list. The solution is to check the type of the object being used to index 'x' and make sure it is a valid type such as a logical vector, numeric vector or character vector.

-   `Error in x[y] <- z : replacement has length zero` - This means that the object being used to replace the values in 'x' has a length of zero. The solution is to check the object being used for replacement and make sure it has the same length as 'x' or the corresponding index.

-   `Warning: Non-ASCII characters are being interpreted as ASCII` - This means that R is interpreting non-ASCII characters as ASCII characters. This can cause unexpected results and it is recommended to check the encoding of your data and make sure it is in the correct format before performing any operations.

These are just a few of the most common errors in R, but there are many other types of error messages that can occur. Keep in mind that the best way to troubleshoot R errors is to read the error message carefully and look for clues about where the error is occurring in your code. And, use the internet as a resource! It is very unlikely you are the first person to encounter any given error. Which brings us to...

## Artificial Intelligence (AI) Models

The following section is a modification of a Twitter thread written by Santiago Valdarrama (@Santiago).

AI models like DeepSeek, powered by natural language processing, can be valuable tools in code development if used effectively. These models can understand and generate human-like text, offering **assistance in writing and suggesting code snippets.** However, it's important to note that while they enhance productivity, AI models are currently not a replacement for coding; they should act only as supportive aids. Never take the response of an AI model at face value. **AI models are flawed and make mistakes often.** Even so, they have the potential of saving you substantial time and can give you a massive boost. With that, here is a list of ways in which AI models can be effectively used to help you on your coding journey.

1)  **Explaining code.** AI model explanations can be very detailed. Dropping convoluted or confusing code into an AI model (plus a request to explain it) can be much quicker than trying to figure out code on your own.

2)  **Improving existing code.** Asking an AI model to improve existing code by dropping it into the chat-bot plus describing what you want it to accomplish will often result in a response that includes working (or, at least close to working), modified code.

3)  **Rewriting code with a different style.** For example, it can be great for re-writing code written in base R into {tidyverse}-style code. AI models will not only give you the updated code, they will also explain the reason for the changes they make.

4)  **Simplifying code.** Asking AI models to simplify complex code can result in a much more compact version of the original code. The output will also provide an explanation for the changes, as well as whether the simpler version is as efficient as the original code.

5)  **Debugging.** If you are having a hard time finding the source of an error in your code, AI models are a great solution. Just provide it the code, and it will often find it and fix it for you.

6)  **Workflow development.** Use AI models to kick off the structure of anything new you want to write.

7)  **Writing test cases.** When writing functions, you can use AI models to generate test cases for you to use in testing whether a function is working the way you want it to.

8)  **Exploring alternatives.** Asking an AI model what the most efficient way to perform a coding action might teach you new ways of writing more efficient and sophisticated code.

9)  **Translating code.** Anytime you want to translate some code from one language to another, ask an AI model to help you.

10) **Writing documentation.** Ask an AI model to write the documentation for a piece of code, and it usually does a pretty great job. It will often even include usage examples as part of the documentation.

## The assignments

1)  `01-debugging_code.Rmd` - This is the R markdown that was used to make the `01-debugging_code_output.html` in the `data/` folder. However, we have **purposefully added mistakes to it**. Your assignment is to fix these mistakes so that it can once again produce the rendered document provided. **Save a copy of this file as '01-debugging_code_YOURNAME.Rmd' with the fixed code, the 5 things you found were incorrect, and knit it to HTML so we can see your correct rendered version.**

2)  `02-using_ai.Rmd` - Follow the questions/prompts in this document to post to a chat bot. **Save a copy of this file as '02-using_ai_YOURNAME.Rmd' to put your responses in.**

#### When you have completed both the code debugging assignment and the AI models assignment, submit both completed assignment files.

**Cited Source**

Santiago Valdarrama [@Santiago], (2023, January 6). *11 ways ChatGPT saves me hours of work every day, and why you'll never outcompete those who use AI effectively. A list for those who write code:* [Tweet thread]. <https://twitter.com/svpino/status/1611357154514186241?s=46&t=BH_LjPb_sC-wByPLLnoc1A>

**Data Source**

Singh, Utkarsh (2023). NOAA Atlantic hurricane database. Kaggle. <https://www.kaggle.com/datasets/utkarshx27/noaa-atlantic-hurricane-database?resource=download>

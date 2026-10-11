# AI Usage Documentation

## 1. AI Tool Used

- **Tool:** ChatGPT (OpenAI)
- **Purpose:** Assistance with R programming, understanding statistical concepts, debugging code, and reviewing my work.

I primarily used ChatGPT as a coding and learning assistant throughout this project. ChatGPT helped me generate and troubleshoot R code, understand statistical concepts, and review my reports. I was responsible for running the simulations, examining the results, analyzing patterns, and making the final decisions about which sample sizes I considered approximately Normal.

I also used ChatGPT to ask follow-up questions and challenge statistical explanations when the results were unclear or did not match my observations.

## 2. AI Prompts and Responses

The following table summarizes examples of my prompts and follow-up questions, along with what ChatGPT provided. These are summarized examples rather than exact transcripts.

| Topic | Example Prompts and Follow-Ups | What AI Provided |
|------------------------|------------------------|------------------------|
| Monte Carlo Simulation | How do I simulate sample means for different sample sizes in R? How does `replicate()` work? | Generated R code using `replicate()` and `lapply()`, and explained how the functions work. |
| Histograms and Q-Q Plots | How do I create and interpret histograms and Normal Q-Q plots for different sample sizes? | Provided plotting code, reference curves and lines, and explanations of how to interpret the graphs. |
| Debugging | Why are my Binomial plots showing results from the Exponential distribution? | Identified a variable-name mismatch and suggested corrections. |
| Statistical Concepts | How do skewness, kurtosis, and standard error help evaluate Normality? | Explained statistical concepts and how they relate to the sampling distributions. |
| Challenging Sample-Size Decisions | Why should I choose this sample size instead of a smaller one when their standard errors are nearly the same? | Explained why similar standard errors do not necessarily mean the sampling distributions are equally close to Normal, and discussed other evidence to consider. |
| Cauchy Distribution | Does the Cauchy distribution ever become Normal? Why does the Q-Q plot at n = 50 appear to follow the line? | Explained why the usual CLT does not apply to the Cauchy distribution and how extreme values can distort the Q-Q plot scale. |
| Additional Sample Sizes | How can I add more sample sizes to my simulation to examine the transition more closely? | Helped adjust the R code to include additional sample sizes for comparison. |
| Numerical Evidence | How do I calculate simulated means, standard deviations, skewness, kurtosis, and IQR? | Provided R code to calculate and organize numerical statistics into tables. |
| Report Review | Can you review my Quarto reports for errors and statistical accuracy? | Reviewed code, explanations, grammar, and formatting, and suggested corrections. |
| Final Summary | Help me organize and review my comparison of the five distributions. | Suggested an outline, helped draft and revise explanations, and reviewed the final summary. |

## 3. Verification and Corrections

I ran the R code in RStudio and examined the generated histograms, Q-Q plots, and numerical tables to verify the results.

When I encountered errors or unexpected results, I asked ChatGPT follow-up questions to understand the problems and possible corrections. For example, I fixed a variable-name mismatch that caused the Binomial plots to display results from the Exponential simulation.

For the Cauchy experiment, I adjusted the histogram display range to better visualize the central distribution while keeping extreme observations in the simulations. I also investigated why the Q-Q plot at n = 50 appeared to follow the reference line, even though the other evidence suggested that the distribution was not Normal.

I did not rely only on the initial simulation results. I added more sample sizes to some experiments to examine the distributions more closely and make more informed decisions about the Normality thresholds.

## 4. My Analysis and Contributions

For each distribution, I examined the histograms, Q-Q plots, and numerical evidence to identify patterns as the sample size increased. I compared the results across different sample sizes and selected the smallest tested n that I felt comfortable calling approximately Normal.

I also challenged explanations when I noticed something that needed further investigation. For example, I questioned why one sample size should be selected over another when their standard errors were nearly identical. I learned that standard error measures the spread of the sampling distribution, but does not determine whether its shape is approximately Normal. I used the histograms, Q-Q plots, and numerical evidence together to make my decisions.

I also questioned whether the sampling distribution of the Cauchy sample mean would ever become approximately Normal as n increased.

To make my experiments more thorough, I chose to test additional sample sizes, especially around the sample sizes where the sampling distributions appeared to become approximately Normal.

My final selected sample sizes were:

- **Standard Normal:** n = 2
- **Six-Sided Die:** n = 10
- **Exponential:** n = 30
- **Binomial:** n = 40
- **Cauchy:** None

I compared these results and developed my conclusions about how the original population affects the Central Limit Theorem and why n = 30 is not a universal rule.

ChatGPT helped me draft and edit some of the written explanations based on my observations. However, the analysis of the results, follow-up investigations, decisions to expand the simulations, and final sample-size selections were my own.

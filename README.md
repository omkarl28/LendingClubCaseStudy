# Lending Club Analysis using EDA & Python Visualization
> To understand the **driving factors (or driver variables)** behind loan default, i.e. the variables which are strong indicators of default and identification of defaulters **using EDA** is the aim of this case study


## Table of Contents
* [Project Info](#project-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

## Project Information
### 1. Business Problem Statement
When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:

If the applicant is **likely to repay the loan**, then not approving the loan results in a **loss of business** to the company

If the applicant is **not likely to repay the loan**, i.e. he/she is likely to **default**, then approving the loan may lead to a **financial loss** for the company

The aim is to identify patterns which indicate if a person is likely to default, which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc. 

We will use EDA to understand how **consumer attributes** and **loan attributes** influence the tendency of default.

### 2. Dataset
When a person applies for a loan, there are **two types** of decisions that could be taken by the company:

**Loan accepted:** If the company approves the loan, there are 3 possible scenarios described below:

- **Fully paid:** Applicant has fully paid the loan (the principal and the interest rate)

 - **Current:** Applicant is in the process of paying the instalments, i.e. the tenure of the loan is not yet completed. These candidates are not labelled as 'defaulted'.

 - **Charged-off:** Applicant has not paid the instalments in due time for a long period of time, i.e. he/she has **defaulted** on the loan 

Loan rejected: The company had rejected the loan (because the candidate does not meet their requirements etc.). Since the loan was rejected, there is no transactional history of those applicants with the company and so this data is not available with the company (and thus in this dataset)

The Dataset contains the information about past loan applicants (around 113 columns & 39,000 rows) and whether they ‘defaulted’ or not. 


## Conclusions
### 1. Segmented Univariate Analysis
- <p style='background-color:#04AF70;padding:10px;color:white'>Default rate is decreased till Rs 9600 and after that the <b>default rate increased as the loan amount increased</b> for customers.</p>
- <p style='background-color:#04AF70;padding:10px;color:white'>Default rate is increased as the interest rate increases.</p>
- <p style='background-color:#04AF70;padding:10px;color:white'>Default rate is increased as the revolving utilization limit increases.</p>
- <p style='background-color:#04AF70;padding:10px;color:white'>Default rate is decreasing from customers with less annual income to more annual income. 
        <br/> <b>defaulted <label style="font-size:25px">&#8733;</label> 1/annual_income</b></p>
- <p style='background-color:#04AF70;padding:10px;color:white'>Default rate is increased as the debt to income ratio is more for customers.</p>
- <p style='background-color:#04AF70;padding:10px;color:white'>Default rate is more in 60 months term and we can say that default rate increases as the term increases.</p>
- <p style='background-color:#04AF70;padding:10px;color:white'>Default rate is increasing from Grade A to G.</p>
- <p style='background-color:#04AF70;padding:10px;color:white'>Default rate is highest in <b>small business</b> & it is also high in house, educational & renewable energy but it has data <1%. So it <b>might</b> effect the defaut rate.</p>
### 2. Bivariate Analysis
- <p style='background-color:#04AF70;padding:10px;color:white'><b>Loan amount</b> is highly correlated with funded amount, funded amount investment & installment.</p>
- <p style='background-color:#04AF70;padding:10px;color:white'><b>Interest rate, Revolving utilzation rate</b> are positively correlated to all continuos variables when compared to other continuos variables.</p>
- <p style='background-color:#04AF70;padding:10px;color:white'><b>Default rate</b> is increased as the loan amount & annual income increases & every bin in annual income has <b>atleast 50%</b> default rate.</p>
- <p style='background-color:#04AF70;padding:10px;color:white'>Default rate is <b>highly co-related</b> to interest rate & grade</p>
- <p style='background-color:#04AF70;padding:10px;color:white'>Default rate is more for all categories in purpose as revol util increases</p>
- <p style='background-color:#04AF70;padding:10px;color:white'>Default rate is <b>decreasing</b> as the dti range and interest rate increased</p>
- <p style='background-color:#04AF70;padding:10px;color:white'>Default rate is increasing as the loan amount and term increased
    <br/>It is also observed that defaulted < loan paid for 36 months and then for 60 months it changed to defaulted > loan paid</p>

<div class="observation" style='background-color:#6495ED;font-size:16px;padding:10px;color:white'>
    <p>Therefore, we can conclude from the above insights that the following variables <b>impact</b> the target variable <b>defaulted</b>
       <br/>&emsp;&emsp; > Interest Rate
       <br/>&emsp;&emsp; > Grade
       <br/>&emsp;&emsp; > Annual Income
       <br/>&emsp;&emsp; > Purpose
       <br/>&emsp;&emsp; > Term
       <br/>&emsp;&emsp; > Revolving utilization rate (revol_util)
       <br/>&emsp;&emsp; > Debt to income ratio (dti)
       <br/>&emsp;&emsp; > Loan amount
    </p>
</div>

## Technologies Used

- numpy - 1.23.5v
- pandas - 1.5.3v
- matplotlib.pyplot - 3.7.0v
- seaborn - 0.12.2v
- regex - 2.5.116v
- python - 3.10.12v

## Acknowledgements

- Our team would like to thank [Anand S](https://sg.linkedin.com/in/sanand0) for his explanation on EDA.
- References for seaborn plots are taken form [Tutorials Point](https://www.tutorialspoint.com/seaborn/seaborn_tutorial.pdf)
- References for annotating plots are taken form [Geeks for Geeks](https://www.geeksforgeeks.org/how-to-annotate-bars-in-barplot-with-matplotlib-in-python/)

## Contact
Created by 
- [@Ravalnath_omkar_lawande](https://in.linkedin.com/in/omkar-lawande)
- [@gnyana_teja](https://www.linkedin.com/in/somanchi-gnyana-teja/) 
 
Feel free to contact us 👍

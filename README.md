# Project Title: Boosting Engagement and Funding for the Digital Literacy Initiative

Author: David Macias
Date: March 10, 2024

## PROBLEM
A local non-profit organization in Phoenix, Arizona, known as Community Tech Link, has been facing two key challenges that are causing concern among stakeholders, including sponsors, board members, and community partners:

➡ Declining participation in the Digital Empowerment Program (DEP), which provides technology training and internet access to underserved adults.

➡ Rising demand for technical support and computer donations, yet slower turnaround times due to outdated systems and under-resourced staff.

The Digital Empowerment Program (DEP) is largely funded by organizations like the Arizona Community Foundation and TechAccess USA, which are committed to closing the digital divide. DEP offers services to adults who need digital skills for work, education, and everyday life. The program includes:

Basic Computer Literacy Courses

Job Search and Online Application Support

Low-cost or Donated Devices Distribution

Over the past two years, the DEP has seen a steady drop in enrollment for Courses 1 and 2, while Course 3 (device distribution) has seen high demand. The support team has also reported a significant backlog in device processing due to staff shortages.

Key challenges identified:

The organization needs increased and stable funding to onboard technical trainers and program assistants.

Outdated data collection systems (Excel files stored on local computers) limit the organization's ability to report outcomes and scale operations effectively.

## DATASET
The dataset covers service delivery from January 2021 to December 2022, including:

Number of new enrollments per month

Attendance and completion rates

Device distribution logs

Staff allocation and service hours

Wait times for device repair and delivery

Data Quality Notes:

Accuracy: Verified using signed attendance sheets and intake forms.

Relevancy: Directly tied to program KPIs and funder requirements.

Completeness: 98% complete; minor gaps in follow-up survey responses.

Timeliness: Updated monthly; date fields aligned with service logs.

Consistency: Cleaned using Excel and Python for consistent formatting and date fields.

## WHAT I DID
✔ Migrated the program’s tracking system from local Excel files to a centralized SharePoint system integrated with Microsoft Forms, enabling automated data entry and real-time dashboards.

✔ Created Tableau dashboards to visualize trends in participation, dropout rates, and service demand. This helped make the case for new funding by demonstrating growth in demand despite staff limitations.

✔ Negotiated an updated funding agreement, increasing the per-client funding rate by 80% and securing multi-year support from TechAccess USA, reducing the reliance on annual grant renewals.

## WHAT I WILL DO
Forecast seasonal peaks in enrollments and support needs using historical data to recommend staffing plans.

Use Tableau to model ROI for different program enhancements, such as additional workshops or device types.



## CEAP DATA CLEANING

The dataset is first cleaned in Excel including but not limited to the following:

- birthday data type
- birthday entered wrong (eg: 1/1/5674, 12-5/1968, 123/2/1970, Agust 5)
- birthday not completed
- using letter O instead of number 0 in dates
- spell out birthday month (eg: August, 30,)
- numerical currency data that's written out (eg: $300/month, 500 job + $400 ssi)
- currency having . and , in wrong places (eg: 6.66.7, 134,05)
- number stored as object or the number is stored as text (use =VALUE()) to convert back. Use =IF(AK2="","",VALUE(AK2)) to convert to float number in excel if containing NaN in rows.
- extremely high monthly income
- negative birthday
- negative income
- find all and replace to fix spelling in the utility company columns to keep it consistent (eg: V24/7, v 247, V247 company)
- turn name into cap for first letter using =PROPER
- grab the year off birthday using =TEXT(cell, "yyyy")
- use =LEFT() or =RIGHT() to grab the specific number for household size-long
- use text to column to fix values
- =DOLLAR() to convert currency if needed
- Using describe() in Python, I run into more issue with the numerical data so the dataset needs to be examine and clean further in Excel.


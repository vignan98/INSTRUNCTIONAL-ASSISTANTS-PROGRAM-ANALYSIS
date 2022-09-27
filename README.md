# INSTRUNCTIONAL-ASSISTANTS-PROGRAM-ANALYSIS
Introduction
This data analysis project is for the Information Technology Services of Northeastern’s
Instructional Assistant program. Instructional assistants (IAs) are trained student technicians
who will be deployed to and will work in the registrar-controlled classrooms to assist faculty with
classroom technology and facilitating interactions. They will be available in the classroom to
help faculty who are teaching in a classroom as well as to assist in the classroom when faculty
are teaching remotely. Student employees will maintain the computers and audio visual
equipment in the NUFlex classrooms across campus. In this project we will analyze the impact
of this program as well the operational gaps to help the ITS stakeholders improve the efficiency
and monitor the operations of this program.
Problem Statement
To analyze number of dispatches raised in different Halls, Dispatch State, Scope of dispatches,
Claim Time, Dispatches from multiple classroom equipment, Impact of
weekday/weekend/holiday dispatches. This would help the ITS team to organize and schedule
handling the dispatches in an effective way.
Data Description
We gathered two data sets from the ITS department. The data was collected for the Fall 21
semester i.e. Septempber’21 - December’21. The first data set is the dispatch log dataset which
had the information of the row wise the individual dispatches, with columns such as issue
reported, time of the request, building, classroom number. The total number of records in this
dataset were 3200. The second data set is the instructional assistant dispatch log, which has
the information of the form responses of the dispatch, once the IA finishes the dispatch, it has
columns such as the kind of issue, is the escalation required or not, explanation of the issue etc.
The total number of records in this dataset were 2014.
Methodology
1. Few of the data cleaning steps like conversion of date column to datetime format and
changing the incorrect naming conventions of the Northeastern Halls were performed
before integrating the data
2. Both the file dispatch logs and an instructional assistant dispatch log have been joined
on (start time, Building) and (Email received, Building) to analyze the End State of each
dispatch.This eventually reduced the number of rows of the data set .
3. Based on the start time and completion time of the dispatch, the time for addressing the
dispatch was calculated. Also the time for dispatch claim was calculated based on
columns Dispatch_notified and Dispatch_claimed. This entity helps to analyze the
percentage of dispatches claimed in a given time period.
4. Based on the dispatch issue keywords were generated focusing on the equipment that
was mentioned in the dispatch. This helps us to categorize different types of dispatches
which inturn helps to find percentage of dispatches from each category
5. Also the classroom from which the dispatches have been raised are categorized into 4
different types like NUFlex Auto, Standard, NUFlex Cart, NUFlex Manual. This was
integrated taking into account each type of class rooms from which dispatches were
raised. This insight would help to visualize the number and type of dispatches from each
type of classroom.
Design Process
The Project was distributed in two dashboards. The first dashboard concentrated on giving an
overview of the IA program. It was designed to give the user an understanding of all the
variables that contribute to the working of the IA program. This dashboard also included details
regarding the layout of buildings and different kinds of classrooms at Northeastern. The aim of
this dashboard was to present the user with a snapshot view of the current performance of theIA
program. The second dashboard talks about the impact of different factors such as day and
hour of the week, holidays and weekends and classroom type on the workload of the IA
program. Together the dashboards give a comprehensive understanding of the program. The
different visualizations used help us to present the user with insights about the program. These
insights are discussed below.
Key insights
1. Ryder and Snell library have the most number of dispatches, as compared to other
buildings.
2. About 18% of dispatches require manager review. This impacts dispatch resolution time
and needs to be addressed.
3. 20% of all dispatches show a claim time of more than 5 minutes. These claims need to
be investigated.
4. We see around 25% of the dispatches raised are not within the ITS scope.
5. We also see that issues with classroom pcs and projects show the highest number of
dispatches. These dispatches are also often urgent and escalated
6. We see a dip in the number of dispatches at 2pm. This dip however again rises at the
end of the day.
7. We also observe as the semester progresses the number of dispatches reduces.
8. As we analyzed the impact of holidays and weekends on the number of dispatches we
discovered that holidays don't give any spike in the number of dispatches. Weekends on
the other hand generally show a small spike in the number of dispatches.
9. NUFlex Auto classes show very high dispatches, this is followed by standard
classrooms.
10. NUFlex manual shows a maximum number of issues with classroom pcs and projectors

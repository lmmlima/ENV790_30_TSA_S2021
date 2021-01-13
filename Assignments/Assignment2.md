
\documentclass[12pt]{article}
% [12pt,who12]
\setlength{\textheight}{8.5in}
\setlength{\topmargin}{-0.25in}
\setlength{\oddsidemargin}{0in}
\setlength{\textwidth}{6.6in}


\usepackage[utf8]{inputenc}
\usepackage[english]{babel}
\usepackage{parskip}
\setlength{\parindent}{0in}
%\setlength{\parskip}{6pt}
\renewcommand{\baselinestretch}{1.2}

\newcommand{\noi}{\noindent}

\usepackage{comment}
\usepackage{xcolor}
\usepackage{enumitem}
%\renewcommand{\theenumi}{\Alph{enumi}}

\usepackage{amsmath}
\usepackage{float}
\usepackage{longtable}
\usepackage{multirow}
\usepackage{multicol}
\usepackage{natbib}
\renewcommand{\bibsection}{}

\begin{document}
%\baselineskip0.22in

\begin{center}
\noi{\Large \bf ENV 790.30 - Time Series Analysis for Energy Data\\}
\noi{{\bf Spring 2020}\\}
\end{center}


\begin{multicols}{2}
\begin{center}
\noi{\bf Instructor\\ } 
\noi{Luana Medeiros Marangon Lima\\
luana.marangon.lima@duke.edu\\}
\noi{{Office hours:} Tue 11:00 to 12:00 pm \& \\ Wed 1:30 to 2:30 pm (Gross Hall 101K)\\}
\end{center}

\columnbreak

\begin{center}
\noi{{\bf TA}\\
Monica Simarmata\\
monica.simarmata@duke.edu\\}
\noi{{Office hours:} Mon 2:00 to 3:00 pm \& \\ Thu 2:00 to 3:00 pm (GH 2107b)\\}
\end{center}
\end{multicols}
%
%
\noindent\rule{6.6in}{0.4pt}
\begin{center}
\noi {\bf Assignment \#2}\\
\noi{ Due date: 02/07/2020}\\ 
\end{center}


%\section*{Question 1}
\noi{\\For this assignment you will need to develop a script using R or Python. You are supposed to submit a report in .pdf using Sakai. Your report should contain the answer to each question and the plots you obtained (when applicable). After you finish the report, include the lines of your script as an appendix. You do not need to submit your script file, just the .pdf report. If you use R, you may use R Markdown to generate your report.

Consider the data provided in the spreadsheet "RenewableEnergy.xlsx". The data comes from the US Energy Information and Administration and corresponds to the December 2017 Monthly Energy Review. The spreadsheet is ready to be used. Use the command $read.table()$ to import the data in R or $panda.read\_excel()$ in Pyhton (note that you will need to import panda package). }

Packages needed for this assignment:"forecast","tseries", and "dplyr". Install these packages, if you haven't done yet. Do not forget to load them before running your script, since they are NOT default packages.\\

\begin{enumerate}[label=(\alph*)]
\item You will work only with the following columns: Total Biomass Energy Production, Total Renewable Energy Production, Hydroelectric Power Consumption. Create a data frame structure with these three time series only. Use the command head() to verify your data.

\item Transform your data frame in a time series object and specify the starting point and frequency of the time series using the function ts().

\item Compute mean and standard deviation for these three series.

\item Display and interpret the time series plot for each of these variables. Try to make your plot as informative as possible by writing titles, labels, etc. For each plot add a horizontal line at the mean of each series in a different color.

\item Compute the correlation between these three series. Are they significantly correlated? Explain your answer.

\item Compute the autocorrelation function from lag 1 up to lag 40 for these three variables. What can you say about these plots? Do the three of them have the same behavior?

\item Compute the partial autocorrelation function from lag 1 to lag 40 for these three variables. How these plots differ from the ones in item(f)?

\item From the plot in part (d), do these series appear to have a trend? If yes, what kind of trend? 

\begin{comment}
\item Use least squares to fit a linear time trend to these time series. Ask R to print the summary of the regression. Interpret the regression output. Save the regression coefficients for further analysis.

\item Use the regression coefficients from item(i) to detrend the series. Plot the detrended series and compare with the plots from part (d). What happened? Did anything change?

\item Repeat items (f) and (g) for the detrended series in part (j). Did the plots change?

\item Does any of these series seems to have a seasonal trend? Which one/ones? Use least squares to fit a seasonal-means trend to this/these time series. Ask R to print the summary of the regression. Interpret the regression output. Save the regression coefficients for further analysis.

\item Use the regression coefficients from item(ll) to detrend the series. Plot the detrended series and compare with the plots from part (d). Did anything change?

\item Repeat items (f) and (g) for the detrended series in part (m). Did anything change?

\item Now let's try to difference these three series using function diff(). Start with the original data from part (b). Try differencing first at lag 1 and plot the remaining series. Did anything change? Do the series still seem to have trend?

\item Compute Mann-Kendall and Spearman's Correlation Rank Test for each time series. Ask R to print the results. Interpret the results. 
\end{comment}
\end{enumerate}




\end{document}

# School-Choice-Mechanism-Design
\documentclass[11pt]{article}
\usepackage{graphicx} % Required for inserting images
\usepackage{amsmath}
\usepackage{times} 
\usepackage{amssymb}
\usepackage{float} 
\usepackage{url}
\usepackage{setspace}


\usepackage[style=apa,backend=biber]{biblatex} 
\addbibresource{ref.bib}
\setlength{\parindent}{0pt}%


\title{A Mechanism Design Approach towards Equitable School Choice Policy}
\author{Vighnesh Avadhanam}
\date{November 2024}

\begin{document}
\singlespacing 

\maketitle

\section{Introduction}

In the United States, school choice policies are still at the forefront of debate amongst state legislators, educators and families. One of the central issues faced in designing these policies is to allow lower-income students to get access to higher quality schools. However, public school allocation is still largely based on a students’ neighborhood which exacerbates income inequalities in access to quality education, as higher-income neighborhoods are likely to have better funded schools. Some of this has been combated in big cities across the country and the world by designing better allocative mechanisms. Abdulkadiroglu and Sonmez (2003) laid the foundation to think about school choice under a mechanism design framework, which is essentially a more generalized auction-like framework. The goal of this paper is to extend a mechanism of school choice to consider how these income inequalities in education access could potentially be solved, by presenting a theoretical framework of allocative mechanisms.

\nocite{*} 

\vspace{10.0pt}

This paper will first provide a quick primer of the theory of mechanism design followed by a literature review. I will then consider two extensions to the basic model of school choice, namely Controlled Choice and Information Asymmetry. Within these settings, I attempt to consider allocative mechanisms that could improve school allocations for lower-income students.

\section{Main Body}

\subsection{Theory of Mechanism Design and School Choice}
Traditionally, economics takes institutions as given and analyzes the outcomes of these institutions. However, mechanism design is a normative economic concept whereby a social planner decides on the outcome that is desirable, possibly based on some measure of welfare. The planner then designs a system that most effectively gets that desired outcome. The theoretical framework is as follows.

\vspace{5.0pt}

\begin{itemize}
    \setlength{\itemsep}{0pt}
    \item \textbf{Set of agents}: \( N = \{1, 2, \dots, n\} \),
    \item \textbf{Set of outcomes}: \( X \),
    \item \textbf{Type of agent \( i \)}: \( \theta_i \in \Theta_i \), where \( \Theta_i \) is the set of possible types for agent \( i \),
    \item \textbf{Type profile}: \( \theta = (\theta_1, \dots, \theta_n) \in \Theta \), with \( \Theta = \Theta_1 \times \dots \times \Theta_n \),
    \item \textbf{Probability distribution over type profiles}: \( \phi \in \Delta \Theta \), where \( \Delta \Theta \) is the set of all probability distributions over  \( \Theta \)
    \item \textbf{Utility function for agent \( i \)}: \( u_i : X \times \Theta_i \to \mathbb{R} \),
    \item \textbf{Mechanism}: \(M = ((S_1, S_2, \dots, S_n), g(\cdot)) \), where \( g : C \to X \) and  \\ \( C = S_1 \times S_2 \times \dots \times S_n \). \(S_i\) is defined as the action or message given by agent \(i\)
\end{itemize}

The probability density function $\phi(\cdot)$, the type sets $\Theta_1, \dots, \Theta_n$, and the utility functions $\ u_i(\cdot)$ are assumed to be common knowledge among the agents. 

We can extend a similar idea to think about a theoretical framework for school choice. Instead of a planner making a decision \( x \in X \), we instead have schools making a decision of who to admit based on a priority ordering of students. So now the agents that we modeled above have an interaction with another set of agents instead of an "inactive" social planner. A general theoretical framework for school choice is as follows.

\vspace{10.0pt}

Consider a set of students  \( N = \{1, 2, \dots, |N|\} \), and a set of schools
  
\( S = \{s_1, s_2, \dots, s_{|S|}\} \). Each school \(s \in S \) has a capacity of \(q_s\). Each student \(i \in N\) has a strict preference relation \(P_i\) over $S \cup \{ i \}$ , where $\{i \}$ denotes the possibility of being unmatched possibly due to an outside option like a private school. Moreover, each school \(s \in S \) has a weak priority ordering  $\succeq_s$ over  $N \cup \{ s \}$ , where $\{s \}$ represents keeping a seat empty. A mechanism $\varphi$ determines a matching for any tuple \( (N,S,q,P,\succeq)\). In some school choice problems we can simply reduce the mechanism to $\varphi(P)$, as every other element can be considered constant. We apply the mechanism to $P$, but students give a signal defined by some preference relation $P'$, which may not be equal to $P$. For the sake of keeping consistent with the mechanism design framework I presented, we can instead consider $\varphi(P')$.

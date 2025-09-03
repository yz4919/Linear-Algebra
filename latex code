\documentclass[12pt]{report}
\usepackage{amsmath, amssymb, amsfonts}
\usepackage{amsmath, amssymb, amsthm}
\usepackage[dvipsnames]{xcolor}
\definecolor{darkgreen}{rgb}{0.0, 0.5, 0.0} 
\newtheorem{theorem}{Theorem}    
\newtheorem{lemma}{Lemma}        
\newtheorem{corollary}{Corollary}
\newtheorem{proposition}{Proposition}
\theoremstyle{definition}
\newtheorem{definition}{Definition}
\theoremstyle{remark}
\newtheorem{remark}{Remark}
\newtheorem{example}{Example}
\usepackage{bm}
\usepackage{mathtools}
\usepackage{tikz-cd}
\usepackage[margin=1in]{geometry}
\usepackage{enumitem}   % Customizable lists
\usepackage{multicol}    % Multiple columns
\usepackage{xcolor}      
\usepackage{graphicx}    
\newcommand{\vecb}[1]{\bm{#1}}        % Bold vector
\newcommand{\mat}[1]{\begin{bmatrix} #1 \end{bmatrix}}  % Shortcut for matrix
\newcommand{\R}{\mathbb{R}}           % Real numbers
\newcommand{\C}{\mathbb{C}}           % Complex numbers
\newcommand{\Z}{\mathbb{Z}}           % Integers
\newcommand{\N}{\mathbb{N}}           % Natural numbers

\newcommand{\colsp}{\mathrm{Col}}     % Column space
\newcommand{\rowsp}{\mathrm{Row}}     % Row space
\newcommand{\rank}{\mathrm{rank}}
\newcommand{\tr}{\mathrm{tr}}         % Trace
\newcommand{\inv}{^{-1}}              % Inverse
\usepackage{tikz}
\usetikzlibrary{arrows.meta, matrix, calc}
\title{linear algebra}
\author{yz4919}
\date{June 2025}
\begin{document}
\maketitle
\tableofcontents
\newpage
\chapter{Basic Notions}
\section{Peano Axioms: Definition of the set of natural numbers}
\begin{definition}
Assume $\exists$ a set $\mathbb{N}$ and a function $s: \mathbb{N} \to \mathbb{N}$ (called ``successor function''), such that the following hold:
\begin{itemize}
    \item[(A)] $0 \in \mathbb{N}$
    \item[(B)] $\forall n \in \mathbb{N},\ s(n) \in \mathbb{N}$
    \item[(C)] $\forall n \in \mathbb{N},\ s(n) \neq 0$
    \item[(D)] $n \neq m \Rightarrow s(n) \neq s(m)$
\item[(E)] Principle of Mathematical Induction: Let $P(n)$ be any statement pertaining to $\mathbb{N}$.
\begin{itemize}
    \item Suppose $P(0)$ is true.
    \item Suppose if $P(n)$ is true, then $P(s(n))$ is true.
\end{itemize}
Then $P(n)$ is true for all $n \in \mathbb{N}$.
\end{itemize}
\end{definition}

\textbf{Axiom of Infinity}

There is a set \( \mathbb{N} \) with an element \( 0 \in \mathbb{N} \) and a successor 
\( s: \mathbb{N} \rightarrow \mathbb{N} \) s.t. (A)–(E) hold.
\section{Equivalence Class (Equivalence Relations)}
\begin{definition}[Equivalence relation]
    Let \(\Omega\) be a set. Let \(\sim\) be a relation on \(\Omega\). We say \(\sim\) is an equivalence relation if and only if it is 
    \begin{itemize}
        \item reflexive: \(\forall x \in \Omega\), \(x \sim x\);
        \item symmetric: \(\forall x, y \in \Omega\), \(x \sim y \implies y \sim x\);
        \item transitive: \(\forall x, y , z \in \Omega\), \(x \sim y\), \(y \sim z \implies x \sim z\).  
    \end{itemize}
\end{definition}
\begin{definition}[Equivalence class]
    If \(\sim\) is an equivalence relation on \(\Omega\), then \(\sim\) partitions \(\Omega\) into mutually disjoint equivalence classes. 
\end{definition}
An equivalence class is of the form \[[x] := \{y \in \Omega: x \sim y\}.\]
\begin{definition}[representative]
If \(\mathcal{C}\) is an equivalence class, and \(x \in \Omega\) such that \(\mathcal{C} = [x]\), we say \(x\) is a representative of \(\mathcal{C}\).     
\end{definition}
\newpage
\chapter{Vector Space Basics}
\section{Vector Space}
\begin{definition}
    A vector space \( V \) is a collection of objects, called vectors, along with two operations —addition of vectors and multiplication by a number (scalar) —such that the following 8 properties (the so-called axioms of a vector space) hold:

The first 4 properties deal with addition:
\begin{enumerate}
    \item Commutativity: \( \mathbf{v} + \mathbf{w} = \mathbf{w} + \mathbf{v} \) for all \( \mathbf{v}, \mathbf{w} \in V \);
    \item Associativity: \( (\mathbf{u} + \mathbf{v}) + \mathbf{w} = \mathbf{u} + (\mathbf{v} + \mathbf{w}) \) for all \( \mathbf{u}, \mathbf{v}, \mathbf{w} \in V \);
    \item Zero vector: There exists a special vector, denoted by \( \mathbf{0} \), such that \( \mathbf{v} + \mathbf{0} = \mathbf{v} \) for all \( \mathbf{v} \in V \);
    \item Additive inverse: For every vector \( \mathbf{v} \in V \), there exists a vector \( \mathbf{w} \in V \) such that \( \mathbf{v} + \mathbf{w} = \mathbf{0} \). Such an additive inverse is usually denoted as \( -\mathbf{v} \);
\end{enumerate}

The next 2 properties concern scalar multiplication:
\begin{enumerate}
    \setcounter{enumi}{4}
    \item Multiplicative identity: \( 1\mathbf{v} = \mathbf{v} \) for all \( \mathbf{v} \in V \);
    \item Multiplicative associativity: \( (\alpha \beta) \mathbf{v} = \alpha (\beta \mathbf{v}) \) for all \( \alpha, \beta \in \mathbb{R} \) and all \( \mathbf{v} \in V \);
\end{enumerate}

And finally, two distributive properties, which connect multiplication and addition:
\begin{enumerate}
    \setcounter{enumi}{6}
    \item Distributivity over vector addition: \( \alpha (\mathbf{u} + \mathbf{v}) = \alpha \mathbf{u} + \alpha \mathbf{v} \) for all \( \alpha \in \mathbb{R} \) and all \( \mathbf{u}, \mathbf{v} \in V \);
    \item Distributivity over scalar addition: \( (\alpha + \beta) \mathbf{v} = \alpha \mathbf{v} + \beta \mathbf{v} \) for all \( \alpha, \beta \in \mathbb{R} \) and all \( \mathbf{v} \in V \).
\end{enumerate}
\end{definition}
\section{Linear combinations, basis}
\begin{definition}[linear combination]
    Let \( V \) be a vector space, and let \( \mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_p \in V \) be a collection of vectors. A \textit{linear combination} of vectors \( \mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_p \) is a sum of form
\[
\alpha_1 \mathbf{v}_1 + \alpha_2 \mathbf{v}_2 + \cdots + \alpha_p \mathbf{v}_p = \sum_{k=1}^{p} \alpha_k \mathbf{v}_k.
\]
\end{definition}
\begin{definition}[basis]
    A system of vectors $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n \in V$ is called a basis (for the vector space $V$) if any vector $\mathbf{v} \in V$ admits a \textit{unique} representation as a linear combination
\[
\mathbf{v} = \alpha_1 \mathbf{v}_1 + \alpha_2 \mathbf{v}_2 + \cdots + \alpha_n \mathbf{v}_n = \sum_{k=1}^{n} \alpha_k \mathbf{v}_k.
\]

The coefficients $\alpha_1, \alpha_2, \ldots, \alpha_n$ are called \textit{coordinates} of the vector $\mathbf{v}$ (in the basis, or with respect to the basis $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n$).

Another way to say that $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n$ is a basis is to say that for any possible choice of the right side $\mathbf{v}$, the equation 
\[
x_1 \mathbf{v}_1 + x_2 \mathbf{v}_2 + \cdots + x_m \mathbf{v}_n = \mathbf{v}
\]
(with unknowns $x_k$) has a unique solution.
\end{definition}
\section{Generating and linearly independent systems}
\begin{definition}[span]
    Let $S \subset V$ be a set. Its \emph{span} in $V$ is
\[
\mathrm{span}(S) := \left\{ \sum_{j=1}^{N} \lambda_j \mathbf{s}_j : N \in \mathbb{N} \text{ and } \mathbf{s}_1, \dots, \mathbf{s}_N \in S \right\}.
\]

That is, the span of $S$ consists of all (finite) linear combinations over elements in $S$.

If vector space $W$ satisfies $W \subset \mathrm{span}(S)$, say "$S$ spans $W$".

\textbf{Thus}, a basis $\mathcal{B}$ for $V$ satisfies (1), $\mathrm{span}(\mathcal{B}) = V$; and (2), each $\mathbf{v} \in V$ can be expressed in a unique way as a linear combination of elements in $\mathcal{B}$.
\end{definition}
\begin{definition}[Generating system]
    A system of vectors $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_p \in V$ is called a generating system (also a \textit{spanning system}, or a \textit{complete system}) in $V$ if any vector $\mathbf{v} \in V$ admits representation as a linear combination
\[
\mathbf{v} = \alpha_1 \mathbf{v}_1 + \alpha_2 \mathbf{v}_2 + \cdots + \alpha_p \mathbf{v}_p = \sum_{k=1}^{p} \alpha_k \mathbf{v}_k.
\]
\end{definition}
\begin{definition}[trivial]
    A linear combination $\alpha_1 \mathbf{v}_1 + \alpha_2 \mathbf{v}_2 + \cdots + \alpha_p \mathbf{v}_p$ is called \textit{trivial} if $\alpha_k = 0 \ \forall k$.
\end{definition}
\begin{definition}[linearly dependent]
    A system of vectors $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_p$ is called \textit{linearly dependent} if $\mathbf{0}$ can be represented as a nontrivial linear combination,
\[
\mathbf{0} = \sum_{k=1}^p \alpha_k \mathbf{v}_k.
\]
Non-trivial here means that at least one of the coefficient $\alpha_k$ is non-zero. This can be (and usually is) written as
\[
\sum_{k=1}^p |\alpha_k| \ne 0.
\]
\end{definition}
\begin{proposition}
    A system of vectors \( \mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_p \in V \) is linearly dependent if and only if one of the vectors \( \mathbf{v}_k \) can be represented as a linear combination of the other vectors,
\[
\mathbf{v}_k = \sum_{\substack{j=1 \\ j \neq k}}^p \beta_j \mathbf{v}_j.
\]
\end{proposition}
Proof omitted. 
\begin{proposition}
    A system of vectors \( \mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n \in V \) is a basis if and only if it is linearly independent and complete (generating).
\end{proposition}
Proof omitted. 
\begin{proposition}
    Any finite generating system contains a basis. 
\end{proposition}
Proof omitted. 
\begin{definition}[dimension]
Let $V$ be a v.s.\ over $K$. Its \emph{dimension} (over $K$) is the number of elements in a basis for $V$.

We denote the dimension of $V$ by $\dim V \equiv \dim_K V$. The subscript $K$ is omitted when there is no confusion of the choice of $K$. Of course, we say that $V$ is a finite-dimensional vector space \emph{(f.d.v.s.)} if $\dim V < \infty$.
\end{definition}
\textbf{\textcolor{black}{Highly nontrivial question:}} Why is this definition of dimension well-defined? That is, why is the number of elements in \textcolor{red}{\emph{every}} basis the same?!
\newpage
\chapter{Linear maps}
\section{Linear transformations}
\begin{definition}[transformation]
    A \textit{transformation} $T$ from a set $X$ to a set $Y$ is a rule that for each argument (input) $x \in X$ assigns a value (output) $y = T(x) \in Y$.

The set $X$ is called the \textit{domain} of $T$, and the set $Y$ is called the \textit{target space} or \textit{codomain} of $T$.

We write $T : X \to Y$ to say that $T$ is a transformation with the domain $X$ and the target space $Y$.
\end{definition}
\begin{definition}[linear transformation]
    Let $V, W$ be vector spaces (over the same field $\mathbb{F}$). A transformation $T : V \to W$ is called linear if
\begin{enumerate}
  \item $T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})$ \quad $\forall\, \mathbf{u}, \mathbf{v} \in V$;
  \item $T(\alpha \mathbf{v}) = \alpha T(\mathbf{v})$ for all $\mathbf{v} \in V$ and for all scalars $\alpha \in \mathbb{F}$.
\end{enumerate}
Properties 1 and 2 together are equivalent to the following one:
\[
T(\alpha \mathbf{u} + \beta \mathbf{v}) = \alpha T(\mathbf{u}) + \beta T(\mathbf{v}) \quad \text{for all } \mathbf{u}, \mathbf{v} \in V \text{ and for all scalars } \alpha, \beta.
\]
\end{definition}
\begin{example}
    Rotation, scaling, and reflection are all examples of linear transformation. 
\end{example}
\section{Linear transformations $\mathbb{F}^n \to \mathbb{F}^m $}

Let $T : \mathbb{F}^n \to \mathbb{F}^m$ be a linear transformation. What information do we need to compute $T(\mathbf{x})$ for all vectors $\mathbf{x} \in \mathbb{F}^n$? 

Claim: it is sufficient to know how $T$ acts on the standard basis $\mathbf{e}_1, \mathbf{e}_2, \ldots, \mathbf{e}_n$ of $\mathbb{F}^n$. Namely, it is sufficient to know $n$ vectors in $\mathbb{F}^m$ (i.e., the vectors of size $m$),

\[
\mathbf{a}_1 = T(\mathbf{e}_1), \quad 
\mathbf{a}_2 := T(\mathbf{e}_2), \quad 
\ldots, \quad 
\mathbf{a}_n := T(\mathbf{e}_n).
\]
Indeed, let
\[
\mathbf{x} = 
\begin{pmatrix}
x_1 \\
x_2 \\
\vdots \\
x_n
\end{pmatrix}.
\]

Then $\mathbf{x} = x_1 \mathbf{e}_1 + x_2 \mathbf{e}_2 + \dots + x_n \mathbf{e}_n = \sum_{k=1}^{n} x_k \mathbf{e}_k$ and
\[
T(\mathbf{x}) = T\left( \sum_{k=1}^{n} x_k \mathbf{e}_k \right) = \sum_{k=1}^{n} T(x_k \mathbf{e}_k) = \sum_{k=1}^{n} x_k T(\mathbf{e}_k) = \sum_{k=1}^{n} x_k \mathbf{a}_k.
\]
\section{Matrix-column multiplication}
As previously discussed, if we join the vectors (columns) $\mathbf{a}_1, \mathbf{a}_2, \ldots, \mathbf{a}_n$ together in a matrix 
$A = [\mathbf{a}_1, \mathbf{a}_2, \ldots, \mathbf{a}_n]$ ($\mathbf{a}_k$ being the $k$th column of $A$, $k = 1, 2, \ldots, n$), this matrix contains all the information about $T$.

Let us show how one should define the product of a matrix and a vector (column) to represent the transformation $T$ as a product, $T(\mathbf{x}) = A\mathbf{x}$. Let
\[
A = 
\begin{pmatrix}
a_{1,1} & a_{1,2} & \cdots & a_{1,n} \\
a_{2,1} & a_{2,2} & \cdots & a_{2,n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m,1} & a_{m,2} & \cdots & a_{m,n}
\end{pmatrix}.
\]

Recall, that the column number $k$ of $A$ is the vector $\mathbf{a}_k$, i.e.
\[
\mathbf{a}_k =
\begin{pmatrix}
a_{1,k} \\
a_{2,k} \\
\vdots \\
a_{m,k}
\end{pmatrix}.
\]

Then if we want $A\mathbf{x} = T(\mathbf{x})$ we get
\[
A\mathbf{x} = \sum_{k=1}^{n} x_k \mathbf{a}_k = 
x_1
\begin{pmatrix}
a_{1,1} \\
a_{2,1} \\
\vdots \\
a_{m,1}
\end{pmatrix}
+
x_2
\begin{pmatrix}
a_{1,2} \\
a_{2,2} \\
\vdots \\
a_{m,2}
\end{pmatrix}
+ \ldots +
x_n
\begin{pmatrix}
a_{1,n} \\
a_{2,n} \\
\vdots \\
a_{m,n}
\end{pmatrix}.
\]
Therefore, the matrix-vector multiplication should be performed by the following column by coordinate rule: \textit{multiply each column of the matrix by the corresponding coordinate of the vector. }
\section{Linear transformation and generating sets}
As previously discussed, linear transformation $T$ (acting from $\mathbb{F}^n$ to $\mathbb{F}^m$) is completely defined by its values on the standard basis in $\mathbb{F}^n$.

The fact that we consider the standard basis is not essential, one can consider any basis, even any generating (spanning) set. Namely,
\[
\boxed{
\parbox{0.85\linewidth}{
A linear transformation $T : V \to W$ is completely defined by its values on a generating set (in particular by its values on a basis).
}
}
\]
\begin{corollary}
    If $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n$ is a generating set (in particular, if it is a basis) in $V$, and $T$ and $T_1$ are linear transformations $T, T_1 : V \to W$ such that
\[
T \mathbf{v}_k = T_1 \mathbf{v}_k, \qquad k = 1, 2, \ldots, n
\]
then $T = T_1$.
\end{corollary}
Proof omitted. 
\section{Linear transformations as a vector space}
We can always multiply a linear transformation for a scalar, i.e., if we have a linear transformation $T : V \to W$ and a scalar $\alpha$, we can define a new transformation $\alpha T$ by
\[
(\alpha T)\mathbf{v} = \alpha (T\mathbf{v}) \qquad \forall\, \mathbf{v} \in V.
\]
It is easy to check that $\alpha T$ is also a linear transformation:
\begin{align*}
(\alpha T)(\alpha_1 \mathbf{v}_1 + \alpha_2 \mathbf{v}_2) 
&= \alpha \left( T(\alpha_1 \mathbf{v}_1 + \alpha_2 \mathbf{v}_2) \right) && \text{by the definition of } \alpha T \\
&= \alpha \left( \alpha_1 T\mathbf{v}_1 + \alpha_2 T\mathbf{v}_2 \right) && \text{by the linearity of } T \\
&= \alpha_1 \alpha T\mathbf{v}_1 + \alpha_2 \alpha T\mathbf{v}_2 
= \alpha_1 (\alpha T)\mathbf{v}_1 + \alpha_2 (\alpha T)\mathbf{v}_2
\end{align*}
If $T_1$ and $T_2$ are linear transformations with the same domain and target space 
($T_1 : V \to W$ and $T_2 : V \to W$, or in short $T_1, T_2 : V \to W$), 
then we can add these transformations, i.e., define a new transformation $T = (T_1 + T_2) : V \to W$ by
\[
(T_1 + T_2)\mathbf{v} = T_1\mathbf{v} + T_2\mathbf{v} \qquad \forall\, \mathbf{v} \in V.
\]
It is easy to check that the transformation $T_1 + T_2$ is also a linear one.

So, if we fix vector spaces $V$ and $W$ and consider the collection of all linear transformations from $V$ to $W$ (let us denote it by $\mathcal{L}(V, W)$), we can define 2 operations on $\mathcal{L}(V, W)$: multiplication by a scalar and addition. 

It can be easily shown that these operations satisfy the axioms of a vector space, defined in the previous discussions. 
\section{Composition of linear transformations and matrix multiplication}
Recalling the row by column rule for matrix-vector multiplication, the definition of matrix multiplication is as follows: 
\begin{definition}
    Let us multiply by $A$ each column of $B$ (matrix-vector multiplication) and join the resulting column-vectors into a matrix. Formally, If \(\mathbf{b}_1, \mathbf{b}_2, \ldots, \mathbf{b}_r\) are the columns of \(B\), then \(A\mathbf{b}_1, A\mathbf{b}_2, \ldots, A\mathbf{b}_r\) are the columns of the matrix \(AB\).
\end{definition}
\begin{remark}
The entry \((AB)_{j,k}\) (the entry in the row \(j\) and column \(k\)) of the product \(AB\) is defined by
\[
(AB)_{j,k} = \text{(row \#} j \text{ of } A) \cdot \text{(column \#} k \text{ of } B)
\]
Formally, it can be rewritten as
\[
(AB)_{j,k} = \sum_{l} a_{j,l} b_{l,k},
\]
\end{remark}
\begin{remark}
In order for the multiplication to be defined, the size of a row of \(A\) should be equal to the size of a column of \(B\).

In other words, the product \(AB\) is defined if and only if \(A\) is an \(m \times n\) matrix and \(B\) is an \(n \times r\) matrix.
\end{remark}
\begin{remark}
    The multiplication of matrices defined above arises naturally from the composition of linear transformations. 
\end{remark}
\textcolor{blue}{Suppose we have two linear transformations, \( T_1 : \mathbb{F}^n \to \mathbb{F}^m \) and \( T_2 : \mathbb{F}^r \to \mathbb{F}^n \). Define the composition \( T = T_1 \circ T_2 \) of the transformations \( T_1, T_2 \) as
\[
T(\mathbf{x}) = T_1(T_2(\mathbf{x})) \qquad \forall \mathbf{x} \in \mathbb{F}^r.
\]}

\textcolor{blue}{Note that \( T_1(\mathbf{x}) \in \mathbb{F}^n \). Since \( T_1 : \mathbb{F}^n \to \mathbb{F}^m \), the expression \( T_1(T_2(\mathbf{x})) \) is well defined and the result belongs to \( \mathbb{F}^m \). Therefore, \( T : \mathbb{F}^r \to \mathbb{F}^m \).}

\textcolor{blue}{Since \( T \) is a linear transformation (proof omitted), it is defined by an \( m \times r \) matrix. How one can find this matrix, knowing the matrices of \( T_1 \) and \( T_2 \)?}

Let \( A \) be the matrix of \( T_1 \) and \( B \) be the matrix of \( T_2 \). As previously discussed, the columns of \( T \) are vectors \( T(\mathbf{e}_1), T(\mathbf{e}_2), \ldots, T(\mathbf{e}_r) \), where \( \mathbf{e}_1, \mathbf{e}_2, \ldots, \mathbf{e}_r \) is the standard basis in \( \mathbb{F}^r \). For \( k = 1, 2, \ldots, r \) we have
\[
T(\mathbf{e}_k) = T_1(T_2(\mathbf{e}_k)) = T_1(B\mathbf{e}_k) = T_1(\mathbf{b}_k) = A\mathbf{b}_k.
\]

So the columns of the matrix of \( T \) are \( A\mathbf{b}_1, A\mathbf{b}_2, \ldots, A\mathbf{b}_r \), and that is exactly how the matrix \( AB \) was defined. 
\begin{remark}
Matrix multiplication has a lot of properties, for example: 
\begin{enumerate}
    \item \textbf{Associativity:} \( A(BC) = (AB)C \), provided that either left or right side is well defined; we therefore can (and will) simply write \( ABC \) in this case.
    
    \item \textbf{Distributivity:} \( A(B + C) = AB + AC, \quad (A + B)C = AC + BC \), provided either left or right side of each equation is well defined.
    
    \item \textbf{One can take scalar multiplies out:} \( A(\alpha B) = (\alpha A)B = \alpha(AB) = \alpha AB \).
\end{enumerate}
\end{remark}
Proof by matching every entry through the row by columns rule. Omitted. 
\section{Transpose}
\begin{definition}[Transpose]
Given a matrix \( A \), its \textit{transpose} (or transposed matrix) \( A^T \) is defined by transforming the rows of \( A \) into the columns.

So the columns of \( A^T \) are the rows of \( A \) and vice versa, the rows of \( A^T \) are the columns of \( A \).

The formal definition is as follows: 
\[
(A^T)_{j,k} = (A)_{k,j}
\]
meaning that the entry of \( A^T \) in the row number \( j \) and column number \( k \) equals the entry of \( A \) in the row number \( k \) and row number \( j \).
\end{definition}
\begin{corollary}
\[(AB)^T = B^T A^T\]
\end{corollary}
Proof omitted. 
\section{Trace}
\begin{definition}[Trace]
For a square \( (n \times n) \) matrix \( A = (a_{j,k}) \), its trace (denoted by \( \mathrm{trace}\, A \)) is the sum of the diagonal entries:
\[
\mathrm{trace}\, A = \sum_{k=1}^{n} a_{k,k}.
\]
\end{definition}
\begin{theorem}
Let \( A \) and \( B \) be matrices of size \( m \times n \) and \( n \times m \) respectively (so both products \( AB \) and \( BA \) are well defined). Then
\[
\mathrm{trace}(AB) = \mathrm{trace}(BA)
\]
\end{theorem}
Proof by calculation. Omitted.
\section{Identity transformation and identity matrices}
\begin{definition}[Identity transformation]
Given a vector space \(V\), the identity transformation is a transformation from \(V\) to itself, such that \[\forall \textbf{x} \in V, I \textbf{x} = \textbf{x}. \]
\end{definition}
\begin{remark}
We will use the notation \( I_V \) when when we want to emphasize in what space the transformation is acting.
\end{remark}
\begin{remark}
Clearly, if \( I : \mathbb{F}^n \to \mathbb{F}^n \) is the identity transformation in \( \mathbb{F}^n \), its matrix is the \( n \times n \) matrix
\[
I = I_n = 
\begin{pmatrix}
1 & 0 & \cdots & 0 \\
0 & 1 & \cdots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \cdots & 1
\end{pmatrix}
\]
(1 on the main diagonal and 0 everywhere else). When we want to emphasize the size of the matrix, we use the notation \( I_n \); otherwise we just use \( I \).
\end{remark}
\begin{remark}
Clearly, for an arbitrary linear transformation \( A \), the equalities
\[
AI = A, \qquad IA = A
\]
hold (whenever the product is defined).
\end{remark}
\section{Invertible transformations and invertible matrices}
\begin{definition}[left invertible and right invertible]
Let \( A : V \to W \) be a linear transformation. We say that the transformation \( A \) is \textit{left invertible} if there exists a linear transformation \( B : W \to V \) such that
\[
BA = I \qquad (I = I_V \text{ here}).
\]
The transformation \( A \) is called \textit{right invertible} if there exists a linear transformation \( C : W \to V \) such that
\[
AC = I \qquad (\text{here } I = I_W).
\]
\end{definition}
\begin{remark}
Note that we did not assume the uniqueness of \(B\) or \(C\) here, and generally left and right inverses are not unique. 
\end{remark}
\begin{definition}[invertible]
A linear transformation \( A : V \to W \) is called \emph{invertible} if it is both right and left invertible.
\end{definition}
\begin{theorem}
If a linear transformation \( A : V \to W \) is invertible, then its left and right inverses \( B \) and \( C \) are unique and coincide.
\end{theorem}
\begin{proof}
A is left invertible implies there exists a map \( B: W \to V \) such that \( BA = I_V \).

A is right invertible implies there exists a map \( C: W \to V \) such that \( AC = I_W \).

Therefore, \( BA = AC = I \).

\textcolor{red}{In fact, here we must have \(I_V = I_W\), which means the two vector spaces \(W\) and \(V\) have the same dimensions. This will be proved later. }

It follows that:
\( BAC = I C = C \),  
and also  
\( BAC = B I = B \).

Hence, \( B = C \).
\end{proof}
\begin{corollary}
A transformation \( A : V \rightarrow W \) is invertible if and only if there exists a unique linear transformation (denoted \( A^{-1} \)),
\[ 
A^{-1}A = I_V, \quad AA^{-1} = I_W. 
\]
The transformation \( A^{-1} \) is called the inverse of \( A \).
\end{corollary}
Proof of the if and only if relation is omitted. 
\begin{definition}[invertible matrix]
A matrix is called \textit{invertible} (resp.\ \textit{left invertible}, \textit{right invertible}) if the corresponding linear transformation is invertible (resp.\ left invertible, right invertible).   
\end{definition}
\begin{remark}
A matrix \(A\) is invertible if there exists a unique matrix \(A^{-1}\) such that \(A^{-1} A = I, A A^{-1} = I\). The matrix \(A^{-1}\) is called the \textit{inverse} of \(A\). 
\end{remark}
\begin{remark}
An invertible matrix must be square (to be proved later). Moreover, if a square matrix has either a left or a right inverse, it is invertible. 
\end{remark}
\begin{corollary}
If linear transformations \(A\) and \(B\) are invertible and the product \(AB\) is defined, then the product \(AB\) is invertible and \[(AB)^{-1} = B^{-1} A^{-1}. \]
\end{corollary}
\begin{proof}
Direct computation shows
\[
(AB)(B^{-1}A^{-1}) = A(BB^{-1})A^{-1} = AIA^{-1} = AA^{-1} = I
\]
and similarly
\[
(B^{-1}A^{-1})(AB) = B^{-1}(A^{-1}A)B = B^{-1}IB = B^{-1}B = I
\]
\end{proof}
\begin{theorem}
The invertibility of \(AB\) does not imply the invertibility of \(A\) and \(B\). But when either \(A\) or \(B\) and \(AB\) are invertible, then the second factor is also invertible. 
\end{theorem}
\begin{proof}
$AB$ is invertible $\Rightarrow \exists C$ such that $ABC = CAB = I$ 

$A$ is invertible $\Rightarrow BC$ is the inverse of $A$ \

$\Rightarrow ABC = BCA = I$ 

Since $CAB = BCA = I$, $CA$ is the inverse of $B$ 

$\Rightarrow B$ is invertible.

For the case of \(B\) being invertible is similar. 
\end{proof}
\begin{theorem}
(Inverse of $A^T$). \textit{If a matrix $A$ is invertible, then $A^T$ is also invertible and}
\[
(A^T)^{-1} = (A^{-1})^T
\]
\end{theorem}
\begin{proof}
\textit{Using $(AB)^T = B^T A^T$ we get}
\[
(A^{-1})^T A^T = (A A^{-1})^T = I^T = I,
\]
\textit{and similarly}
\[
A^T (A^{-1})^T = (A^{-1} A)^T = I^T = I.
\]
\end{proof}
\begin{theorem}
If \(A\) is invertible, then \(A^{-1}\) is also invertible, and \((A^{-1})^{-1} = A\). 
\end{theorem}
Proof omitted. 
\section{Isomorphisms}
An invertible linear transformation \(A: V \to W\) is an isomorphism. 

Two vector spaces \(V\) and \(W\) are isomorphic (denoted \(V \cong W\)) if there is an isomorphism \(A: V \to W\). 

Isomorphic spaces can be considered as different representation of the same space, meaning that all properties and constructions involving vector space operations are preserved under isomorphism. 
\begin{theorem}
Let $A : V \to W$ be an isomorphism, and let $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n$ be a basis in $V$. Then the system $A\mathbf{v}_1, A\mathbf{v}_2, \ldots, A\mathbf{v}_n$ is a basis in $W$.
\end{theorem}
Proof omitted. 
\begin{remark}
In the above theorem we can replace "basis" by "linearly independent", "generating" or "linearly dependent", as all these properties are preserved under isomorphisms. Proof omitted. 
\end{remark}
\begin{remark}
If $A$ is an isomorphism, then so is $A^{-1}$. Therefore, in the above theorem we can state that $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n$ is a basis if and only if $A\mathbf{v}_1, A\mathbf{v}_2, \ldots, A\mathbf{v}_n$ is a basis.
\end{remark}
Proof omitted. 
\begin{theorem}
Let $A : V \to W$ be a linear map, and let $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n$ and $\mathbf{w}_1, \mathbf{w}_2, \ldots, \mathbf{w}_n$ be bases in $V$ and $W$ respectively. If $A\mathbf{v}_k = \mathbf{w}_k$, $k = 1, 2, \ldots, n$, then $A$ is an isomorphism.
\end{theorem}
\begin{proof}
Define the inverse transformation $A^{-1}$ by $A^{-1} \mathbf{w}_k = \mathbf{v}_k$, $k = 1, 2, \ldots, n$ (as we know, a linear transformation is defined by its values on a basis).
\end{proof}
\section{Invertibility and equations}
\begin{theorem}
Let $A : X \rightarrow Y$ be a linear transformation. Then $A$ is invertible if and only if for any right side $\mathbf{b} \in Y$ the equation
\[
A \mathbf{x} = \mathbf{b}
\]
has a unique solution $\mathbf{x} \in X$.
\end{theorem}
\begin{proof}
We offer two proofs here. The first proof is by trying to find a basis \(\{\mathbf{b}_i\}\) in \(W\) and show that the solution set is also a basis in \(V\). Omitted. 

The second proof is from the book. Suppose $A$ is invertible. Then $\mathbf{x} = A^{-1} \mathbf{b}$ solves the equation $A\mathbf{x} = \mathbf{b}$. To show that the solution is unique, suppose that for some other vector $\mathbf{x}_1 \in X$

\[
A\mathbf{x}_1 = \mathbf{b}
\]

Multiplying this identity by $A^{-1}$ from the left we get

\[
A^{-1}A\mathbf{x}_1 = A^{-1}\mathbf{b},
\]

and therefore $\mathbf{x}_1 = A^{-1}\mathbf{b} = \mathbf{x}$. Note that both identities, $AA^{-1} = I$ and $A^{-1}A = I$ were used here.

Let us now suppose that the equation $A\mathbf{x} = \mathbf{b}$ has a unique solution $\mathbf{x}$ for any $\mathbf{b} \in Y$. Let us use symbol $\mathbf{y}$ instead of $\mathbf{b}$. We know that given $\mathbf{y} \in Y$ the equation

\[
A\mathbf{x} = \mathbf{y}
\]

has a unique solution $\mathbf{x} \in X$. Let us call this solution $B(\mathbf{y})$.

Note that $B(\mathbf{y})$ is defined for all $\mathbf{y} \in Y$, so we defined a transformation $B : Y \rightarrow X$.

Let us check that $B$ is a linear transformation. We need to show that $B(\alpha \mathbf{y}_1 + \beta \mathbf{y}_2) = \alpha B(\mathbf{y}_1) + \beta B(\mathbf{y}_2)$. Let $\mathbf{x}_k := B(\mathbf{y}_k),\ k=1,2$, i.e. $A\mathbf{x}_k = \mathbf{y}_k$, $k=1,2$. Then

\[
A(\alpha \mathbf{x}_1 + \beta \mathbf{x}_2) = \alpha A\mathbf{x}_1 + \beta A\mathbf{x}_2 = \alpha \mathbf{y}_1 + \beta \mathbf{y}_2,
\]

which means

\[
B(\alpha \mathbf{y}_1 + \beta \mathbf{y}_2) = \alpha B(\mathbf{y}_1) + \beta B(\mathbf{y}_2).
\]
And finally, let us show that $B$ is indeed the inverse of $A$. Take $\mathbf{x} \in X$ and let $\mathbf{y} = A\mathbf{x}$, so by the definition of $B$ we have $\mathbf{x} = B\mathbf{y}$. Then for all $\mathbf{x} \in X$

\[
BA\mathbf{x} = B\mathbf{y} = \mathbf{x},
\]

so $BA = I$. Similarly, for arbitrary $\mathbf{y} \in Y$ let $\mathbf{x} = B\mathbf{y}$, so $\mathbf{y} = A\mathbf{x}$. Then for all $\mathbf{y} \in Y$

\[
AB\mathbf{y} = A\mathbf{x} = \mathbf{y}
\]

so $AB = I$. 
\end{proof}
\begin{corollary}
An $m \times n$ matrix is invertible if and only if its columns form a basis in $\mathbb{F}^m$.
\end{corollary}
\begin{proof}
\(A\) invertible \(\iff A\) acting on the canonical basis results in another basis. Omitted. 
\end{proof}
\newpage
\chapter{More on vector spaces}
\section{Subspaces}
\begin{definition}[subspace]
A subspace of a vector space $V$ is a non-empty subset $V_0 \subset V$ of $V$ which is closed under the vector addition and multiplication by scalars, i.e.

\begin{enumerate}
    \item If $\mathbf{v} \in V_0$ then $\alpha \mathbf{v} \in V_0$ for all scalars $\alpha$;
    \item For any $\mathbf{u}, \mathbf{v} \in V_0$ the sum $\mathbf{u} + \mathbf{v} \in V_0$;
\end{enumerate}

The conditions 1 and 2 can be replaced by the following one:
\[
\alpha \mathbf{u} + \beta \mathbf{v} \in V_0 \quad \text{for all } \mathbf{u}, \mathbf{v} \in V_0, \text{ and for all scalars } \alpha, \beta.
\]
\end{definition}
\begin{example}
Trivial subspaces of a space $V$, namely $V$ itself and $\{\mathbf{0}\}$ (the subspace consisting only of zero vector). Note that the empty set $\varnothing$ is not a vector space, since it does not contain a zero vector, so it is not a subspace.
\end{example}
With each linear transformation \(A: V \to W\) we can associate the following two subspaces:
\begin{example}
The null space, or kernel of $A$, which is denoted as $\text{Null}\, A$ or $\text{Ker}\, A$ and consists of all vectors $\mathbf{v} \in V$ such that $A\mathbf{v} = \mathbf{0}$
\end{example}
\begin{example}
The range $\text{Ran}\, A$ is defined as the set of all vectors $\mathbf{w} \in W$ which can be represented as $\mathbf{w} = A\mathbf{v}$ for some $\mathbf{v} \in V$.
\end{example}
If \( A \) is a matrix, i.e. \( A : \mathbb{F}^m \to \mathbb{F}^n \), then recalling \emph{column by coordinate} rule of the matrix–vector multiplication, we can see that any vector \( \mathbf{w} \in \mathrm{Ran}\, A \) can be represented as a linear combination of columns of the matrix \( A \). That explains why the term column space (and notation \( \mathrm{Col}\, A \)) is often used for the range of the matrix. So, for a matrix \( A \), the notation \( \mathrm{Col}\, A \) is often used instead of \( \mathrm{Ran}\, A \).
\begin{example}
Given a system of vectors $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_r \in V$ its \textit{linear span} (sometimes called simply \textit{span}) $\mathcal{L}\{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_r\}$ is the collection of all vectors $\mathbf{v} \in V$ that can be represented as a linear combination 
\[
\mathbf{v} = \alpha_1 \mathbf{v}_1 + \alpha_2 \mathbf{v}_2 + \cdots + \alpha_r \mathbf{v}_r
\]
of vectors $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_r$. The notation $\text{span}\{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_r\}$ is also used instead of \\$\mathcal{L}\{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_r\}$.
\end{example}
\section{Direct sums}
Suppose \( V_1, \ldots, V_m \) are subspaces of \( V \). Every element of \( V_1 + \cdots + V_m \) can be written in the form
\[
\mathbf{v}_1 + \cdots + \mathbf{v}_m,
\]
where each \( \mathbf{v}_k \in V_k \).
\begin{definition}[Direct sum, \(\oplus\)]
Suppose $V_1, \dots, V_m$ are subspaces of $V$.
\begin{itemize}
  \item The sum $V_1 + \cdots + V_m$ is called a \textit{direct sum} if each element of $V_1 + \cdots + V_m$ can be written in only one way as a sum $v_1 + \cdots + v_m$, where each $v_k \in V_k$.
  \item If $V_1 + \cdots + V_m$ is a direct sum, then $V_1 \oplus \cdots \oplus V_m$ denotes $V_1 + \cdots + V_m$, with the $\oplus$ notation serving as an indication that this is a direct sum.
\end{itemize}
\end{definition}
\begin{corollary}
Suppose \( V_1, \ldots, V_m \) are subspaces of \( V \). Then \( V_1 + \cdots + V_m \) is a direct sum if and only if the only way to write \( \mathbf{0} \) as a sum \( v_1 + \cdots + v_m \), where each \( v_k \in V_k \), is by taking each \( v_k \) equal to \( \mathbf{0} \).
\end{corollary}
\begin{proof}
\begin{itemize}
    \item Suppose \( V_1 + \cdots + V_m \) is a direct sum. Then there is only one way of representing \(\mathbf{0} \in V_1 + \cdots + V_m\). Since taking each \( v_k \) equal to \( 0 \) gives \(\mathbf{0}\), this is the only way to write \(\mathbf{0}\).
    \item Suppose the only way to write \( 0 \) as a sum \( v_1 + \cdots + v_m \), where each \( v_k \in V_k \), is by taking each \( v_k \) equal to \( \mathbf{0} \). We want to show that each element in \( V_1 + \cdots + V_m \) can be represented in only one way. Suppose \(\mathbf{x} \in V_1 + \cdots + V_m\) can be represented in two ways \( v_1 + \cdots + v_m \) and \( u_1 + \cdots + u_m \), then \(\mathbf{0}\) can also be represented as \( (v_1 - u_1) + \cdots + (v_m - u_m) \). Contradiction.
\end{itemize}
\end{proof}
\begin{corollary}
Suppose \( U \) and \( W \) are subspaces of \( V \). Then
\[
U + W \text{ is a direct sum} \iff U \cap W = \{0\}.
\]
\end{corollary}
\begin{proof}
\begin{itemize}
    \item Suppose \(U \cap W = \{0\}\). Then \(\mathbf{0}\) has only one representation, which is \(\mathbf{0} + \mathbf{0}\). 
    \item Suppose \(U + W\) is a direct sum. Let \(\mathbf{v} \in U \cap W\). Since \(\mathbf{v} \in U + W\), \(\mathbf{v}\) has only one representation. Let \(\mathbf{v} = \mathbf{x}+\mathbf{y}\) where \(\mathbf{x} \in U\) and \(\mathbf{y} \in W\). Then \(\mathbf{v} = \mathbf{y}+\mathbf{x}\) which implies \(\mathbf{x} = \mathbf{y}.\) By property of vector spaces, \(\mathbf{v} = 2\mathbf{x} = \frac{1}{2} \mathbf{x} + \frac{3}{2} \mathbf{x}\). However, there should be only one representation of \(\mathbf{v}\), which means \(\mathbf{x} = \mathbf{0}\), therefore \(\mathbf{v} = \mathbf{0}\) \(\Rightarrow\) \(U \cap W = \{\mathbf{0}\}\). 
\end{itemize}
\end{proof}
\section{Products of vector spaces}
\begin{definition}[Products of vector spaces]
Suppose \( V_1, \ldots, V_m \) are vector spaces over \( \mathbb{F} \).
\begin{itemize}
  \item The \textit{product} \( V_1 \times \cdots \times V_m \) is defined by
  \[
  V_1 \times \cdots \times V_m = \{ (v_1, \ldots, v_m) : v_1 \in V_1, \ldots, v_m \in V_m \}.
  \]
  
  \item Addition on \( V_1 \times \cdots \times V_m \) is defined by
  \[
  (u_1, \ldots, u_m) + (v_1, \ldots, v_m) = (u_1 + v_1, \ldots, u_m + v_m).
  \]
  
  \item Scalar multiplication on \( V_1 \times \cdots \times V_m \) is defined by
  \[
  \lambda (v_1, \ldots, v_m) = (\lambda v_1, \ldots, \lambda v_m).
  \]
\end{itemize}
\end{definition}
\begin{corollary}
Product of vector spaces is a vector space. 
\end{corollary}
Proof omitted. 
\begin{corollary}
Suppose \( V_1, \ldots, V_m \) are finite-dimensional vector spaces. Then \( V_1 \times \cdots \times V_m \) is finite-dimensional and
\[
\dim(V_1 \times \cdots \times V_m) = \dim V_1 + \cdots + \dim V_m.
\]
\end{corollary}
\begin{proof}
Suppose \(\{\mathbf{v}_i^1, ..., \mathbf{v}_i^{k_i}\}\) is a basis for \(V_i\) for each \(i = 1, 2, ..., m\). Let \(S =\)
\[\{(\mathbf{v}_1^1, 0, ..., 0), (\mathbf{v}_1^2, 0, ..., 0), ..., (\mathbf{v}_1^{k_1}, 0, ..., 0), \]
\[(0, \mathbf{v}_2^1, 0, ..., 0), (0, \mathbf{v}_2^2, 0, ..., 0), ..., (0, \mathbf{v}_2^{k_2}, 0, ..., 0)\]
\[\cdots \]
\[(0, ..., 0, \mathbf{v}_m^1), (0, ..., 0, \mathbf{v}_m^2), ..., (0, ..., 0, \mathbf{v}_m^{k_m})\}.\]
Since each vector in \(V_1 \times \cdots \times V_m\) can be written as a linear combination of vectors in \(S\) (proof omitted), and vectors in \(S\) are linearly independent (proof omitted), \(S\) is a basis for \(V_1 \times \cdots \times V_m\). Therefore \(\dim (V_1 \times \cdots \times V_m) = |S| = \sum_{i = 1}^m \dim V_i\). 
\end{proof}
\section{Quotients of vector spaces}
\begin{definition}[Notation \(\mathbf{v}+ U\)]
Suppose \( v \in V \) and \( U \subseteq V \). Then \( v + U \) is the subset of \( V \) defined by
\[
v + U = \{ v + u : u \in U \}.
\]
\end{definition}
\begin{definition}[Translate]
For \( v \in V \) and \( U \) a subset of \( V \), the set \( v + U \) is said to be a \textit{translate} of \( U \).
\end{definition}
\begin{definition}[Quotient space]
Suppose \( U \) is a subspace of \( V \). Then the \emph{quotient space} \( V/U \) is the set of all translates of \( U \). Thus
\[
V/U = \{ v + U : v \in V \}.
\]
\end{definition}
\begin{corollary}[Two translates of a subspace are either equal or disjoint]
Suppose \( U \) is a subspace of \( V \) and \( v, w \in V \). Then
\[
v - w \in U 
\iff 
v + U = w + U 
\iff 
(v + U) \cap (w + U) \neq \emptyset.
\]
\end{corollary}
\begin{proof}
Suppose \(\mathbf{v} - \mathbf{w} \in U\). Then \(\mathbf{v} + U = \mathbf{w} + U \) (proof omitted). Suppose \(\mathbf{v} - \mathbf{w} \notin U\), assume \(\mathbf{x} \in (\mathbf{v}+U) \cap (\mathbf{w}+U)\). Then \(\mathbf{x} = \mathbf{v}+\mathbf{u}_1 = \mathbf{w}+\mathbf{u}_2\) for some \(\mathbf{u}_1\), \(\mathbf{u}_2 \in U\). Then \(\mathbf{v} - \mathbf{w} \in U\), contradiction \(\Rightarrow \) \((\mathbf{v}+U) \cap (\mathbf{w}+U)\) is empty. 
\end{proof}
\begin{definition}[Addition and multiplication on \(V/U\)]
Suppose \( U \) is a subspace of \( V \). Then \emph{addition} and \emph{scalar multiplication} are defined on \( V/U \) by
\[
(v + U) + (w + U) = (v + w) + U
\]
\[
\lambda (v + U) = (\lambda v) + U
\]
for all \( v, w \in V \) and all \( \lambda \in \mathbb{F} \).
\end{definition}
\begin{corollary}
The quotient space \( V/U \) is a vector space.
\end{corollary}
Note that the zero element in \(V/U\) is \(U\). The eight properties are easy to check. Proof omitted. 
\begin{definition}
Suppose \(U\) is a subspace of \(V\). The quotient map
\[\pi: V/U\]
is the linear map defined by 
\[\pi (\mathbf{v}) = \mathbf{v} + U\]
for each \(\mathbf{v} \in V\). 
\end{definition}
\begin{theorem}[Dimension of a quotient space]
Suppose \( V \) is finite-dimensional and \( U \) is a subspace of \( V \). Then
\[
\dim V/U = \dim V - \dim U.
\]
\end{theorem}
\begin{proof}
Suppose \(\{\mathbf{u}_1, \cdots \mathbf{u}_m\}\) is a basis for \(U\). Then \(\dim U = m\). Since this is also a set of linearly independent vectors in \(V\), we can extend it into a basis \(\{\mathbf{u}_1, \cdots \mathbf{u}_m, \mathbf{v}_1, \cdots \mathbf{v}_n\}\) for \(V\). Then \(\dim V = m+n\). 

Pick an arbitrary \(\mathbf{v} + U\) in \(V/U\). Since \(\mathbf{v} \in V\), there exists \(x_1, ..., x_{m+n} \in \mathbb{F}\), such that \(\mathbf{v} = \sum_{i = 1}^m x_i \mathbf{u}_i + \sum_{j = m +1}^n x_j \mathbf{v}_{j-m}\). Therefore, \(\mathbf{v}+U = \sum_{j = m + 1}^n x_j \mathbf{v}_{j-m}+U\). Therefore, \(\{\mathbf{v}_1 + U, ..., \mathbf{v}_n + U\}\) spans \(V/U\). 

Suppose \(\mathbf{v}+U\) has a new linear combination \(\mathbf{v}+U = \sum_{j = m + 1}^n y_j \mathbf{v}_{j-m}+U\). Then \(\sum_{j = m+1}^n (y_j - x_j)(\mathbf{v}_{j-m} + U)\) is the zero element in \(V/U\) which is \(U\), which means \(\sum_{j = m+1}^n (y_j - x_j) \mathbf{v}_{j-m} \in U\). Therefore, \(y_j = x_j\) for all \(j\), and for an arbitrary \(\mathbf{v}+U\) it can have only one linear combination. \(\Rightarrow\) \(\dim (V/U) = \dim V - \dim U\). 
\end{proof}
\begin{definition}[Notation: \(\widetilde{T}\)]
Suppose \( T \in \mathcal{L}(V, W) \). Define \( \widetilde{T} : V / (\text{null } T) \to W \) by
\[
\widetilde{T}(v + \text{null } T) = Tv.
\]
\end{definition}
\begin{theorem}[Null space and range of \(\widetilde{T}\)]
Suppose \(T \in \mathcal{L}(V, W)\). Then
\begin{itemize}
    \item \(\widetilde{T} \circ \pi = T, \text{ where } \pi \text{ is the quotient map of } V \text{ onto } V / (\text{null } T);\)
    \item \(\widetilde{T} \text{ is injective;}\)
    \item \(\text{range } \widetilde{T} = \text{range } T;\)
    \item \(V / (\text{null } T) \text{ and range } T \text{ are isomorphic vector spaces.}\)
\end{itemize}  
\end{theorem}
\begin{proof}
\begin{itemize}
    \item \(\forall \mathbf{v}\) in \(V\), \(\pi \mathbf{v} = \mathbf{v} + \ker T\); \(\widetilde{T} (\mathbf{v} + \ker T) = T \mathbf{v}\).
    \item Suppose \(\widetilde{T} \mathbf{x} + \ker T = \widetilde{T} \mathbf{y} + \ker T\), then \(\mathbf{x} - \mathbf{y} \in \ker T\), which means \(\mathbf{x} + \ker T = \mathbf{y} + \ker T\).
    \item We need to show inclusion from both directions. 
    
    Suppose \(\mathbf{y} \in \operatorname{range} T\), then there exists \(\mathbf{x}\) in \(V\), such that \(T \mathbf{x} = \mathbf{y}\). Then \(\widetilde{T} \mathbf{x} + \ker T = T \mathbf{x} = \mathbf{y}\), which means \(\mathbf{y}\) is also in \(\operatorname{range} \widetilde{T}\). So \(\operatorname{range} T \subset \operatorname{\widetilde{T}}\). 

    Suppose \(\mathbf{y} \in \operatorname{range} \widetilde{T}\), then there exists \(\mathbf{x}\) in \(V\), such that \(\widetilde{T} \mathbf{x} + \ker T = \mathbf{y}\). Therefore \(T \mathbf{x} = \mathbf{y}\), and \(\operatorname{range} \widetilde{T} \subset \operatorname{T}\). 
    \item For any \(\mathbf{v}+\ker T\) in \(V/ \operatorname{null} T\), \(\widetilde{T} (\mathbf{v}+\ker T) = T \mathbf{v}\) in \(\operatorname{range} T\). Therefore, 
    \[\widetilde{T}: V/\ker T \to \operatorname{range} T\]
    is surjective for \(\operatorname{range} T\). Since \(\widetilde{T}\) is also injective (proved in the previous steps), \(\widetilde{T}\) is an isomorphism. 
\end{itemize}
\end{proof}
\section{Linear transformation as a vector space, revisited}
\begin{theorem}
Suppose $v_1, \ldots, v_n$ is a basis of $V$ and $w_1, \ldots, w_m$ is a basis of $W$. Then $\mathcal{M}$ is an isomorphism between $\mathcal{L}(V, W)$ and $\mathbb{F}^{m,n}$.
\end{theorem}
\begin{proof}
Suppose \(T: V \to W\). Since \(T\) can be determined completely on how it acts on a basis for \(V\), if \(T \mathbf{v}_1, ..., T\mathbf{v}_n\) are determined, then \(T\) is determined. Since each \(T \mathbf{v}_i \in W\), there exists a unique linear combination of \(\mathbf{w}_1, ..., \mathbf{w}_m\) for each \(T \mathbf{v}_i \in W\). Denote each \(T \mathbf{v}_i\) as 
\[T \mathbf{v}_i = \sum_{j = 1}^m a_{ij} \mathbf{w}_j,\]
we can see that the linear transformation \(T\) is completely determined by the \(m \times n\) coefficients \(a_{ij}\). Define \(\mathcal{M} (T) = \{a_{ij}\}_{i,j}\), then \(\mathcal{M}\) is both injective and surjective (proof omitted). 
\end{proof}
\begin{theorem}
Suppose $V$ and $W$ are finite-dimensional. Then $\mathcal{L}(V, W)$ is finite-dimensional and
\[
\dim \mathcal{L}(V, W) = (\dim V)(\dim W).
\]
\end{theorem}
\begin{proof}
Define \(T_{ij}\) as the linear transformation that maps \(\mathbf{v}_i\) to \(\mathbf{w}_j\), and maps all other \(\mathbf{v}_k\) to \(\mathbf{0}\). Define \(S = \{T_{ij}: i = 1, ..., n; j = 1, ..., m\}\). Then \(S\) is a basis for \(\mathcal{L}(V, W)\). Proof omitted. 
\end{proof}
\newpage
\chapter{Systems of linear equations}
\section{Linear systems}
The naive linear system is a collection of $m$ linear equations with $n$ unknowns $x_1, x_2, \ldots, x_n$,
\[
\left\{
\begin{aligned}
a_{1,1}x_1 &+ a_{1,2}x_2 + \cdots + a_{1,n}x_n &= b_1 \\
a_{2,1}x_1 &+ a_{2,2}x_2 + \cdots + a_{2,n}x_n &= b_2 \\
&\vdots \\
a_{m,1}x_1 &+ a_{m,2}x_2 + \cdots + a_{m,n}x_n &= b_m
\end{aligned}
\right.
\]
To solve the system is to find \textit{all} $n$-tuples of numbers $x_1, x_2, \ldots, x_n$ which satisfy all $m$ equations simultaneously.

If we denote $\mathbf{x} := (x_1, x_2, \ldots, x_n)^T \in \mathbb{F}^n$, $\mathbf{b} = (b_1, b_2, \ldots, b_m)^T \in \mathbb{F}^m$, and
\[
A = 
\begin{pmatrix}
a_{1,1} & a_{1,2} & \cdots & a_{1,n} \\
a_{2,1} & a_{2,2} & \cdots & a_{2,n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m,1} & a_{m,2} & \cdots & a_{m,n}
\end{pmatrix},
\]

then the above linear system can be written in the \textit{matrix form} (as a \textit{matrix-vector equation})
\[
A\mathbf{x} = \mathbf{b}.
\]
To solve the above equation is to find all vectors $\mathbf{x} \in \mathbb{F}^n$ satisfying $A\mathbf{x} = \mathbf{b}$.

Hence, all the information we need is contained in the following matrix
\[
\left(
\begin{array}{cccc|c}
a_{1,1} & a_{1,2} & \cdots & a_{1,n} & b_1 \\
a_{2,1} & a_{2,2} & \cdots & a_{2,n} & b_2 \\
\vdots  & \vdots  & \ddots & \vdots  & \vdots \\
a_{m,1} & a_{m,2} & \cdots & a_{m,n} & b_m
\end{array}
\right)
\]
which is obtained by attaching the column $\mathbf{b}$ to the matrix $A$. This matrix is called the \textit{augmented matrix} of the system. We will usually put the vertical line separating $A$ and $\mathbf{b}$ to distinguish between the augmented matrix and the coefficient matrix.
\section{Gauss--Jordan elimination}
Linear system are solved by the \textit{Gauss--Jordan elimination} (which is sometimes called \textit{row reduction}). By performing operations on rows of the augmented matrix of the system (i.e.\ on the equations), we reduce it to a simple form, the so-called \textit{echelon form}. When the system is in the \textit{echelon form}, one can easily write the solution.

\textbf{Row operations:} There are three types of row operations we use:
\begin{enumerate}
  \item Row exchange: interchange two rows of the matrix;
  \item Scaling: multiply a row by a non-zero scalar $a$;
  \item Row replacement: replace a row \# $k$ by its sum with a constant multiple of a row \# $j$; all other rows remain intact;
\end{enumerate}
We can see that the three types of row operations don't change the solution space. 
\section{Row operations and multiplication by elementary matrices}
Every row operation is equivalent to the multiplication of the matrix from the left by one of the special elementary matrices:
\begin{enumerate}
  \item Row exchange: 
  \[
\text{Multiplication by the matrix}
\qquad
\begin{array}{c@{}c@{}c}
  \begin{array}{c} \\ j \\ \\ \\ k \\ \\ \end{array} &
  \left(
  \begin{array}{ccccccc}
    1 &        &        &        &        &        &        \\
      & \ddots &        &        &        &        &        \\
      &        & 1      &        &        &        &        \\
    \cdots & \cdots & \cdots & 0      & \cdots & 1 & \cdots \\
      &        &        &        & 1      &        &        \\
      &        &        & \cdots & \cdots & \cdots & \cdots \\
    \cdots & \cdots & \cdots & 1      & \cdots & 0 & 0 \\
      &        &        &        &        & 1      &        \\
      &        &        &        &        &        & \ddots \\
      &        &        &        &        &        & 1 \\
  \end{array}
  \right)
\end{array}
\]
interchanges the rows number \(j\) and number \(k\).
  \item Scaling: 
Multiplication by the matrix \[
k \begin{pmatrix}
1 & & & & & & 0 \\
& \ddots & & & & & \vdots \\
& & 1 & 0 & & & \vdots \\
& & 0 & a & 0 & & \vdots \\
& & & 0 & 1 & & \vdots \\
& & & & & \ddots & 0 \\
0 & \cdots & \cdots & \cdots & \cdots & 0 & 1
\end{pmatrix} \]
multiplies the row number \(k\) by \(a\). 
  \item Row replacement: 
Multiplication by the matrix
\[
\begin{pmatrix}
1 & \cdots & \cdots & & & 0 \\
\vdots & \ddots & \vdots & & & \vdots \\
\cdots & \cdots & 1 & \cdots & 0 & \cdots \\
\cdots & \cdots & \vdots & \ddots & \vdots \\
\cdots & \cdots & a & \cdots & 1 & \cdots \\
0 & & & & & \ddots \\
0 & & & \cdots & & 1
\end{pmatrix}
\]
adds to the row \# $k$ row \# $j$ multiplied by $a$, and leaves all other rows intact.
\end{enumerate}
Note that all these matrices are invertible, as their corresponding row operations are reversible. 

Therefore, performing a row operation on the augmented matrix of the system \(A\mathbf{x} = \mathbf{b}\) is equivalent to the multiplication of the system (from the left) by a special invertible matrix \(E\). Then any solution of the equation \[A\mathbf{x} = \mathbf{b}\] is also a solution of \[EA\mathbf{x} = E\mathbf{b}.\]
\section{Row reduction}
\textbf{Row reduction:} The main step of row reduction consists of three sub-steps:
\begin{enumerate}
    \item Find the leftmost non-zero column of the matrix;
    \item Make sure, by applying row operations of type 1 (row exchange), if necessary, that the first (the upper) entry of this column is non-zero. This entry will be called the \textit{pivot entry} or simply the \textit{pivot};
    \item ``Kill'' (i.e.\ make them 0) all non-zero entries below the pivot by adding (subtracting) an appropriate multiple of the first row from the rows number $2, 3, \ldots, m$.
\end{enumerate}
After applying the main step to a matrix, we leave the first row alone and apply the main steps to rows 2, 3, ..., \(m\), then we leave the second row alone and apply the main steps to rows 3, 4, ..., \(m\), etc. 

We will get an upper triangular matrix after row reduction, then the solution set will become evident through back substitution. 

Another method: Instead of using back substitution, we can do row reduction from bottom to top, killing all the entries above the main diagonal of the coefficient matrix.
\section{Echelon and reduced echelon forms}
\textbf{Echelon form:} A matrix is in \textit{echelon form} if it satisfies the following two conditions:
\begin{enumerate}
    \item All zero rows (i.e.\ the rows with all entries equal 0), if any, are below all non-zero entries.
\end{enumerate}
For a non-zero row, let us call the leftmost non-zero entry the \textit{leading entry}.
Then the second property of the echelon form can be formulated as follows:
\begin{enumerate}
    \setcounter{enumi}{1}
    \item For any non-zero row its leading entry is strictly to the right of the leading entry in the previous row.
\end{enumerate}
The leading entry in each row in echelon form is also called \textit{pivot entry}, or simply \textit{pivot}, because these entries are exactly the \textit{pivots} we used in the row reduction.
\begin{example}
A particular case of the echelon form is the so-called \textit{triangular} form. In this form the coefficient matrix is square \((n \times n)\), all its entries on the main diagonal are non-zero, and all the entries below the main diagonal are zero. 
\end{example}
\textbf{Reduced echelon form:} A matrix is in the \textit{reduced echelon form}, if it is in the echelon form and
\begin{enumerate}
    \setcounter{enumi}{2}
    \item All pivot entries are equal 1;
    \item All entries above the pivots are 0. Note, that all entries below the pivots are also 0 because of the echelon form.
\end{enumerate}
\begin{remark}
Note that if we kill all entries above the pivots, we won't be able to kill all the entries above the non-zero entries which are non-pivots. If that happens it is pure coincidence. 
\end{remark}
To get reduced echelon form from echelon form, we work from the bottom to the top and from the right to the left, using backward row reduction to kill all entries above the pivots. 

An example of the reduced echelon form is the system with the coefficient matrix equal $I$. In this case, one just reads the solution from the reduced echelon form. In general case, one can also easily read the solution from the reduced echelon form. For example, let the reduced echelon form of the system (augmented matrix) be
\[
\left(
\begin{array}{cccccc|c}
\boxed{1} & 2 & 0 & 0 & 0 & 0 & 1 \\
0 & 0 & \boxed{1} & 5 & 0 & 0 & 2 \\
0 & 0 & 0 & 0 & 0 & \boxed{1} & 3
\end{array}
\right);
\]
here we boxed the pivots. The idea is to move the variables, corresponding to the columns without pivot (the so-called \textit{free variables}) to the right side. Then we can just write the solution.
\[
\left\{
\begin{array}{l}
x_1 = 1 - 2x_2 \\
x_2 \text{ is free} \\
x_3 = 2 - 5x_4 \\
x_4 \text{ is free} \\
x_5 = 3
\end{array}
\right.
\]
\section{Pivots}
All questions about existence of a solution and its uniqueness can be answered by analyzing pivots in the echelon (reduced echelon) form of the augmented matrix of the system.

\textbf{Question:} when is the equation \(A \mathbf{x} = \mathbf{b}\) inconsistent, i.e., when it does not have a solution?

\textbf{A:} a system is inconsistent (does not have a solution) if and only if an echelon form of the augmented matrix has a row \( (\, 0 \quad 0 \quad \dots \quad 0 \mid b\,) \), \( b \ne 0 \) in it.

\textcolor{red}{Therefore, if the system is consistent, i.e., it has at least one solution, either the \textit{reduced echelon form} of the \textit{coefficient matrix} has a pivot in every row, or all the zero rows of the reduced echelon form of the coefficient matrix are matched with zeros}.

If the system has a solution and it is unique, it means there are no free variables. \textcolor{blue}{Recall that a system of linear equations has free variables if and only if there are non-pivot non-zero entries of the \textit{reduced echelon form} of the \textit{coefficient matrix}.} 

Therefore, we reach the following conclusion:
\begin{enumerate}
    \item If the reduced echelon form of the coefficient matrix has at least one row \( (\, 0 \quad 0 \quad \dots \quad 0 \mid b\,) \), \( b \ne 0 \) in it, then the linear system has no solution. 
    \item If the reduced echelon form of the coefficient matrix has a pivot in every row, it must have solution/solutions. 
    \item If the reduced echelon form of the coefficient matrix has a pivot in every row and a pivot in every column, then it has a unique solution. 
\end{enumerate}
\section{Column vectors and pivots}
Let us have a system of vectors $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m \in \mathbb{F}^n$, and let $A = [\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m]$ be an $n \times m$ matrix with columns $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m$. Then we have the following three corollaries: 
\begin{corollary}
The system $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m$ is linearly independent iff the echelon form of $A$ has a pivot in every column.
\end{corollary}
\begin{proof}
\begin{enumerate}
    \item Since $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m$ is linearly independent, \(span\{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m\}\) is a subspace of \(\mathbb{F}^n\), and the set of column vectors form a basis in that subspace. \(A\mathbf{x}\) is a linear combination of the column vectors, therefore \(A\mathbf{x} \in span\{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m\}\). If \(\mathbf{b} \in span\{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m\}\), the system has a unique solution; if not, the system has no solution. 

    For the above two scenarios, if the system has a unique solution, then there is a pivot in every column. If the system has no solution, then there is at least one row in the reduced echelon form of the coefficient matrix in the form \( (\, 0 \quad 0 \quad \dots \quad 0 \mid b\,) \), \( b \ne 0 \). We make the \(b\)'s to be zeros so that the system again has a unique solution (note that this won't change the reduced echelon form of the coefficient matrix). 

    Therefore, in conclusion, the reduced echelon form of the coefficient matrix has a pivot in every column. 

    \item Proof from the book: The system $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m \in \mathbb{F}^n$ is linearly independent if and only if the equation
    \[
    x_1 \mathbf{v}_1 + x_2 \mathbf{v}_2 + \cdots + x_m \mathbf{v}_m = \mathbf{0}
    \]
    has the unique (trivial) solution $x_1 = x_2 = \cdots = x_m = 0$, or equivalently, the equation $A\mathbf{x} = \mathbf{0}$ has unique solution $\mathbf{x} = \mathbf{0}$. By the above statements, it happens if and only if there is a pivot in every column of the matrix.
\end{enumerate}
\end{proof}
\begin{corollary}
The system $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m$ is complete in $\mathbb{F}^n$ (spanning, generating) iff the echelon form of $A$ has a pivot in every row. 
\end{corollary}
\begin{proof}
The column vectors are spanning so the system always has a solution/solutions. Therefore, there are no all-zero rows in the reduced echelon form of the coefficient matrix with corresponding \(b \neq 0\). Therefore, by the above analysis, there is one pivot in every column. 
\end{proof}
\begin{corollary}
The system $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m$ is a basis in $\mathbb{F}^n$ iff the echelon form of $A$ has a pivot in every column and in every row.
\end{corollary}
\begin{proof}
The column vectors form a basis in \(\mathbb{F}^n\) (note that we have \(m = n\) here) so the system has a unique solution. By our previous discussions, the reduced echelon form of the coefficient matrix has a pivot in every row and a pivot in every column. 
\end{proof}
\section{Relationships among column vectors and their implications}
The following corollaries are on linear independence:
\begin{corollary}
Any linearly independent system of vectors in \(\mathbb{F}^n\) cannot have more than \(n\) vectors in it.
\end{corollary}
\begin{proof}
Let a system $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m \in \mathbb{F}^n$ be linearly independent, and let $A = [\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m]$ be the $n \times m$ matrix with columns $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m$. By our previous discussion, echelon form of $A$ must have a pivot in every column, which is impossible if $m > n$ (number of pivots cannot be more than number of rows).
\end{proof}
\begin{corollary}
Any basis in \(\mathbb{F}^n\) must have exactly \(n\) vectors in it. 
\end{corollary}
\begin{proof}
Let \( \mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m \) be a basis in \( \mathbb{F}^n \) and let \( A \) be the \( n \times m \) matrix with columns \( \mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m \). The fact that the system is a basis means that the equation
\[
A\mathbf{x} = \mathbf{b}
\]
has a unique solution for any (all possible) right side \( b \). The existence means that there is a pivot in every row (of a reduced echelon form of the matrix), hence the number of pivots is exactly \( n \). The uniqueness means that there is a pivot in every column of the coefficient matrix (its echelon form), so
\[
m = \text{number of columns} = \text{number of pivots} = n
\]
\end{proof}
\begin{corollary}
Any spanning (generating) set in \(\mathbb{F}^n\) must have at least \(n\) vectors.
\end{corollary}
\begin{proof}
Let \( \mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m \) be a spanning system in \( \mathbb{F}^n \) and let \( A \) be the \( n \times m \) matrix with columns \( \mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m \). Therefore, \(A\mathbf{x} = \mathbf{b}\) must have a solution \(\Rightarrow A\) has a pivot in every row. Since number of pivots cannot exceed the number of columns, we have \(n \leq m\). 
\end{proof}
\section{Corollaries about invertible matrices}
The following corollaries concern invertible matrices:
\begin{corollary}
A matrix \(A\) is invertible if and only if its echelon form has pivot in every column and every row. 
\end{corollary}
\begin{proof}
Recall that \(A\) is invertible if there exists a matrix \(A^{-1}\) which is both the left inverse and right inverse of \(A\). 

Suppose \(A\) is invertible, then for any \(\mathbf{b}\) in the image space, its corresponding solution should be equal to \(A^{-1} \mathbf{b}\). Therefore, \(A\) invertible implies that \(A\mathbf{x} = \mathbf{b}\) always has a solution for any \(\mathbf{b}\). Therefore, by previous discussions, the reduced echelon form of \(A\) has a pivot in every row. By invertibility of \(A\), the solution is unique, but if \(A\) has more columns than the number of pivots, there would be multiple solutions, contradiction. Therefore, \(A_e\), the reduced echelon form of \(A\) has pivot in every column and every row. 

Suppose the reduced echelon form of \(A\) has a pivot in every row and every column. Then \(A\) is a square matrix and \(A\mathbf{x} = \mathbf{b}\) always has a unique solution. By our previous discussion, \(A\) is invertible if and only if \(A\mathbf{x} = \mathbf{b}\) always has a unique solution. Therefore \(A\) is invertible. 
\end{proof}
This result gives an immediate consequence:
\begin{corollary}
An invertible matrix must be square.
\end{corollary}
Proof omitted. 
\begin{corollary}
If a square \( (n \times n) \) matrix is left invertible, or if it is right invertible, then it is invertible. In other words, to check the invertibility of a square matrix \( A \) it is sufficient to check only one of the conditions \( AA^{-1} = I \), \( A^{-1}A = I \).
\end{corollary}
\begin{proof}
We go through some general argument first: 

Suppose \(A\) is not invertible, and \(A\) has a left inverse \(L\).
\begin{enumerate}
    \item Suppose \(A\mathbf{x} = \mathbf{b}\) has no solution. 

    Let \( \mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m \) be column vectors in \(A\), then span\(\{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m\}\) does not include \(\mathbf{b}\). \textcolor{blue}{In this case, even if we let \(\mathbf{x} = L \mathbf{b}\), \(A L \mathbf{b}\) is still a linear combination of the column vectors of \(A\), so it is not equal to \(\mathbf{b}\)}. 

    An example is as follows:
    \[
    \text{Let } A = \begin{bmatrix} 1 & 0 \\ 0 & 0 \\ 0 & 0 \end{bmatrix}, \quad \mathbf{b} = \begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix}
    \]
    Then \( A\mathbf{x} = \mathbf{b} \) has no solution.
    \[
    L = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \end{bmatrix} \text{ is a left inverse of } A
    \]
    However,
    \[
    L \mathbf{b} = \begin{bmatrix} 1 \\ 2 \end{bmatrix} \text{ is not a solution of } A\mathbf{x} = \mathbf{b}.
    \]
    
    \item Suppose \(A\mathbf{x} = \mathbf{b}\) has multiple solutions. 

    Let \(\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m\) be column vectors in \(A\), then span\(\{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m\}\) include \(\mathbf{b}\), and \(\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m\) are linearly dependent. Note that the span may not cover the entire domain. 
    
    \textcolor{red}{In this case, \(A\) has not left inverse}. Prove by contradiction: Assume \(L\) is the left inverse of \(A\), then take two different solutions of \(A\mathbf{x} = \mathbf{b}\), namely, \(\mathbf{x}\) and \(\mathbf{y}\). Then \(A \mathbf{x} - A \mathbf{y} = \vec{0}\) and \(\mathbf{x} - \mathbf{y} \neq \vec{0}\). Therefore, \(LA (\mathbf{x} - \mathbf{y}) = \mathbf{x} - \mathbf{y}\). However, \(L \vec{0} = \vec{0}\), contradiction. 

    There is a theoretical approach to explain this fact. Assume \(A\) has linearly dependent column vectors and \(L\) is its left inverse. Suppose \(\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_m\) are column vectors of \(A\), then there exists \(c_1, c_2, \ldots, c_{m-1}\), such that \(\mathbf{v}_m = \sum_{i = 1}^{m-1} c_i \mathbf{v}_i\). Since \(LA = I\) and column vectors of \(LA\) are \(L \mathbf{v}_1, L \mathbf{v}_2, \ldots, L \mathbf{v}_m\), which are \(\mathbf{v}_1, \mathbf{v}_2, \ldots, \sum_{i = 1}^{m-1} c_i L \mathbf{v}_i\); this implies that the last column vector of \(LA\) is spanned by the previous column vectors of \(LA\). However, the last column vector of \(LA\) should be the last vector from the canonical basis, and it should not be spanned by the previous column vectors (because the column vectors in an identity matrix are independent). Contradiction. 
\end{enumerate}
Suppose \(A\) has a right inverse \(R\). 
\begin{enumerate}
\setcounter{enumi}{2}
    \item Suppose \(A\mathbf{x} = \mathbf{b}\) has no solution. \textcolor{blue}{In this case \(A\) has no right inverse}. Assume it has a right inverse \(R\), then \(AR \mathbf{y} = \mathbf{y}\) and the linear combination of the column vectors of \(A\) defined by the vector \(R \mathbf{y}\) spans the whole image space, which produces a contradiction. 

    \item Suppose \(A\mathbf{x} = \mathbf{b}\) has multiple solutions. As previously discussed, \(A\) does not have a right inverse unless \(A\mathbf{x} = \mathbf{b}\) has solution(s) for every \(\mathbf{b}\). And if \(A\mathbf{x} = \mathbf{b}\) has solution(s) for every \(\mathbf{b}\), column vectors of \(A\) will span the entire image space. In this case, there are more columns than rows in \(A\). 

    If \(A\mathbf{x} = \mathbf{b}\) has multiple solutions for some \(\mathbf{b}\), column vectors of \(A\) are dependent, so \(A\mathbf{x} = \mathbf{0}\) has multiple solutions \(\Rightarrow A\mathbf{x} = \mathbf{b}\) has multiple solutions for all \(\mathbf{b}\) in the image space. Since \(AR = I\), let \(\mathbf{r}_1, \mathbf{r}_2, \ldots, \mathbf{r}_n\) be the column vectors of \(R\), then we have \(A \mathbf{r}_i = \mathbf{e}_i\) for all \(i = 1, 2, \ldots n\). Since each \(A \mathbf{r}_i = \mathbf{e}_i\) has multiple solutions for \(\mathbf{r}_i\), \textcolor{red}{there are multiple right inverses of \(A\)}. 
\end{enumerate}
Now suppose \(A\) is a square matrix and it is left invertible. By our previous discussion, since \(A\) has a left inverse, \(A\mathbf{x} = \mathbf{b}\) can have at most one solution. By previous discussion regarding pivots, this implies the column vectors of \(A\) are linearly independent in \(\mathbb{F}^n\), thus they form a basis in \(\mathbb{F}^n\). This means that \(A\) maps the canonical basis in \(\mathbb{F}^n\) to the set of column vectors of \(A\) which is also a basis. By Theorem 7, \(A\) is invertible. 

Suppose \(A\) is a square matrix and it is right invertible. Let \(R\) be its right inverse. Then \(A(R \mathbf{b}) = (AR) \mathbf{b} = \mathbf{b}\), which means \(A\mathbf{x} = \mathbf{b}\) always has a solution for any \(\mathbf{b} \in \mathbb{F}^n\). Therefore column vectors of \(A\) spans \(\mathbb{F}^n\), and with \(n\) of them this means they form a basis in \(\mathbb{F}^n\). By Theorem 7 again, \(A\) is invertible. 
\end{proof}
\section{Row reduction}
\begin{definition}[Row equivalent]
Matrices \(A\) and \(B\) are row equivalent if \(A\) can be formed by doing row operations on \(B\) and vise versa. 
\end{definition}
As previously discussed, any invertible matrix is row equivalent to the identity matrix. 

An algorithm of finding the inverse of an \( n \times n \) matrix is as follows:
\begin{enumerate}
    \item Form an \textit{augmented} \( n \times 2n \) matrix \( (A \mid I) \) by writing the \( n \times n \) identity matrix right of \( A \);
    \item Performing row operations on the augmented matrix transform \( A \) to the identity matrix \( I \);
    \item The matrix \( I \) that we added will be automatically transformed to \( A^{-1} \);
    \item If it is impossible to transform \( A \) to the identity by row operations, \( A \) is not invertible.
\end{enumerate}
An explanation of this algorithm is as follows: Let \(E_1, E_2, \ldots, E_N\) be the elementary matrices corresponding to the row operation we need to transform \(A\) into its reduced echelon form (which is the identity matrix), then we have \(E_N \ldots E_2 E_1 A = I\), which means \(E_N \ldots E_2 E_1 = A^{-1}\). Since we are doing row operations simultaneously, the matrix on the right side is \(E_N \ldots E_2 E_1 I = A^{-1}\). 
\begin{theorem}
Any invertible matrix can be represented as a product of elementary matrices. 
\end{theorem}
Proof omitted. 
\section{Dimension}
\begin{definition}
The dimension \( \dim V \) of a vector space \( V \) is the number of vectors in a basis.

For a vector space consisting only of zero vector \( \mathbf{0} \) we put \( \dim V = 0 \). If \( V \) does not have a (finite) basis, we put \( \dim V = \infty \).

If \( \dim V \) is finite, we call the space \( V \) \textit{finite-dimensional}; otherwise we call it \textit{infinite-dimensional}.
\end{definition}
\begin{proposition}
A vector space \(V\) is finite-dimensional if and only if it has a finite spanning system. 
\end{proposition}
Proof omitted. 
\begin{proposition}
An linearly independent system in a finite-dimensional vector space \(V\) cannot have more than \(\text{dim}V\) vectors in it. 
\end{proposition}
Proof omitted. 
\begin{proposition}
Any generating system in a finite-dimensional vector space \(V\) must have at least dim\(V\) vectors in it.
\end{proposition}
Proof omitted. 
\begin{proposition}[Completion to a basis]
A linearly independent system of vectors in a finite-dimensional space can be completed to a basis, i.e., if \(\mathbf{v}_1, ..., \mathbf{v}_r\) are linearly independent vectors in a finite-dimensional vector space \(V\) then one can find vectors \(\mathbf{v}_{r+1}, \mathbf{v}_{r+2}, \cdots \mathbf{v}_n\) such that the system of vectors \(\mathbf{v}_1, ..., \mathbf{v}_n\) is a basis in \(V\). 
\end{proposition}
\begin{proof}
Let \( n = \dim V \) and let \( r < n \) (if \( r = n \) then the system \( \mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_r \) is already a basis, and the case \( r > n \) is impossible). Take any vector not belonging to \( \mathrm{span}\{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_r\} \) and call it \( \mathbf{v}_{r+1} \) (one can always do that because the system \( \mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_r \) is not generating). Note that the system \( \mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_r, \mathbf{v}_{r+1} \) is linearly independent. Repeat the procedure with the new system to get vector \( \mathbf{v}_{r+2} \), and so on.

We will stop the process when we get a generating system. Note that the process cannot continue infinitely, because a linearly independent system of vectors in \( V \) cannot have more than \( n = \dim V \) vectors.
\end{proof}
\section{General solution of a linear system}
\begin{definition}
A homogeneous system is a system of the form \(A \mathbf{x} = \mathbf{0}\). 
\end{definition}
\begin{theorem}[General solution of a linear system]
Let a vector $\mathbf{x}_1$ satisfy the equation $A\mathbf{x} = \mathbf{b}$, and let $H$ be the set of all solutions of the associated homogeneous system
\[
A\mathbf{x} = \mathbf{0}.
\]

Then the set
\[
\{ \mathbf{x} = \mathbf{x}_1 + \mathbf{x}_h : \mathbf{x}_h \in H \}
\]
is the set of all solutions of the equation $A\mathbf{x} = \mathbf{b}$.

In other words, this theorem can be stated as
\[
\boxed{\text{General solution of } A\mathbf{x} = \mathbf{b}} 
= 
\boxed{\text{A particular solution of } A\mathbf{x} = \mathbf{b}} \]
\[+ 
\boxed{\text{General solution of } A\mathbf{x} = \mathbf{0}}.
\]
\end{theorem}
Proof by checking set inclusion from both directions. Omitted. 
\section{Fundamental subspaces of a matrix}
Recall that, given a linear transformation \(A: V \to W\), we can associate two subspace, its kernel and its range:
\begin{enumerate}
    \item \(\mathrm{Ker}\, A = \mathrm{Null}\, A := \{ \mathbf{v} \in V : A\mathbf{v} = \mathbf{0} \} \subset V\)
    
    \item \(\mathrm{Ran}\, A = \{ \mathbf{w} \in W : \mathbf{w} = A\mathbf{v} \text{ for some } \mathbf{v} \in V \} \subset W\)
\end{enumerate}
In other words, the kernel \(Ker A\) is the solution set of the homogeneous equation \(A \mathbf{x} = \mathbf{0}\), the range \(ran A\) is the set of the right sides \(\mathbf{b} \in  W\) for which the equation \(A\mathbf{x} = \mathbf{b}\) has a solution. 

By column by coordinate rule, any vector \(\mathbf{w} \in Ran A\) can be represented as a linear combination of columns of \(A\). This is why \(Ran A\) is also called column space (with notation \(Col A\)). 

We have other notations here:
\begin{enumerate}
\setcounter{enumi}{2}
    \item Row space \(Ran A^T\)
    \item Left null space \(Ker A^T\)
\end{enumerate}
The four subspaces are called the \textit{fundamental subspaces} of the matrix \(A\). 
\begin{definition}
Given a linear transformation (matrix) \(A\), its rank, rank\(A\), is the dimension of the range of \(A\) 
\[\text{rank} A := \text{dim Ran} A.\]
\end{definition}
\section{Relations between the dimensions of the four fundamental subspaces}
Here are several arguments regarding the four fundamental subspaces of \(A\):
\begin{enumerate}
    \item The pivot columns of the original matrix \(A\) give us a basis in Ran\(A\).
    \begin{proof}
        When we do row reductions on \(A\) and get its reduced echelon form \(A_e\), it is essentially multiplying a finite number of elementary matrices on the left of \(A\). Namely, we have \(A_e = E_N E_{N-1} \cdots E_2 E_1 A\). Suppose \(A\) is a \(m \times n\) matrix. Let \(E = E_N E_{N-1} \cdots E_2 E_1\), then \(A_e = EA\) and column vectors of \(A_e\) are \(E \mathbf{v}_1, \cdots E\mathbf{v}_n\) where \(\mathbf{v}_1, \cdot \mathbf{v}_n\) are column vectors of \(A\). Therefore, any subset of \(\{E \mathbf{v}_1, \cdots E\mathbf{v}_n\}\) is linearly independent if and only if the corresponding subset of \(\{\mathbf{v}_1, \cdots \mathbf{v}_n\}\) is linearly independent. 

        Note that the pivot columns of \(A_e\) is linearly independent and they form a basis of Ran\(A_e\). Any other column vector in \(A_e\) can be written as a linear combination of the pivot columns. Therefore, the corresponding column vectors in \(A\), i.e., the pivot columns of the original matrix \(A\), is linearly independent and any additional column vector in \(A\) is a linear combination of the pivot columns of \(A\). 

        Therefore, the span  of the pivot columns of \(A\) form ran\(A\). 

        \textcolor{red}{Note that the column space of \(A\) is not the same as the column space of \(A_e\) in general}. 
    \end{proof}

    \item The pivot rows of the echelon form \(A_e\) gives us a basis in the row space.
    \begin{proof}
        Note that doing row operations on \(A\) is removing row vectors in \(A\) that can be written as a linear combination of the other row vectors, which means doing row operation on \(A\) do not change the row space. 

        One can easily see that doing row operations on \(A\) cannot form vectors outside of the subspace spanned by the existing rows. Since we can do row operations reversely, inclusion in the other direction is also true. 

        To be precise, 
        \[\text{Ran}A^T = \text{Ran}(A_e)^T.\]

        Since the pivot rows of \(A_e\) is linearly independent and any other row vectors is within their span, the pivot rows of \(A_e\) is a basis for the row space. 
    \end{proof}
    \textcolor{blue}{Note that in this case the row spaces of \(A\) and \(A_e\) are the same.}
    \item To find a basis in the null space Ker\(A\) one needs to solve the homogeneous equation \(A\mathbf{x} = \mathbf{0}\). 
\end{enumerate}
\begin{theorem}[The Rank Theorem]
For a matrix \(A\), \[\text{rank} A = \text{rank} A^T.\]
\end{theorem}
\begin{proof}
Dimension of Ran\(A\) = number of pivots in \(A_e\) = dimension of Ran\(A^T\). Omitted.
\end{proof}
Let $A$ be an $m \times n$ matrix, i.e.\ a linear transformation from $\mathbb{F}^n$ to $\mathbb{F}^m$. Then we have the following theorems:
\begin{theorem}
\(\dim \ker A + \dim \operatorname{Ran} A = \dim \ker A + \operatorname{rank} A = n\) = dimension of the domain of $A$. 
\end{theorem}
\begin{proof}
To determine the dimension of \(\ker A\), we first go through the following algorithm: 
\begin{itemize}
    \item Let \(S_{col} = \{\mathbf{v}_1, \mathbf{v}_2, \cdots \mathbf{v}_n\}\) be the set of column vectors of \(A\);
    \item Let \(S = S_{col}\);
    \item Let \(S_{del} = \emptyset\);
    \item Take \(\mathbf{v}_1\); if \(\mathbf{v}_1 = \mathbf{0}\), remove it from set \(S\) and add it to \(S_{del}\);
    \item Take \(\mathbf{v}_2\); if \(\mathbf{v}_2 \in \text{span}\{\mathbf{v}_1\}\), remove it from \(S\) and add it to \(S_{del}\);
    \item Take \(\mathbf{v}_3\); if \(\mathbf{v}_3 \in \text{span}\{\mathbf{v}_1, \mathbf{v}_2\}\), remove it from \(S\) and add it to \(S_{del}\);
    \item Continue the above process until we reach \(\mathbf{v}_n\);
\end{itemize}
Now we have three sets of column vectors of \(A\): \(S_{col}\), \(S\) and \(S_{del}\). We have several claims here:
\begin{itemize}
    \item span\(S\) = span\(S_{col}\) = ran\(A\).
    
    \textit{Proof.} We already know that span\(S_{col}\) = ran\(A\). Since \(S \subset S_{col}\), span\(S \subset\) ran\(A\). Every vector in ran\(A\) can be spanned by \(S_{col}\), and every vector in \(S_{col}\) can be spanned by \(S\). The rest is omitted. 

    \item Number of elements in \(S\) = dimension of ran\(A\). 

    Proof omitted. 

    \item  Given any vector \(\mathbf{u}\) in \(S_{del}\) and the set \(S\), \textcolor{ForestGreen}{we can find a vector in \(\ker A\)}.

    \textit{Proof.} Suppose there are \(k\) elements in \(S\), \(k \leq n\). \(\mathbf{u} \in S_{del} \Rightarrow \mathbf{u}\) can be written as a linear combination of vectors in \(S\). Denote \(\mathbf{u} = \sum_{i = 1}^{k} c_{p_i} \mathbf{v}_{p_i}\).
    
    Denote the column index of the vectors in \(S\) as \(p_1, p_2, \cdots p_k\), and the column index of \(\mathbf{u}\) as \(q\), then \(A \mathbf{x} = \mathbf{y} = - \mathbf{u} + \sum_{i = 1}^{k} c_{p_i} \mathbf{v}_{p_i} = 0\), and \(\mathbf{x}\) is a vector in \(\ker A\).  

    \(\mathbf{x}\) can be written in a column vector with the \(q\)-th entry equals to \(-1\), the \(p_i\)-th entry equals to \(c_{p_i}\) for all \(i = 1, 2, \cdots k\), and all the other entries equal to \(0\).  

    \item The \(n - k\) vectors found through the above process, denoted as \(\mathbf{x}_1, \cdots \mathbf{x}_{n-k}\), are linearly independent. 

    \textit{Proof.} The proof is obvious: each vector \(\mathbf{x}_j\) has the entry corresponding to \(\mathbf{u}_j \in S_{del}\) equal to \(-1\), and entries \(p_{i,j}\) for \(i = 1, ..., k\), \(j = 1, ..., n-k\) equal to \(c_{p_1}^j, \cdots c_{p_k}^j\), i.e., entry \(p_{i, j}\) has value \(c_{p_i}^j\) for all \(i, j\), and all other entries 0. Pick any \(j\) from \(1, ..., n-k\). No linear combination of the rest \(n - k -1\) vectors in \(S_{del}\) can make the entry corresponding to \(\mathbf{u}_j\) be equal to \(-1\), because the rest of the vectors all have 0 on that entry. 

    Therefore, the dimension of \(\ker A\) is at least \(n - k\). We will see in the following argument that it is exactly \(n - k\). 
\end{itemize}
The following are notations for the proof:
\begin{itemize}
    \item Denote \(S = \{\mathbf{v}_{p_1}, \cdots \mathbf{v}_{p_k}\}\) and \(S_{del} = \{\mathbf{v}_{q_1}, \cdots \mathbf{v}_{q_r}\}\), with \(r = n - k\); and each \(\mathbf{v}_i\) is the \(i\)-th column vector in \(A\) for all \(i \in \{\mathbf{v}_{p_1}, \cdots \mathbf{v}_{p_k}, \mathbf{v}_{q_1}, \cdots \mathbf{v}_{q_r}\}\). 
    
    \item Denote \(K = \{\mathbf{x}_{q_1}, \cdots \mathbf{x}_{q_r}\}\) as the set containing all vectors in \(\ker A\) found in the above process (marked in green). 

    \item Let \(\mathbf{y}_{q_s} = A \mathbf{x}_{q_s}\) for all \(s = 1, \cdots r\). Then \(\mathbf{y}_s = 0\) for any \(s\) (proof omitted) and \(\mathbf{y}_s\) can be written as a linear combination of column vectors of \(A\), namely 
    \[\mathbf{y}_s = \sum_{i = 1}^k c_{p_i}^s \mathbf{v}_{p_i} - \mathbf{v}_{q_s}, \]
    for some unique (as the \(\mathbf{v}_{p_i}\)'s are linearly independent) \([c_{p_1}^s, \cdots c_{p_k}^s] \in \mathbb{F}^k\). 

    \item Clearly, the corresponding vector \(\mathbf{x}_s\) is in the form \([\cdots, c_{p_1}^s, \cdots, c_{p_2}^s, \cdots, \cdots, c_{p_k}^s, \cdots]^T\), with one additional entry valued \(-1\) and all the rest entries valued 0. 
\end{itemize}
Now we can use the previous discussion to argue that \(K\) is a basis for \(\ker A\): 
\begin{itemize}
    \item Fix some \(\mathbf{x} \in \ker A\), denoted as \(\mathbf{x} = [d_1, d_2, ..., d_n]^T\). Claim: \(\mathbf{x}\) is determined if the \(q_1, q_2, ..., q_r\)-th entries of \(\mathbf{x}\) are determined. 

    \textit{Proof.} Existence of such a vector: take \(\mathbf{x}_0 = - \sum_{j = 1}^r d_{q_j} \mathbf{x}_{q_j}\), then \(\mathbf{x}_0\) is a linear combination of vectors in \(K\), we have \(\mathbf{x}_0 \in \ker A\). Since vectors in \(K\) have all other \(q\)-labeled entries 0, the \(q_1, q_2, ..., q_r\)-th entries of \(\mathbf{x}\) are indeed \(d_{q_1}, ..., d_{q_r}\). 
    
    Uniqueness of such a vector: suppose \(\exists \mathbf{x}_1 \in \ker A\) has \(d_{q_1}, ..., d_{q_r}\) on its \(q_1, q_2, ..., q_r\)-th entries, and \(\mathbf{x}_1 \neq \mathbf{x}_0\). Therefore \(\mathbf{x}_2 = \mathbf{x}_1 - \mathbf{x}_0\), it is a non-zero vector in \(\ker A\), while its \(q\)-labeled entries are all 0. However, such a vector cannot exist, because \(A \mathbf{x}_2\) would be a non-trivial linear combination of vectors in \(S\). Vectors in \(S\) are linearly independent, so \(A \mathbf{x}_2 \neq \mathbf{0} \Rightarrow \mathbf{x}_2 \notin \ker A\). Contradiction. 

    Therefore, there exists one and only one vector in \(\ker A\) when the \(q_1, q_2, ..., q_r\)-th entries of the vector is fixed. 
    
    \item Any vector \(\mathbf{x} \in \ker A\) can be written as a linear combination of \(\mathbf{x}_1, \cdots \mathbf{x}_{n-k}\). 

    \textit{Proof.} Suppose \(\mathbf{x} = [d_1, d_2, ..., d_n]^T\), then \(\mathbf{x} = - \sum_{j = 1}^r d_{q_j} \mathbf{x}_{q_j}\).

    \item Therefore, \(K\) is a basis for \(\ker A\), and \(\dim \ker A = r\). Proof omitted. 
\end{itemize}
The rest of the proof is omitted. 
\end{proof}
\begin{remark}
Recall in quotient space, we have proved that for 
\[T: V \to W,\]
we have 
\[\operatorname{range} T \cong V/\ker T.\]
Therefore, 
\[\dim \operatorname{range} T = \dim (V/\ker T) = \dim V - \dim \ker T,\]
which means 
\[\dim V = \dim \ker T + \dim \operatorname{range} T.\]
So \textcolor{red}{this offers another proof of the above theorem}.
\end{remark}
\begin{theorem}
\(\dim \ker A^T + \dim \operatorname{Ran} A^T = \dim \ker A^T + \operatorname{rank} A^T 
= \dim \ker A^T + \operatorname{rank} A = m\) = dimension of the target space of $A$.
\end{theorem}
\begin{proof}
If \(A: V \to W\), then \(A^T: W \to V\). Omitted. 
\end{proof}
\begin{theorem}
Let \(A\) be an \(m \times n\) matrix. Then the equation 
\[A \mathbf{x} = \mathbf{b}\]
has a solution for every \(\mathbf{b} \in \mathbb{F}^m\) if and only if the dual equation 
\[A^T \mathbf{x} = \mathbf{0}\]
has a unique (the trivial) solution. 
\end{theorem}
\begin{proof}
\(A \mathbf{x} = \mathbf{b}\) always has solution(s) \(\Rightarrow A\) is full rank, \(\rank A = m\) \(\Rightarrow \rank A^T = \rank A = m\) \(\Rightarrow \ker A^T = 0\) \(\Rightarrow\) the dual equation has a unique solution. 
\end{proof}
\section{Represent a linear transformation in arbitrary bases}
\begin{definition}
Let \(V\) be a vector space with a basis \(\mathcal{B} := \{\mathbf{b}_1, \cdots \mathbf{b}_n\}\). Any vector \(\mathbf{v} \in V\) admits a unique representation as a linear combination
\[\mathbf{v} = x_1 \mathbf{b}_1 + \cdots + x_n \mathbf{b}_n = \sum_{k = 1}^n x_k \mathbf{b}_k.\]
The numbers \(x_1, x_2, ..., x_n\) are called the \textit{coordinates} of the vector \(\mathbf{v}\) in the basis \(\mathcal{B}\). It is convenient to join these coordinates into the so-called 
\textit{coordinate vector} of $\mathbf{v}$ relative to the basis $\mathcal{B}$, 
which is the column vector
\[
[\mathbf{v}]_{\mathcal{B}} := 
\begin{pmatrix}
x_1 \\
x_2 \\
\vdots \\
x_n
\end{pmatrix}
\in \mathbb{F}^n.
\]
\end{definition}
\begin{remark}
The mapping 
\[\mathbf{v} \mapsto [\mathbf{v}]_{\mathcal{B}}\]
is an isomorphism between \(V\) and \(\mathbb{F}^n\). It transforms the basis \(\{\mathbf{b}_1, \cdots \mathbf{b}_n\}\) to the standard basis \(\{\mathbf{e}_1, \cdots \mathbf{e}_n\}\) in \(\mathbb{F}^n\). 
\end{remark}
\section{Matrix of a linear transformation}
Let \(T: V \to W\) be a linear transformation. Let \(\mathcal{A} = \{\mathbf{a}_1, \mathbf{a}_2, ..., \mathbf{a}_n\}\) be a basis for \(V\), let \(\mathcal{B} = \{\mathbf{b}_1, \mathbf{b}_2, \cdots \mathbf{b}_m\}\) be a basis for \(W\). 

When we define \(\mathbf{v}\) as a vector, we don't need basis as reference. In general, the same vector has different \textit{column vectors of coordinates} when represented in different bases. Therefore, when we define \(T\) as a linear transformation, \textcolor{red}{we don't need any basis as reference}. Recall that \(T\) is defined by specifying what vectors it will map to for a basis of the domain space. However, even if we pick another basis for the domain space, the vectors \(T\) maps to for the original basis would be the same. 

On the other hand, \textcolor{red}{a matrix transforming a column vector of coordinates into another column vector of coordinates, is defined on specific bases for the domain space and the target space}. 
\begin{example}
Suppose \((x_1, ..., x_n)^T\) is a column vector of coordinates, if the basis specified for the domain space is \(\mathcal{A}\), the vector this column vector of coordinates represents is 
\[\mathbf{v} = \sum_{i = 1}^n x_i \mathbf{a}_i \in V.\]

Suppose \(M\) is an \(m \times n\) matrix, and \(M (x_1, ..., x_n)^T = (y_1, ..., y_m)^T\). Since the basis specified for the target space is \(\mathcal{B}\), the vector in the target space we are referring to is 
\[\mathbf{w} = \sum_{j = 1}^m y_j \mathbf{b}_j.\]

Therefore, \textcolor{blue}{when we specify the two bases for the domain space and the target space, the matrix is representing a linear transformation}. 
\end{example}
A matrix of the transformation \( T \) in (or with respect to) the bases \( \mathcal{A} \) and \( \mathcal{B} \) is an \( m \times n \) matrix, denoted by \( [T]_{\mathcal{B}\mathcal{A}} \), which relates the coordinate vectors \( [T\mathbf{v}]_{\mathcal{B}} \) and \( [\mathbf{v}]_{\mathcal{A}} \),
\[
[T\mathbf{v}]_{\mathcal{B}} = [T]_{\mathcal{B}\mathcal{A}} [\mathbf{v}]_{\mathcal{A}};
\]
notice the balance of symbols \( \mathcal{A} \) and \( \mathcal{B} \) here: this is the reason we put the first basis \( \mathcal{A} \) into the second position.
\begin{remark}
Given different bases for the domain and target spaces, in general, we will have different matrices to represent the same linear transformation \(T\). 
\end{remark}
\begin{remark}
On the other hand, for the same matrix \(M\), when we specify different bases for the domain space and target space, they represent different linear transformations. 
\end{remark}
Suppose \(T: V \to W\) is defined as a linear transformation, and the bases for the domain space and target space are specified as \(\mathcal{A}\) and \(\mathcal{B}\). How to find \([T]_{\mathcal{B}\mathcal{A}}\)?

The answer is simple: Let \(M = [T]_{\mathcal{B}\mathcal{A}}\) be the matrix we are looking for. Note that \(M [1, 0, ..., 0]^T\) is the first column of \(M\), \(M [0, 1, 0, ..., 0]^T\) is the second column of \(M\) and so on. Since
\[[\mathbf{a}_1]_{\mathcal{A}} = [1, 0, ..., 0]^T,\]
\[[\mathbf{a}_2]_{\mathcal{A}} = [0, 1, 0, ..., 0]^T\]
and so on, the \(i\)-th column of \(M\) is 
\[M [\mathbf{a}_i]_{\mathcal{A}},\]
which is
\[[T]_{\mathcal{B}\mathcal{A}} [\mathbf{a}_i]_{\mathcal{A}} = [T\mathbf{a}_i]_{\mathcal{B}}.\]
Note that \([T\mathbf{a}_i]_{\mathcal{B}}\) is a column vector of coordinates, so the matrix \(M\) we just found is well-defined. 
\begin{corollary}[Composition of linear transformations]
Let \( T_1 : X \to Y \) and \( T_2 : Y \to Z \) be linear transformations, and let \( \mathcal{A}, \mathcal{B} \), and \( \mathcal{C} \) be bases in \( X, Y \), and \( Z \) respectively.  
Then for the composition \( T = T_2 T_1 \),  
\[
T : X \to Z, \qquad T\mathbf{x} := T_2(T_1(\mathbf{x}))
\]  
we have  
\[
[T]_{\mathcal{C}\mathcal{A}} = [T_2 T_1]_{\mathcal{C}\mathcal{A}} = [T_2]_{\mathcal{C}\mathcal{B}} [T_1]_{\mathcal{B}\mathcal{A}}
\]  
(notice again the balance of indices here).
\end{corollary}
Proof omitted. 
\section{Change of coordinate matrix}
Let \(\mathcal{A} = \{\mathbf{a}_1, ..., \mathbf{a}_n\}\), \(\mathcal{B} = \{\mathbf{b}_1, ..., \mathbf{b}_n\}\) both be basis for a vector space \(V\). Consider the identity transformation \(I = I_V\) and its matrix \([I]_{\mathcal{B} \mathcal{A}}\) in these bases. 

By definition,
\[[\mathbf{v}]_{\mathcal{B}} = [I]_{\mathcal{B} \mathcal{A}} [\mathbf{v}]_{\mathcal{A}} \quad \forall \mathbf{v} \in V.\]
i.e., for any vector \(\mathbf{v} \in V\), the matrix \([I]_{\mathcal{B} \mathcal{A}}\) transforms its column vector of coordinates in the basis \(\mathcal{A}\) into column vector of coordinates in the basis \(\mathcal{B}\). 

The matrix $[I]_{\mathcal{B} \mathcal{A}}$ is often called the \textit{change of coordinates} (from the basis $\mathcal{A}$ to the basis $\mathcal{B}$) matrix.

The matrix $[I]_{\mathcal{B} \leftarrow \mathcal{A}}$ is easy to compute: according to the general rule of finding the matrix of a linear transformation, its $k$th column is the coordinate representation $[\mathbf{a}_k]_{\mathcal{B}}$ of $k$th element of the basis $\mathcal{A}$.

Note that
\[
[I]_{\mathcal{A} \mathcal{B}} = \left( [I]_{\mathcal{B} \mathcal{A}} \right)^{-1},
\]
so any change of coordinate matrix is always invertible.
\begin{proof}
We have
\[[I]_{\mathcal{A} \mathcal{B}} [I]_{\mathcal{B} \mathcal{A}} = [I]_{\mathcal{A} \mathcal{A}},\]
and since 
\[[\mathbf{v}]_{\mathcal{A}} = [I]_{\mathcal{A} \mathcal{A}} [\mathbf{v}]_{\mathcal{A}} \quad \forall \mathbf{v} \in V,\]
\([I]_{\mathcal{A} \mathcal{A}}\) is the identity matrix. 
\end{proof}
\section{Matrix of a transformation and change of coordinates}
Let \( T : V \to W \) be a linear transformation, let \( \mathcal{A}, \widetilde{\mathcal{A}} \) be two bases in \( V \) and let \( \mathcal{B}, \widetilde{\mathcal{B}} \) be two bases in \( W \). Suppose we know the matrix \( [T]_{\mathcal{B}\mathcal{A}} \), and we would like to find the matrix representation with respect to new bases \( \widetilde{\mathcal{A}}, \widetilde{\mathcal{B}} \), i.e. the matrix \( [T]_{\widetilde{\mathcal{B}}\widetilde{\mathcal{A}}} \). 

To do this is simple: We need a little help from two change of coordinates matrices. Indeed, suppose we pick an arbitrary vector in \(V\), denoted as \(\mathbf{v}\), then this vector written in basis \(\widetilde{\mathcal{A}}\) is a column vector of coordinates denoted as \([\mathbf{v}]_{\widetilde{\mathcal{A}}}\). We have 
\[[T \mathbf{v}]_{\mathcal{B}} = [T]_{\mathcal{B} \mathcal{A}} [\mathbf{v}]_{\mathcal{A}};\]
\[[T \mathbf{v}]_{\widetilde{\mathcal{B}}} = [I]_{\widetilde{\mathcal{B}} \mathcal{B}} [T \mathbf{v}]_{\mathcal{B}};\]
\[[\mathbf{v}]_{\mathcal{A}} = [I]_{\mathcal{A} \widetilde{\mathcal{A}}} [\mathbf{v}]_{\widetilde{\mathcal{A}}}; \]
\[[T \mathbf{v}]_{\widetilde{\mathcal{B}}} = [T]_{\widetilde{\mathcal{B}} \widetilde{\mathcal{A}}} [\mathbf{v}]_{\mathcal{A}};\]
Therefore, 
\begin{equation*}
[T \mathbf{v}]_{\widetilde{\mathcal{B}}}  
= [I]_{\widetilde{\mathcal{B}} \mathcal{B}} [T \mathbf{v}]_{\mathcal{B}} 
= [I]_{\widetilde{\mathcal{B}} \mathcal{B}} [T]_{\mathcal{B} \mathcal{A}} [\mathbf{v}]_{\mathcal{A}}  
= [I]_{\widetilde{\mathcal{B}} \mathcal{B}} [T]_{\mathcal{B} \mathcal{A}} [I]_{\mathcal{A} \widetilde{\mathcal{A}}} [\mathbf{v}]_{\widetilde{\mathcal{A}}}
\end{equation*}
Therefore, 
\[[T]_{\widetilde{\mathcal{B}} \widetilde{\mathcal{A}}} = [I]_{\widetilde{\mathcal{B}} \mathcal{B}} [T]_{\mathcal{B} \mathcal{A}} [I]_{\mathcal{A} \widetilde{\mathcal{A}}}.\]
Note the balance of indices. Therefore the formula is well-defined. 
\section{Case of one basis: similar matrices}
Let \(V\) be a vector space, let \(\{\mathbf{a}_1, \mathbf{a}_2, \cdots, \mathbf{a}_n\}\) be a basis in \(V\). Consider a linear transformation \(T: V \to V\) and let \([T]_{\mathcal{A} \mathcal{A}}\) be its matrix in this basis. This means we use the same basis as "inputs" and "outputs". 

The case when we use the same basis for inputs and outputs is important, because \textcolor{red}{in this case we can multiply a matrix by itself}. In this case, we often use the shorter notation \([T]_{\mathcal{A}}\). 

Let \(\mathcal{B} = \{\mathbf{b}_1, \mathbf{b}_2, \ldots, \mathbf{b}_n\}\) be another basis in \(V\). By the change of coordinate rule above
\[
[T]_{\mathcal{B}\mathcal{B}} = [I]_{\mathcal{B}\mathcal{A}} [T]_{\mathcal{A}\mathcal{A}} [I]_{\mathcal{A}\mathcal{B}}
\]
Recalling that
\[
[I]_{\mathcal{B}\mathcal{A}} = [I]_{\mathcal{A}\mathcal{B}}^{-1}
\]
and denoting \(Q := [I]_{\mathcal{A}\mathcal{B}}\), we can rewrite the above formula as
\[
[T]_{\mathcal{B}\mathcal{B}} = Q^{-1} [T]_{\mathcal{A}\mathcal{A}} Q.
\]
\begin{definition}
We say a matrix \(A\) is similar to a matrix \(B\) if there exists an invertible matrix \(Q\), such that \(A = Q^{-1} B Q\). 
\end{definition}
\begin{corollary}
Since an invertible matrix must be square, it follows from counting dimensions, that similar matrices \(A\) and \(B\) are both square and of the same size.
\end{corollary}
\begin{corollary}
If \(A\) is similar to \(B\), then \(B\) is similar to \(A\). Therefore, we just say matrices \(A\) and \(B\) are similar. 
\end{corollary}
\begin{remark}
The above discussion shows, \textcolor{red}{one can treat similar matrices as different matrix representations of the same linear operator}. On the other hand, when the bases of the domain space and the target space are the same for each representation, two different matrix representations of the same linear operator are always similar. 
\end{remark}
\begin{remark}
Besides, the above analysis also shows that two different matrix representations of the same linear operator are not necessarily similar when the bases of the domain space and the target space are different. 
\end{remark}
\newpage
\chapter{Duality}
\section{Dual space and dual map}
\begin{definition}[Linear functional]
A \textit{linear functional} on $V$ is a linear map from $V$ to $\mathbb{F}$. In other words, a linear functional is an element of $\mathcal{L}(V, \mathbb{F})$.
\end{definition}
\begin{example}
An evaluation on a space of functions is a functional. 
\end{example}
\begin{example}
An integration on a space of functions is a functional. 
\end{example}
\begin{definition}[Dual space \(V'\)]
The \textit{dual space} of \( V \), denoted by \( V' \), is the vector space of all linear functionals on \( V \). In other words, \( V' = \mathcal{L}(V, \mathbb{F}) \).
\end{definition}
\begin{theorem}[\(\dim V = \dim V'\)]
Suppose \( V \) is finite-dimensional. Then \( V' \) is also finite-dimensional and
\[
\dim V' = \dim V.
\]
\end{theorem}
Proof omitted. 
\begin{definition}[dual basis]
If \( v_1, \ldots, v_n \) is a basis of \( V \), then the \textit{dual basis} of \( v_1, \ldots, v_n \) for \(V'\) is the list \( \varphi_1, \ldots, \varphi_n \) of elements of \( V' \), where each \( \varphi_j \) is the linear functional on \( V \) such that
\[
\varphi_j(v_k) = 
\begin{cases}
1 & \text{if } k = j, \\
0 & \text{if } k \ne j.
\end{cases}
\]
\end{definition}
\begin{remark}
Note that \textcolor{red}{the dual basis is defined based on a specific basis of the original space}. 
\end{remark}
\begin{remark}
We can run a simple check, and we can see that the dual basis can span the entire function space and are linearly independent, so \textcolor{blue}{it is indeed a basis for \(V'\)}. Besides, defining such a set and proving it is a basis offers another proof for the dimension theorem. 
\end{remark}
\begin{corollary}[Dual basis gives the coefficients for linear combination]
Suppose \( v_1, \ldots, v_n \) is a basis of \( V \) and \( \varphi_1, \ldots, \varphi_n \) is the dual basis. Then
\[
v = \varphi_1(v) v_1 + \cdots + \varphi_n(v) v_n
\]
for each \( v \in V \).
\end{corollary}
Proof omitted. 
\begin{definition}[dual map, \(T'\)]
Suppose \( T \in \mathcal{L}(V, W) \). The \emph{dual map} of \( T \) is the linear map \( T' \in \mathcal{L}(W', V') \) defined for each \( \varphi \in W' \) by
\[
T'(\varphi) = \varphi \circ T.
\]   
\end{definition}
\begin{remark}
The dual map \(T': W' \to V'\) is defined after knowing an original map \(T: V \to W\).
\end{remark}
\begin{remark}
\begin{enumerate}
    \item \(\varphi \in W'\), so \(\varphi\) maps vectors in \(W\) to scalars;
    \item \(T': W' \to V'\) maps functionals in \(W'\) to functionals in \(V'\);
    \item Therefore, \(T'(\varphi) \in V'\), \(T'(\varphi)\) is a functional in \(V'\);
    \item On the other hand, \(\varphi \circ T\) maps elements in \(V\) to \(W'\), by composition.
\end{enumerate}
Now let's check that \(T'(\varphi)\) is indeed a functional in \(V'\):
\[
\begin{tikzcd}
V \arrow[r, "T"] \arrow[dr, "T'(\varphi)"'] & W \arrow[d, "\varphi"] \\
& K
\end{tikzcd}
\]
Pick \(\mathbf{v} \in V\), then by definition,
    \[T'(\varphi) \mathbf{v} = \varphi \circ T(\mathbf{v})\]
    is \(\varphi\) acting on an element \(T \mathbf{v} \in W\), which is a scalar. Therefore, \textcolor{red}{\(T'(\varphi)\) is indeed a functional in \(V'\)}. 
\end{remark}
\begin{remark}
Given \(T: V \to W\), its dual map \(T'\) as defined above is a linear map. Proof omitted. 
\end{remark}
\begin{example}
Let \(D'\) denote the dual of the linear map \(D\), and let \(p'\) denote the derivative of a polynomial \(p\).

Here are some basic notions:
\begin{itemize}
    \item The space of polynomials on \(\mathbb{R}\), \(\mathbb{C}\) or some general scalar space \(K\), is a vector space. 
    \begin{proof}
    Suppose the polynomials have highest degree \(N\), then the polynomial space is a vector space of dimension \(N + 1\). Indeed, pick \(1, x, x^2, ..., x^N\) in the space, then those elements are linearly independent in the polynomial space, and they span the entire space, which means they form a basis for the polynomial space. 

    Suppose the polynomials does not have a highest degree, then this space is an infinite dimensional vector space, with a choice of basis being \(\{1, x, x^2, ..., x^n, ...\}\). 

    In any of the above cases, addition and scalar multiplication are well-defined. 
    \end{proof}
    
    \item Denote \(\mathbb{P}^N\) as the set of polynomial on \(\mathbb{R}\) with highest degree \(N\). Define 
    \[D: \mathbb{P}^N \to \mathbb{P}^{N-1}\]
    as the differentiation map. Then \(D\) is a linear transformation. 
    \begin{proof}
    Since \(\{1, 2x, 3x^2, 4x^3, ..., nx^{n-1}, ..., Nx^{N-1}\}\) is a basis for \(\mathbb{P}^{N-1}\), and \(D\) maps the basis \(\{1, x, x^2, ..., x^N\}\) to the above basis (element-wise), \(D\) is a linear transformation. 
    \end{proof}
\end{itemize}
We denote \(\mathbb{P}(\mathbb{R})\) as the vector space of polynomials over \(\mathbb{R}\). 
\begin{itemize}
  \item Suppose $\varphi$ is the linear functional on $\mathbb{P}(\mathbb{R})$ defined by $\varphi(p) = p(3)$. Then $D'(\varphi)$ is the linear functional on $\mathbb{P}(\mathbb{R})$ given by
  \[
  (D'(\varphi))(p) = (\varphi \circ D)(p) = \varphi(Dp) = \varphi(p') = p'(3).
  \]
  Thus $D'(\varphi)$ is the linear functional on $\mathbb{P}(\mathbb{R})$ taking $p$ to $p'(3)$.

  \item Suppose $\varphi$ is the linear functional on $\mathbb{P}(\mathbb{R})$ defined by $\varphi(p) = \int_0^1 p$. Then $D'(\varphi)$ is the linear functional on $\mathbb{P}(\mathbb{R})$ given by
  \begin{align*}
  (D'(\varphi))(p) &= (\varphi \circ D)(p) \\
  &= \varphi(Dp) \\
  &= \varphi(p') \\
  &= \int_0^1 p' \\
  &= p(1) - p(0).
  \end{align*}
  Thus $D'(\varphi)$ is the linear functional on $\mathbb{P}(\mathbb{R})$ taking $p$ to $p(1) - p(0)$.
\end{itemize}
\end{example}
\begin{theorem}[algebraic properties of dual maps]
Suppose $T \in \mathcal{L}(V, W)$. Then
\begin{itemize}
  \item[(a)] $(S + T)' = S' + T'$ for all $S \in \mathcal{L}(V, W)$;
  \item[(b)] $(\lambda T)' = \lambda T'$ for all $\lambda \in \mathbb{F}$;
  \item[(c)] $(ST)' = T'S'$ for all $S \in \mathcal{L}(W, U)$.
\end{itemize}
\end{theorem}
\begin{proof}
Proofs for \((a)\) and \((b)\) are omitted. For \((c)\), given any \(\varphi \in U'\), \((ST)' (\varphi)\) is \(\varphi \circ (ST)\). On the other hand, 
\[(T'S')(\varphi) = (T') (S' (\varphi)) = (T') (\varphi \circ S) = \varphi \circ S \circ T.\]
\end{proof}
\section{Null space and range of dual of linear map}
\begin{definition}[annihilator, \(U^0\)]
For \( U \subseteq V \), the \textit{annihilator} of \( U \), denoted by \( U^0 \), is defined by
\[
U^0 = \{ \varphi \in V' : \varphi(u) = 0 \text{ for all } u \in U \}.
\]
\end{definition}
\begin{corollary}
The annihilator of \(U\), denoted \(U^0\), is a subspace of \(V'\). 
\end{corollary}
Proof omitted. 
\begin{example}
Suppose \(U\) is the subspace of \(\mathbb{P}(\mathbb{R})\) consisting of polynomial multiplers of \(x^2\). If \(\varphi\) is the linear functional of \(\mathbb{P}(\mathbb{P})\) defined by \(\varphi(p) = p'(0)\), then \(\varphi \in U^0\). 
\end{example}
\begin{theorem}
Suppose \(V\) is finite-dimensional and \(U\) is a subspace of \(V\). Then 
\[\dim U^0 = \dim V - \dim U.\]
\end{theorem}
\begin{proof}
Let \(\dim V = m\), \(\dim U = n\). Let 
\[\{\mathbf{v}_1, ..., \mathbf{v}_m\}\]
be a basis for \(V\), and among them 
\[\{\mathbf{v}_1, ..., \mathbf{v}_n\}\]
is a basis for \(U\). 

Let 
\[\{\varphi_1, \varphi_2, \cdots, \varphi_m\}\]
be a dual basis in \(V'\), such that for each \(i\) in \(1, 2, \cdots, m\), \(\varphi_i (\mathbf{v}_i) = 1\) and \(\varphi_i (\mathbf{v}_j) = 0\) for \(j \ne i\). 

We claim that \(\{\varphi_{n+1}, \varphi_{n+2}, \cdots, \varphi_m\}\) is a basis for \(U^0\). 
\begin{enumerate}
    \item First of all, any linear combination 
    \[\varphi = \sum_{k = n+1}^m c_k \varphi_k\]
    is in \(U^0\). Indeed, \(\forall \mathbf{v} \in U\), it is in the form 
    \[\mathbf{v} = x_1 \mathbf{v}_1 + \cdots + \mathbf{v}_n,\]
    and \(\varphi(\mathbf{v}) = 0\). 
    \item Second, \(\{\varphi_{n+1}, \varphi_{n+2}, \cdots, \varphi_m\}\) is linearly independent. This is obvious because this set is a subset of the dual basis in \(V'\). 
    \item Third, the set \(\{\varphi_{n+1}, \varphi_{n+2}, \cdots, \varphi_m\}\) spans \(U^0\). This is also obvious: Let
    \[\varphi = c_1 \varphi_1 + \cdots + c_m \varphi_m,\]
    since the coefficients are arbitrary, it can represent any element in \(V'\). Now since it should map every element in \(U\) to zero, it should map 
    \[\{\varphi_1, \varphi_2, \cdots, \varphi_n\}\]
    to zeros. Therefore 
    \[c_1 = c_2 = ... = c_n = 0.\]
    Therefore the set formed by \(\varphi\)'s in the form
    \[\varphi = c_{n+1} \varphi_{n+1} + \cdots + c_m \varphi_m\]
    contains \(U^0\) as a subset, and \(\{\varphi_{n+1}, \varphi_{n+2}, \cdots, \varphi_m\}\) spans it. 
\end{enumerate}
Therefore \[\{\varphi_{n+1}, \varphi_{n+2}, \cdots, \varphi_m\}\] 
is a basis for \(U^0\), and we have 
\[\dim U^0 = \dim V - \dim U.\]
\end{proof}
\begin{theorem}
Suppose \(V\) is finite-dimensional, and \(U\) is a subspace of \(V\). Then 
\begin{itemize}
    \item \(U^0 = \{0\}\) \(\iff\) \(U = V\);
    \item \(U^0 = V'\) \(\iff\) \(U = \{0\}\).
\end{itemize}
\end{theorem}
Proof by using the relation 
\[\dim U^0 = \dim V - \dim U.\] 
Omitted. 
\begin{theorem}[the null space of \(T'\)]
Suppose \( V \) and \( W \) are finite-dimensional and \( T \in \mathcal{L}(V, W) \). Then
\begin{itemize}
  \item[(a)] \( \operatorname{null} T' = (\operatorname{range} T)^0\);
  \item[(b)] \( \dim \operatorname{null} T' = \dim \operatorname{null} T + \dim W - \dim V \).
\end{itemize}
\end{theorem}
\begin{proof}
The first one is trivial. Omitted. For the second one, by the previous result, we have
\[\dim \ker T' = \dim (\operatorname{range} T)^0 = \dim W - \dim \operatorname{range} T\]
which is 
\[\dim W - (\dim V - \dim \ker T) = \dim \operatorname{null} T + \dim W - \dim V.\]
\end{proof}
\begin{theorem}[\(T\) surjective is equivalent to \(T'\) injective]
Suppose \( V \) and \( W \) are finite-dimensional and \( T \in \mathcal{L}(V, W) \). Then
\[
T \text{ is surjective } \Longleftrightarrow T' \text{ is injective}.\]
\end{theorem}
\begin{proof}
\(T\) is surjective \(\Longrightarrow\) \(\dim \operatorname{range} T = \dim W\) \(\Longrightarrow\) \(\dim \ker T' = \dim \ker T + \dim W - \dim V  = \dim \ker T + \dim \operatorname{range} T - \dim V = 0\) \(\Longrightarrow\) \(T'\) is injective. 

\(T'\) is injective \(\Longrightarrow\) \(\dim \ker T' = 0\) \(\Longrightarrow\) \(\dim \ker T + \dim W-\dim V = 0\) \(\Longrightarrow\) \(\dim W = \dim \operatorname{range} T\) \(\Longrightarrow\) \(T\) is surjective. 
\end{proof}
\begin{theorem}[range of \(T'\)]
Suppose \( V \) and \( W \) are finite-dimensional and \( T \in \mathcal{L}(V, W) \). Then  
\begin{itemize}
  \item[(a)] \( \dim \operatorname{range} T' = \dim \operatorname{range} T \);
  \item[(b)] \( \operatorname{range} T' = (\operatorname{null} T)^0 \).
\end{itemize}
\end{theorem}
\begin{proof}
\begin{align*}
\dim \operatorname{range} T' &= \dim W' - \dim \ker T' \\
&= \dim W - \dim \ker T' \\
&= \dim W - (\dim \ker T + \dim W - \dim V) \\
&= \dim V - \dim \ker T \\
&= \dim \operatorname{range} T
\end{align*}
\[\operatorname{range}T = \{\varphi \in V' : \exists \psi \in W', \psi \circ T = \varphi\}\]
\[(\ker T)^0 = \{\varphi \in V': \varphi(\ker T) = \{0\}\}\]
Clearly, 
\[\forall \varphi \in \operatorname{range} T', \varphi (\ker T) = \psi \circ T (\ker T) = \{0\}\]
for some \(\psi\) in \(W'\); we have \(\operatorname{range} T \subset (\ker T)^0\). On the other hand, 
\begin{align*}
\dim (\ker T)^0 &= \dim V - \dim \ker T \\
&= \dim \operatorname{range} T \\
&= \dim \operatorname{range} T' 
\end{align*}
Therefore the two subspaces are the same. 
\end{proof}
\begin{theorem}[\(T\) injective is equivalent to \(T'\) surjective]
Suppose \( V \) and \( W \) are finite-dimensional and \( T \in \mathcal{L}(V, W) \). Then  
\[
T \text{ is injective} \iff T' \text{ is surjective}.
\]
\end{theorem}
\begin{proof}
\begin{align*}
T \text{ is injective} &\iff \dim \ker T = 0 \\
&\iff \dim V = \dim \operatorname{range} T \\
&\iff \dim V' = \dim \operatorname{range} T \\
&\iff T' \text{ is surjective}
\end{align*}
\end{proof}
\section{Matrix of dual of linear map}
Suppose $V$ and $W$ are vector spaces, with bases 
$\{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_n\}$ and 
$\{\mathbf{w}_1, \mathbf{w}_2, \dots, \mathbf{w}_m\}$, respectively. 

Automatically we have dual bases 
$\{\varphi_1, \varphi_2, \dots, \varphi_n\}$ and $\{\psi_1, \psi_2, \dots, \psi_m\}$ 
for dual spaces $V'$ and $W'$, respectively.

Suppose \(T: V \to W\) is a linear transformation from \(V\) to \(W\), and the matrix \(\mathcal{M}(T)\) is computed with respect to the above two bases of \(V\) and \(W\). 

Let 
\[\mathcal{A} = \{\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_n\},\]
\[\mathcal{B} = \{\mathbf{w}_1, \mathbf{w}_2, \dots, \mathbf{w}_m\}.\]
Recall that 
\[\textcolor{red}{\mathcal{M}(T)} = \textcolor{red}{[T]_{\mathcal{B} \mathcal{A}}}\]
and
\[\textcolor{ForestGreen}{[\mathbf{w}]_{\mathcal{B}}} = \textcolor{red}{[T]_{\mathcal{B} \mathcal{A}}}\textcolor{ForestGreen}{[\mathbf{v}]_{\mathcal{A}}}.\]
Note that in the above two equations we marked matrices in red and coordinate vectors in green. 

Since 
\[\textcolor{red}{[T]_{\mathcal{B} \mathcal{A}}} \textcolor{ForestGreen}{[0 \cdots 0 \quad 1 \quad 0 \cdots  0]^T} = \textcolor{ForestGreen}{\text{the \(i\)-th column vector of the matrix }[T]_{\mathcal{B} \mathcal{A}}},\]
where the column vector is the \(i\)-th canonical vector. 

Therefore we have 
\[\textcolor{red}{[T]_{\mathcal{B} \mathcal{A}}} \textcolor{ForestGreen}{[\mathbf{v}_i]_{\mathcal{B}}} = \textcolor{ForestGreen}{[T \mathbf{v}_i]_{\mathcal{B}}},\]
which means the \(i\)-th column vector of the matrix \(\textcolor{red}{[T]_{\mathcal{B} \mathcal{A}}}\) is defined by \(\textcolor{ForestGreen}{[T \mathbf{v}_i]_{\mathcal{B}}}\). 

Similarly, let 
\[\mathcal{C} = \{\varphi_1, \varphi_2, \dots, \varphi_n\}\]
be the dual basis for \(V'\) and 
\[\mathcal{D} = \{\psi_1, \psi_2, \dots, \psi_m\}\]
be the dual basis for \(W'\). We have
\[T': W' \to V',\]
and
\[\varphi_i: V \to \mathbb{F}\]
for each \(i\),
\[\psi_j: W \to \mathbb{F}\]
for each \(j\). 

Let \(\mathcal{E} = \{1\}\) be the basis for \(\mathbb{F}\). Now each vector in the two dual spaces can be written as a matrix with respect to bases for \(V\) or \(W\) and \(\mathcal{E}\). We have 
\[[\varphi_i \mathbf{v}]_{\mathcal{E}} = [\varphi_i]_{\mathcal{EA}} [\mathbf{v}]_{\mathcal{A}}\]
and 
\[[\psi_j \mathbf{w}]_{\mathcal{E}} = [\psi_j]_{\mathcal{EB}} [\mathbf{w}]_{\mathcal{B}}.\]
By the general rule described above, we have
\[[\varphi_i]_{\mathcal{EA}} [\mathbf{v_k}]_{\mathcal{A}} = [\varphi_i \mathbf{v_k}]_{\mathcal{E}} = 0\]
when \(i \ne k\), and 
\[[\varphi_i]_{\mathcal{EA}} [\mathbf{v_i}]_{\mathcal{A}} = [\varphi_i \mathbf{v_i}]_{\mathcal{E}} = 1.\]
Therefore, 
\[[\varphi_i]_{\mathcal{EA}} = [0 \cdots 0 \quad 1 \quad 0 \cdots 0]\]
where the \(i\)-th entry is 1 and all other entries are 0. 

Similarly, for the dual basis \(\mathcal{D}\), 
\[[\psi_j \mathbf{w}_k]_{\mathcal{E}} = [\psi_j]_{\mathcal{EB}} [\mathbf{w}_k]_{\mathcal{B}} = 0\]
when \(j \ne k\) and 
\[[\psi_j \mathbf{w}_j]_{\mathcal{E}} = [\psi_j]_{\mathcal{EB}} [\mathbf{w}_j]_{\mathcal{B}} = 1.\]
So the matrix \([\psi_j]_{\mathcal{EB}}\) is a row vector with the \(j\)-th entry 1 and all other entries 0. 

\textcolor{purple}{However, when interpreted as vectors of a vector space, whether \(W'\) or \(V'\), the coordinate vectors written with respect to bases \(\mathcal{D}\) and \(\mathcal{C}\) respectively, are column vectors}, because the matrix representation of \(T'\) is defined to map column vectors to column vectors. 

Similar to the above general rule of defining the matrix representation of \(T\), the \(l\)-th column vector of \(\mathcal{M}(T') = [T']_{\mathcal{CD}}\) is \(T' (\psi_l)_{\mathcal{C}}\). 
\begin{theorem}[matrix of \(T'\) is transpose of matrix \(T\)]
Suppose \( V \) and \( W \) are finite-dimensional and \( T \in \mathcal{L}(V, W) \). Then
\[
\mathcal{M}(T') = \left( \mathcal{M}(T) \right)^T.
\]
\end{theorem}
\begin{proof}
Suppose \(B\) is the matrix representation of \(T'\), i.e., the \(l\)-th column vector of \(B\) is 
\[[T' \psi_l]_{\mathcal{C}} = [T']_{\mathcal{CD}} [\psi_l]_{\mathcal{D}}.\]
Suppose it is 
\[\begin{bmatrix}
b_1^l \\
b_2^l \\
\vdots \\
b_n^l
\end{bmatrix}.
\]
Then 
\[[T' \psi_l]_{\mathcal{C}} = [\psi_l \circ T]_{\mathcal{C}} \text{ is } \begin{bmatrix}
b_1^l \\
b_2^l \\
\vdots \\
b_n^l
\end{bmatrix}.\]
This means, as real vector values, we have 
\[\psi_l \circ T = b_1^l \varphi_1 + b_2^l \varphi_2 + \cdots + b_n^l \varphi_n.\]
Now written into matrix representations again, we have 
\[[\psi_l]_{\mathcal{EB}} [T]_{\mathcal{BA}} = [b_1^l \varphi_1 + b_2^l \varphi_2 + \cdots + b_n^l \varphi_n]_{\mathcal{EA}}.\]
For the left hand side, since \([\psi_l]_{\mathcal{EB}}\) is a row vector with the \(l\)-th entry is 1 and all the other entries 0, \([\psi_l]_{\mathcal{EB}} [T]_{\mathcal{BA}}\) is the \(l\)-th row vector of \([T]_{\mathcal{BA}}\). For the right hand side, since 
\[[b_1^l \varphi_1 + b_2^l \varphi_2 + \cdots + b_n^l \varphi_n]_{\mathcal{EA}} = b_1^l [\varphi_1]_{\mathcal{EA}} + b_2^l [\varphi_2]_{\mathcal{EA}} + \cdots + b_n^l [\varphi_n]_{\mathcal{EA}},\] 
it is 
\[[b_1^l \quad b_2^l \cdots b_n^l].\]
Therefore, the \(l\)-th column of \(\mathcal{M}(T')\) is the \(l\)-th row of \(\mathcal{M}(T)\). \(\mathcal{M}(T)^T = \mathcal{M}(T')\). 
\end{proof}
\begin{theorem}
Suppose \(A \in \mathbb{F}^{m,n}\). Then the column rank of \(A\) equals the row rank of \(A\). 
\end{theorem}
\begin{proof}
We have proved this theorem before, but now we offer another proof: 

Define \( T : \mathbb{F}^{n,1} \to \mathbb{F}^{m,1} \) by \( Tx = Ax \). Thus \( \mathcal{M}(T) = A \), where \( \mathcal{M}(T) \) is computed with respect to the standard bases of \( \mathbb{F}^{n,1} \) and \( \mathbb{F}^{m,1} \). Now
\begin{align*}
\text{column rank of } A &= \text{column rank of } \mathcal{M}(T) \\
&= \dim \operatorname{range} T \\
&= \dim \operatorname{range} T' \\
&= \text{column rank of } \mathcal{M}(T') \\
&= \text{column rank of } A^T \\
&= \text{row rank of } A.
\end{align*}
\end{proof}
\newpage
\chapter{Polynomials}
\section{Zeros of polynomials}
Recall that a function \( p : \mathbb{F} \to \mathbb{F} \) is called a polynomial of degree \( m \) if there exist 
\( a_0, \ldots, a_m \in \mathbb{F} \) with \( a_m \ne 0 \) such that
\[
p(z) = a_0 + a_1 z + \cdots + a_m z^m
\]
for all \( z \in \mathbb{F} \). A polynomial could have more than one degree if the representation 
of \( p \) in the form above were not unique. Our first task is to show that this cannot happen.
\begin{definition}[zero of a polynomial]
A number \( \lambda \in \mathbb{F} \) is called a \emph{zero} (or \emph{root}) of a polynomial \( p \in \mathcal{P}(\mathbb{F}) \) if
\[
p(\lambda) = 0.
\]
\end{definition}
\begin{theorem}[each zero of a polynomial corresponds to a degree-one factor]
Suppose \( m \) is a positive integer and \( p \in \mathcal{P}(\mathbb{F}) \) is a polynomial of degree \( m \).  
Suppose \( \lambda \in \mathbb{F} \). Then \( p(\lambda) = 0 \) if and only if there exists a polynomial  
\( q \in \mathcal{P}(\mathbb{F}) \) of degree \( m - 1 \) such that
\[
p(z) = (z - \lambda) q(z)
\]
for every \( z \in \mathbb{F} \).
\end{theorem}
\begin{proof}
\(\Leftarrow\) is trivial. Omitted. For \(\Rightarrow\), note that for any \(a, b \in \mathbb{F}\) and some positive integer \(k\), we have
\[(a-b)(a^k + a^{k-1}b + a^{k-2}b^2 + \cdots + a^2 b^{k-1} + ab^k) = a^{k+1} - b^{k+1}; \tag{7.1.1}\]
since \(p(\lambda) = 0\), 
\[p(z) = p(z) - p(\lambda) = a_m(z^m - \lambda^m)+a_{m-1}(z^{m-1} - \lambda^{m-1}) + \cdots + a_1(z - \lambda),\]
we can write each \(z^j - \lambda^j\) into the product of \((z - \lambda)\) with a degree-\((j-1)\) polynomial. Therefore, we can write \(p(z)\) into the product of \((z - \lambda)\) with a degree-\((m-1)\) polynomial.
\end{proof}
\begin{theorem}[degree \(m\) implies at most \(m\) zeros]
Suppose \( m \) is a positive integer and \( p \in \mathcal{P}(\mathbb{F}) \) is a polynomial of degree \( m \).  Then \( p \) has at most \( m \) zeros in \( \mathbb{F} \).
\end{theorem}
\begin{proof}
By induction, assume we have \(p(\lambda_m) = 0\), then there exists a degree \(m-1\) polynomial \(q_{m-1}(z)\) such that \(p(z) = (z-\lambda_m) q_{m-1}(z)\). Assume \(q_{m-1}(\lambda_{m-1}) = 0\), then we get a degree \(m-2\) polynomial \(q_{m-2}\). Eventually we get \(p(z) = a_m(z-\lambda_m)(z-\lambda_{m-1}) \cdots (z-\lambda_1)\) and the polynomial cannot have any additional zeros. 
\end{proof}
\section{Division algorithm}
\begin{theorem}[division algorithm for polynomials]
Suppose that \( p, s \in \mathcal{P}(\mathbb{F}) \), with \( s \ne 0 \). Then there exist unique polynomials  
\( q, r \in \mathcal{P}(\mathbb{F}) \) such that
\[
p = sq + r
\]
and \( \deg r < \deg s \).
\end{theorem}
\begin{proof}
Let \( n = \deg p \) and let \( m = \deg s \). If \( n < m \), then take \( q = 0 \) and \( r = p \)  
to get the desired equation \( p = sq + r \) with \( \deg r < \deg s \). Thus we now assume that 
\( n \geq m \).

Now we want to show that polynomials \(q\) and \(r\) exists. 

The list
\[
1, z, \ldots, z^{m-1}, s, zs, \ldots, z^{n-m}s \tag{7.2.1}
\]
is linearly independent in \( \mathcal{P}_n(\mathbb{F}) \) because each polynomial in this list has a different degree (\textcolor{blue}{elements in \((7.2.1)\) has degrees \(0, 1, 2, ..., m\)}). Also, the list has length \(n+1\), which is the same as the degree of polynomial \(p\). Therefore polynomial \(p\) can be written into a unique linear combination of \((7.2.1)\). 

Suppose the linear combination is 
\[p(z) = c_n z^{n-m}s + c_{n-1} z^{n-m-1}s + \cdots + c_m s + c_{m-1} z^{m-1} + \cdots + c_1 z + c_0\]
for unique \([c_0, c_1, ..., c_n]^T \in \mathbb{F}^{n+1}\). Then we have 
\[p = s (c_n z^{n-m} + c_{n-1} z^{n-m-1} + \cdots + c_m) + c_{m-1} z^{m-1} + \cdots + c_1 z + c_0,\]
which means 
\[q(z) = c_n z^{n-m} + c_{n-1} z^{n-m-1} + \cdots + c_m\]
and 
\[r(z) = c_{m-1} z^{m-1} + \cdots + c_1 z + c_0,\]
and the two polynomials \(q\) and \(r\) are unique. 

Note that according to the formula, the degree of polynomial \(r\) is at most \(m-1\). 
\end{proof}
\begin{remark}[Another proof for uniqueness]
Suppose polynomials \( r \) and \( q \) exist, but are not unique. Then we have
\[
p(z) = q_1(z)s(z) + r_1(z)
\]
\[
p(z) = q_2(z)s(z) + r_2(z)
\]
where \( q_1(z) \neq q_2(z) \), \( r_1(z) \neq r_2(z) \),
\begin{align*}
0 &= \left(q_1(z)s(z) + r_1(z)\right) - \left(q_2(z)s(z) + r_2(z)\right) \\
  &= (q_1 - q_2)s + (r_1 - r_2)
\end{align*}
Then
\[
(q_1 - q_2)s = r_2 - r_1
\]
However, \( \deg((q_1 - q_2)s) \geq \deg(s) \)
\[
\deg(r_2 - r_1) \leq \max(\deg r_2, \deg r_1)
\]
which contradicts the assumption that
\[
\deg r_1 < \deg s, \quad \deg r_2 < \deg s
\]
Therefore, polynomials \( q \) and \( r \) are unique.
\end{remark}
\section{Factorization of polynomials over \(\mathbb{C}\)}
We have been handling polynomials with complex coefficients and polynomials with real coefficients simultaneously, letting \( \mathbb{F} \) denote \( \mathbb{R} \) or \( \mathbb{C} \). Now we will see differences between these two cases. First we treat polynomials with complex coefficients. Then we will use those results to prove corresponding results for polynomials with real coefficients.
\begin{remark}
\textcolor{ForestGreen}{The fundamental theorem of algebra is an existence theorem. Its proof does not lead to a method for finding zeros. The quadratic formula gives the zeros explicitly for polynomials of degree 2. Similar but more complicated formulas exist for polynomials of degree 3 and 4. No such formulas exist for polynomials of degree 5 and above.}
\end{remark}
\begin{theorem}[Fundamental theorem of algebra, first version]
Every non-constant polynomial with complex coefficients has a zero in \(\mathbb{C}\). 
\end{theorem}
\begin{proof}
First of all, every complex number has a \(k\)-th root, for any positive integer \(k\).

Suppose \(p\) is a non-constant polynomial with complex coefficients and highest-order nonzero term \(c_m z^m\). Then 
\[|p(z)| \to \infty \text{ as } z \to \infty.\]
Therefore, the continuous function \(z \mapsto |p(z)|\) has global minimum(s) at some point(s). We denote one of the minimums as \(\eta \in \mathbb{C}\), and we want to show that \(|p(\eta)| = 0\). 

Assume \(|p(\eta)| \neq 0\). Then we can define a new polynomial
\[q(z) = \frac{p(z+\eta)}{p(\eta)}\]
which is 
\[q(z) = \frac{c_m}{p(\eta)}(z+\eta)^m + \frac{c_{m-1}}{p(\eta)}(z+\eta)^{m-1} + \cdots + \frac{c_1}{p(\eta)}(z+\eta) + \frac{c_0}{p(\eta)},\]
and the function \(z \mapsto |q(z)|\) has a global minimum at \(0\) and \(|q(0)| = q(0) = 1\). 

Now we denote 
\[q(z) = 1 + a_k z^k + \cdots + a_m z^m,\]
where \(k\) is the smallest positive integer such that the coefficient of \(z^k\) is nonzero. However, \(z \mapsto |q(z)|\) is a non-constant holomorphic function, so when we pick \(U\) as the unit circle in \(\mathbb{C}\) centered at \(0\), its global minimum would be on the boundary of \(U\). Therefore, \(0\), which is an interior point of the region \(U\), cannot be the global minimum. Contradiction. 
\end{proof}
\begin{theorem}[Fundamental theorem of algebra, second version]
If \( p \in \mathcal{P}(\mathbb{C}) \) is a non-constant polynomial, then \( p \) has a unique factorization (except for the order of the factors) of the form
\[
p(z) = c(z - \lambda_1) \cdots (z - \lambda_m),
\]
where \( c, \lambda_1, \ldots, \lambda_m \in \mathbb{C} \).
\end{theorem}
\begin{proof}
Let \( p \in \mathcal{P}(\mathbb{C}) \) and let \( m = \deg p \). We will use induction on \( m \). If \( m = 1 \), then the desired factorization exists and is unique. So assume that \( m > 1 \) and that the desired factorization exists and is unique for all polynomials of degree \( m - 1 \).

First we will show that the desired factorization of \( p \) exists. By the first version of the fundamental theorem of algebra, \( p \) has a zero \( \lambda \in \mathbb{C} \). By 4.6, there is a polynomial \( q \) of degree \( m - 1 \) such that
\[
p(z) = (z - \lambda) q(z)
\]
for all \( z \in \mathbb{C} \). Our induction hypothesis implies that \( q \) has the desired factorization, which when plugged into the equation above gives the desired factorization of \( p \).

Now we turn to the question of uniqueness. The number \( c \) is uniquely determined as the coefficient of \( z^m \) in \( p \). So we only need to show that except for the order, there is only one way to choose \( \lambda_1, \ldots, \lambda_m \). If
\[
(z - \lambda_1) \cdots (z - \lambda_m) = (z - \tau_1) \cdots (z - \tau_m)
\]
for all \( z \in \mathbb{C} \), then because the left side of the equation above equals 0 when \( z = \lambda_1 \), one of the \( \tau \)'s on the right side equals \( \lambda_1 \). Relabeling, we can assume that \( \tau_1 = \lambda_1 \). Now if \( z \ne \lambda_1 \), we can divide both sides of the equation above by \( z - \lambda_1 \), getting
\[
(z - \lambda_2) \cdots (z - \lambda_m) = (z - \tau_2) \cdots (z - \tau_m)
\]
for all \( z \in \mathbb{C} \) except possibly \( z = \lambda_1 \). Actually the equation above holds for all \( z \in \mathbb{C} \), because otherwise by subtracting the right side from the left side we would get a nonzero polynomial that has infinitely many zeros. The equation above and our induction hypothesis imply that except for the order, the \( \lambda \)'s are the same as the \( \tau \)'s, completing the proof of uniqueness.
\end{proof}
\section{Factorization of polynomials over \(\mathbb{R}\)}
\begin{theorem}[polynomials with real coefficients have nonreal zeros in pairs]
Suppose \( p \in \mathcal{P}(\mathbb{C}) \) is a polynomial with real coefficients.  
If \( \lambda \in \mathbb{C} \) is a zero of \( p \), then so is \( \overline{\lambda} \).
\end{theorem}
\begin{proof}
Let
\[
p(z) = a_0 + a_1 z + \cdots + a_m z^m,
\]
where \( a_0, \ldots, a_m \) are real numbers. Suppose \( \lambda \in \mathbb{C} \) is a zero of \( p \). Then
\[
a_0 + a_1 \lambda + \cdots + a_m \lambda^m = 0.
\]
Take the complex conjugate of both sides of this equation, obtaining
\[
a_0 + a_1 \overline{\lambda} + \cdots + a_m \overline{\lambda}^m = 0,
\]
where we have used basic properties of the complex conjugate. The equation above shows that \( \overline{\lambda} \) is a zero of \( p \).
\end{proof}
\begin{theorem}[factorization of a quadratic polynomial]
Suppose \( b, c \in \mathbb{R} \). Then there is a polynomial factorization of the form
\[
x^2 + bx + c = (x - \lambda_1)(x - \lambda_2)
\]
with \( \lambda_1, \lambda_2 \in \mathbb{R} \) if and only if \( b^2 \geq 4c \).
\end{theorem}
Proof omitted. 
\begin{theorem}[factorization of a polynomial over \(\mathbb{R}\)]
Suppose $p \in \mathcal{P}(\mathbb{R})$ is a non-constant polynomial. Then $p$ has a unique factorization (except for the order of the factors) of the form
\[
p(x) = c(x - \lambda_1)\cdots(x - \lambda_m)(x^2 + b_1x + c_1)\cdots(x^2 + b_Mx + c_M),
\]
where $c, \lambda_1, \ldots, \lambda_m, b_1, \ldots, b_M, c_1, \ldots, c_M \in \mathbb{R}$, with $b_k^2 < 4c_k$ for each $k$.
\end{theorem}
\begin{proof}
We first write the factorization of the polynomial in complex coefficients, then sort the zeros into real ones and complex ones. We can see that the real zeros are singletons, while the complex zeros come in pairs. When we come across a real zero, we factorize it alone. When we come across a pair of complex zeros, we factorize them together, then combine the factors into a quadratic polynomial. 
\end{proof}
\newpage
\chapter{Eigenvalues and eigenvectors}
\section{Invariant subspaces}
\begin{definition}
A linear map from a vector space to itself is called an \textit{operator}.
\end{definition}
Suppose \( T \in \mathcal{L}(V) \). If \( m \geq 2 \) and
\[
V = V_1 \oplus \cdots \oplus V_m,
\]
where each \( V_k \) is a nonzero subspace of \( V \), then to understand the behavior of \( T \) we only need to understand the behavior of each \( T|_{V_k} \); here \( T|_{V_k} \) denotes the restriction of \( T \) to the smaller domain \( V_k \). Dealing with \( T|_{V_k} \) should be easier than dealing with \( T \) because \( V_k \) is a smaller vector space than \( V \).

However, to let the above process make sense, we need to make sure that \(T |_{V_k}\) maps \(V_k\) to itself, for each \(k\). This leads to the following definition:
\begin{definition}
Suppose \( T \in \mathcal{L}(V) \). A subspace \( U \) of \( V \) is called \textit{invariant} under \( T \) if \( Tu \in U \) for every \( u \in U \).
\end{definition}
\begin{corollary}
\(U\) is invariant under \(T\) if \(T|_{U}\) is an operator on \(U\). 
\end{corollary}
\begin{example}
Subspaces of the polynomial space that has degree \(n\) or lower is invariant under the differentiation operator. 
\end{example}
\begin{example}
If \( T \in \mathcal{L}(V) \), then the following subspaces of \( V \) are all invariant under \( T \).
\begin{itemize}
  \item \( \{0\} \) \quad The subspace \( \{0\} \) is invariant under \( T \) because if \( u \in \{0\} \), then \( u = 0 \) and hence \( Tu = 0 \in \{0\} \).
  
  \item \( V \) \quad The subspace \( V \) is invariant under \( T \) because if \( u \in V \), then \( Tu \in V \).
  
  \item \( \text{null } T \) \quad The subspace \( \text{null } T \) is invariant under \( T \) because if \( u \in \text{null } T \), then \( Tu = 0 \), and hence \( Tu \in \text{null } T \).
  
  \item \( \text{range } T \) \quad The subspace \( \text{range } T \) is invariant under \( T \) because if \( u \in \text{range } T \), then \( Tu \in \text{range } T \).
\end{itemize}
\end{example}
\begin{remark}
\textcolor{ForestGreen}{Must an operator \( T \in \mathcal{L}(V) \) have any invariant subspaces other than \( \{0\} \) and \( V \)? 
Later we will see that this question has an affirmative answer if \( V \) is finite-dimensional and 
\( \dim V > 1 \) (for \( \mathbb{F} = \mathbb{C} \)) or \( \dim V > 2 \) (for \( \mathbb{F} = \mathbb{R} \)).}
\end{remark}
\section{Eigenvalues}
Now we begin to study the simplest possible nontrivial invariant subspaces: Invariant subspaces of dimension one. 

Take any \( v \in V \) with \( v \ne 0 \) and let \( U \) equal the set of all scalar multiples of \( v \):
\[
U = \{ \lambda v : \lambda \in \mathbb{F} \} = \text{span}(v).
\]
Then \( U \) is a one-dimensional subspace of \( V \) (and every one-dimensional subspace 
of \( V \) is of this form for an appropriate choice of \( v \)). If \( U \) is invariant under an 
operator \( T \in \mathcal{L}(V) \), then \( Tv \in U \), and hence there is a scalar \( \lambda \in \mathbb{F} \) such that
\[
Tv = \lambda v.
\]
Conversely, if \( Tv = \lambda v \) for some \( \lambda \in \mathbb{F} \) and \(v \ne 0\), then \( \operatorname{span}(v) \) is a one-dimensional subspace of \( V \) invariant under \( T \). \textcolor{blue}{Note that given nonzero \(v\), if \(Tv = \lambda v\), then for any vector \(u\) in \(U = \operatorname{span}(v)\), \(T u = \lambda u\).}

\begin{definition}[Eigenvalue]
Suppose \( T \in \mathcal{L}(V) \). A nonzero number \( \lambda \in \mathbb{F} \) is called an eigenvalue of \( T \) if there exists \( v \in V \) such that \( v \ne 0 \) and \( Tv = \lambda v \).
\end{definition}
\begin{remark}
Note that the definition of eigenvalues are based on a specific linear operator, not on its corresponding scalar. 
\end{remark}
\begin{corollary}
Suppose \( V \) is finite-dimensional, \( T \in \mathcal{L}(V) \), and \( \lambda \in \mathbb{F} \). Then the following are equivalent:
\begin{itemize}
    \item[(a)] \( \lambda \) is an eigenvalue of \( T \).
    \item[(b)] \( T - \lambda I \) is not injective.
    \item[(c)] \( T - \lambda I \) is not surjective.
    \item[(d)] \( T - \lambda I \) is not invertible.
\end{itemize}
\end{corollary}
\begin{proof}
\((a) \Longleftrightarrow (b)\), \((a) \Longrightarrow (c)\) and \((a) \Longleftrightarrow (d)\) are trivial. Omitted. For \((a) \Longleftarrow (c)\), since \(T : V \to V\), \((c)\) implies \(\ker (T-\lambda I)\) is nontrivial. Omitted. 
\end{proof}
\begin{definition}
Suppose \( T \in \mathcal{L}(V) \) and \( \lambda \in \mathbb{F} \) is an eigenvalue of \( T \). A vector \( v \in V \) is called an \textit{eigenvector} of \( T \) corresponding to \( \lambda \) if \( v \ne 0 \) and \( Tv = \lambda v \).
\end{definition}
\begin{remark}
For any nonzero \(k\) in \(\mathbb{F}\), \(kv\) is also an eigenvector corresponding to \(\lambda\). Proof omitted. 
\end{remark}
\begin{remark}
\[Tv = \lambda v \Longleftrightarrow (T - \lambda I) v = 0.\]
\end{remark}
\begin{theorem}
Suppose \(T \in \mathcal{L}(V)\). Then every list of eigenvectors of \(T\) corresponding to distinct eigenvalues of \(T\) is linearly independent. 
\end{theorem}
\begin{proof}
Assume the list of eigenvectors, denoted \(v_1, v_2, ..., v_n\) contain finitely many elements. (We will later show that it is true.) Suppose those eigenvectors have corresponding eigenvalues \(\lambda_1, \lambda_2, ..., \lambda_n \in \mathbb{F}\). 

We now prove by induction: First of all, the first two vectors \(v_1\) and \(v_2\) are linearly independent. Proof omitted. 

Second, assume \(v_3\) can be written as a linear combination of \(v_1\) and \(v_2\), namely \(v_3 = k_1 v_1 + k_2 v_2\) for scalars \(k_1, k_2\). Then 
\[T v_3 = \lambda_3 v_3 = \lambda_3 k_1 v_1 + \lambda_3 k_2 v_2\]
and
\[T v_3 = k_1 \lambda_1 v_1 + k_2 \lambda_2 v_2,\]
but \(\lambda_3 \ne \lambda_1\) and \(\lambda_3 \ne \lambda_2\) implies the two linear combinations are different, which causes the vector value to be different (since they are different linear combinations of two linearly independent vectors). Therefore we reach a contradiction, and \(v_1, v_2, v_3\) are linearly independent vectors. 

Third, assume vectors \(v_1, ..., v_{n-1}\) are linearly independent. Then if \(v_n\) is not linearly independent with them, we would have 
\[ \lambda_n v_n = \lambda_n k_1 v_1 + ..., +\lambda_n k_{n-1} v_{n-1}\]
and
\[\lambda_n v_n = k_1 \lambda_1 v_1 + ..., + \lambda_n k_{n-1} \lambda_{n-1},\]
which reaches contradiction. 

Therefore, the list of eigenvectors are linearly independent. 

\textcolor{blue}{Another proof from the book:}

Suppose the desired result is false. Then there exists a smallest positive 
integer \( m \) such that there exists a linearly dependent list 
\( v_1, \ldots, v_m \) of eigenvectors of \( T \) corresponding to 
distinct eigenvalues \( \lambda_1, \ldots, \lambda_m \) of \( T \) 
(note that \( m \geq 2 \) because an eigenvector is, by definition, 
nonzero). Thus there exist \( a_1, \ldots, a_m \in \mathbb{F} \), 
none of which are 0 (because of the minimality of \( m \)), such that
\[
a_1 v_1 + \cdots + a_m v_m = 0.
\]
Apply \( T - \lambda_m I \) to both sides of the equation above, getting
\[
a_1(\lambda_1 - \lambda_m)v_1 + \cdots + a_{m-1}(\lambda_{m-1} - \lambda_m)v_{m-1} = 0.
\]
Because the eigenvalues \( \lambda_1, \ldots, \lambda_m \) are distinct, 
none of the coefficients above equal 0. Thus \( v_1, \ldots, v_{m-1} \) 
is a linearly dependent list of \( m - 1 \) eigenvectors of \( T \) 
corresponding to distinct eigenvalues, contradicting the minimality of \( m \). 
This contradiction completes the proof.
\end{proof}
\begin{corollary}
Suppose \(V\) is finite-dimensional. Then each operator on \(V\) has at most \(\dim V\) distinct eigenvalues. 
\end{corollary}
Proof omitted. 
\section{Polynomials applied to operators}
\begin{definition}[notation: \(T^m\)]
Suppose \( T \in \mathcal{L}(V) \) and \( m \) is a positive integer.
\begin{itemize}
  \item \( T^m \in \mathcal{L}(V) \) is defined by 
  \[
  T^m = \underbrace{T \cdots T}_{m \text{ times}}.
  \]
  
  \item \( T^0 \) is defined to be the identity operator \( I \) on \( V \).
  
  \item If \( T \) is invertible with inverse \( T^{-1} \), then \( T^{-m} \in \mathcal{L}(V) \) is defined by
  \[
  T^{-m} = (T^{-1})^m.
  \]
\end{itemize}
\end{definition}
\begin{definition}[notation \(p(T)\)]
Suppose \( T \in \mathcal{L}(V) \) and \( p \in \mathcal{P}(\mathbb{F}) \) is a polynomial given by
\[
p(z) = a_0 + a_1 z + a_2 z^2 + \cdots + a_m z^m
\]
for all \( z \in \mathbb{F} \). Then \( p(T) \) is the operator on \( V \) defined by
\[
p(T) = a_0 I + a_1 T + a_2 T^2 + \cdots + a_m T^m.
\]
\end{definition}
\begin{definition}[products of polynomials]
If \( p, q \in \mathcal{P}(\mathbb{F}) \), then \( pq \in \mathcal{P}(\mathbb{F}) \) is the polynomial defined by
\[
(pq)(z) = p(z) \, q(z)
\]
for all \( z \in \mathbb{F} \).
\end{definition}
\begin{corollary}[multiplicative properties]
Suppose \( p, q \in \mathcal{P}(\mathbb{F}) \) and \( T \in \mathcal{L}(V) \). Then  
\begin{itemize}
  \item[(a)] \( (pq)(T) = p(T) q(T); \)
  \item[(b)] \( p(T) q(T) = q(T) p(T). \)
\end{itemize}
\textcolor{red}{Note that this is a case for polynomials to be commutative.} Proof omitted. 
\end{corollary}
\begin{theorem}
Suppose \( T \in \mathcal{L}(V) \) and \( p \in \mathcal{P}(\mathbb{F}) \). Then \( \text{null}\, p(T) \) and \( \text{range}\, p(T) \) are invariant under \( T \).
\end{theorem}
\begin{proof}
Suppose \(v \in \ker p(T)\), then \(p(T) v = 0\). Then \(p(T) T v = T p(T) v = 0\). \(\ker p(T)\) is invariant under \(T\). 

Suppose \(v \in \operatorname{range} p(T)\). Since \(p(T) (Tv) \in \operatorname{range} p(T)\), this subset is also invariant under \(T\). 
\end{proof}
\section{Existence of eigenvalues on complex vector spaces}
\begin{theorem}
Every operator on a finite-dimensional nonzero complex vector space has an eigenvalue. 
\end{theorem}
\begin{proof}
Pick any nonzero vector \(v \in V\), where \(V\) is the nonzero complex vector space with finite dimension. Then for the operator \(T\), there are at most finitely many vectors, \(v, Tv, T^2 v, ..., T^{M} v\), that are linearly dependent. We pick the minimum number \(n\) such that the \(n+1\) vectors \(v, Tv, T^2 v, ..., T^n v\) are linearly dependent. Then there are complex coefficients \(a_0, a_1, ..., a_n\) such that 
\[a_0 v + a_1 T v + a_2 T^2 v + ... + a_n T^n v = 0.\]
Therefore, let \(p(z) = a_n z^n + a_{n-1} z^{n-1} + ... + a_1 z + a_0\), we have \(p(T) v = 0\). Since such a polynomial has \(n\) roots, as we previously discussed, now we have 
\[a_n (T - \lambda_n I) (T-\lambda_{n-1} I) ... (T - \lambda_1 I) v = 0.\]
Now let us name \(n\) polynomials of degree \(n-1\), that for each \(k = 1, 2, ..., n\), we define polynomial
\[q_k (z) = a_n (z - \lambda_n) (z - \lambda_{n-1}) ... (z - \lambda_{k+1}) (z - \lambda_{k-1}) ... (z - \lambda_1).\]
Now we have 
\[(T - \lambda_k) q_k (T) v = 0.\]
Since \(q_k\) is a polynomial with degree \(n-1\), it is a linear combination of vectors 
\[v, Tv, T^2 v, ..., T^{n-1} v.\] 
\textcolor{red}{Recall that the vectors \(v, Tv, T^2 v, ..., T^n v\) are of the minimum number to be linearly dependent. This means the rest of the vectors \(v, Tv, T^2 v, ..., T^{n-1} v\) are linearly independent. Every \(q_k (T) v\) is a nontrivial (because it has degree \(n-1\)) linear combination of the vectors \(v, Tv, T^2 v, ..., T^{n-1} v\), which means it is nonzero.} Therefore every \(\lambda_k\) is an eigenvalue of \(T\), with corresponding eigenvector \(q_k (T) v \ne 0\). 
\end{proof}
\begin{remark}
Therefore, given \(T \in \mathcal{L}(V)\), where \(V\) is an \(n\)-dimensional vector space over \(\mathbb{C}\), \(T\) has at most \(n\) eigenvalues and at least one eigenvalue. 
\end{remark}
\begin{remark}
Suppose \(T: V \to V\), where \(V\) is an \(n\)-dimensional vector space over \(\mathbb{C}\). \textcolor{red}{If there exists \(v\) in \(V\) such that}
\textcolor{red}{\[\{v, Tv, T^v, ..., T^m v\} \text{ are linearly independent, and}\]}
\textcolor{red}{\[T^{m+1} v \in \operatorname{span} \{v, Tv, T^2 v, ..., T^m v\},\]}
\textcolor{red}{we can only conclude that \(T\) has at least \(m\) eigenvalues, but we cannot conclude that \(T\) has exactly \(m\) eigenvalues.}

The explaination is simple: \textcolor{ForestGreen}{The existence of such a \(v\) does not eliminate the possibility of the existence of some \(w \in V\), such that}
\textcolor{ForestGreen}{\[\{w, Tw, T^w, ..., T^l w\} \text{ are linearly independent, and}\]}
\textcolor{ForestGreen}{\[T^{l+1} w \in \operatorname{span} \{w, Tw, T^2 w, ..., T^l w\}, \text{ for some } l > m.\]}
\end{remark}
\begin{example}
Define \( T \in \mathcal{L}(\mathcal{P}(\mathbb{C})) \) by \( (Tp)(z) = zp(z) \). If \( p \in \mathcal{P}(\mathbb{C}) \) is a nonzero polynomial, then the degree of \( Tp \) is one more than the degree of \( p \), and thus \( Tp \) cannot equal a scalar multiple of \( p \). Hence \( T \) has no eigenvalues.

Because \( \mathcal{P}(\mathbb{C}) \) is infinite-dimensional, this example does not contradict the result above.
\end{example}
\section{Eigenvalues and the minimal polynomial}
\begin{definition}[monic polynomial]
A monic polynomial is a polynomial whose highest-degree coefficient equals to 1. 
\end{definition}
\begin{theorem}[Existence, uniqueness, and degree of minimal polynomial]
Suppose \( V \) is finite-dimensional and \( T \in \mathcal{L}(V) \). Then there is a unique monic polynomial \( p \in \mathcal{P}(\mathbb{F}) \) of smallest degree such that \( p(T) = 0 \). Furthermore, \textcolor{purple}{\( \deg p \leq \dim V \)}.
\end{theorem}
\begin{proof}
Pick any basis 
\[\{v_1, v_2, ..., v_n\}\]
for \(V\), then there is a polynomial of \(T\), denoted \(p_i (T)\) for each $v_i$, such that \(p_i(T) v_i = 0\). Therefore, 
\[p_1 (T) p_2 (T) ... p_n (T) v = 0 \text{ for any } v \in V,\]
which means \(p_1 (T) p_2 (T) ... p_n (T) = 0\). Therefore we can make sure that the degree of the polynomial is less than or equal to \(n^2\). 

Now let us show that the degree of such a polynomial is actually smaller than or equal to \(n\):
\begin{itemize}
    \item Recall that for a vector \(v \in V\), when \(\dim V = n\), the vectors 
    \[v, Tv, T^2 v, ..., T^n v\]
    are linearly dependent, so there exists a smallest integer \(m\) such that \(m \leq n\) and 
    \[v, Tv, T^2 v, ..., T^m v\]
    are linearly dependent, which means there exists a polynomial \(p(T)\) such that 
    \[p(T) v = [T^m + a_{m-1} T^{m-1} + ... + a_1 T + a_0] v = 0.\]
    Now we factorize \(p(T) v\) into 
    \[p(T) v = (T - \alpha_1 I)(T - \alpha_2 I)...(T - \alpha_m I)v,\]
    then no matter whether those \(\alpha\)'s contain multiplicities, the vectors 
    \[\{q_1(T) v = (T - \alpha_2 I)...(T - \alpha_m I)v \text{ (which is a linear combination of }v, Tv, ..., T^{m-1}v),\]
    \[q_2 (T) v = (T - \alpha_3 I)...(T - \alpha_m I)v \text{ (which is a linear combination of }v, Tv, ..., T^{m-2}v),\]
    \[q_3 (T) v = (T - \alpha_4 I)...(T - \alpha_m I)v \text{ (which is a linear combination of }v, Tv, ..., T^{m-3}v),\]
    \[\vdots\]
    \[q_{m-1} (T) v = (T - \alpha_m I)v \text{ (which is a linear combination of }v, Tv),\]
    \[q_m (T) v = v \text{ (which is a linear combination of }v)\}\]
    are linearly independent. 
    \item Pick a basis
    \[\{b_1, b_2, ..., b_n\}\]
    for \(V\). Suppose \(p_1 (T)\) is the monic polynomial of the smallest degree such that \(p_1 (T) b_1 = 0\), with \(\deg p_1 = d_1 \leq n\); \(p_2(T)\) is the monic polynomial of the smallest degree such that \(p_2(T) b_2 = 0\), with \(\deg p_2 = d_2 \leq n\), \(\cdots\), \(p_n(T)\) is the monic polynomial of the smallest degree such that \(p_n (T) b_n = 0\), with \(\deg p_n = d_n \leq n\). 
    \item Now we factorize each polynomial:
    \[p_1(T) = (T - \lambda_{1, 1} I)(T - \lambda_{1, 2} I) ... (T - \lambda_{1, d_1} I);\]
    \[p_2(T) = (T - \lambda_{2, 1} I)(T - \lambda_{2, 2} I) ... (T - \lambda_{2, d_2} I);\]
    \[p_3(T) = (T - \lambda_{3, 1} I)(T - \lambda_{3, 2} I) ... (T - \lambda_{3, d_3} I);\]
    \[\vdots\]
    \[p_n(T) = (T - \lambda_{n, 1} I)(T - \lambda_{n, 2} I) ... (T - \lambda_{n, d_n} I).\]
    Note that, since each of the above polynomials are of the smallest degree, the numbers 
    \[\lambda_{1, 1}, \lambda_{1, 2}, ..., \lambda_{1, d_1},\]
    \[\lambda_{2, 1}, \lambda_{2, 2}, ..., \lambda_{2, d_2},\]
    \[\lambda_{3, 1}, \lambda_{3, 2}, ..., \lambda_{3, d_3},\]
    \[\vdots\]
    \[\lambda_{n, 1}, \lambda_{n, 2}, ..., \lambda_{n, d_n}\]
    are all eigenvectors. 
    \item For all \(i, j\), \(\lambda_{i, j}\) has a corresponding eigenvector
    \[(T - \lambda_{i, 1} I)(T - \lambda_{i, 2} I)...(T - \lambda_{i, j-1} I)(T - \lambda_{i, j+1} I)...(T - \lambda_{i, d_i} I)b_i.\]
    For each \(i, j\), we normalize every eigenvector, and denote them as \(k_{i, j}\), where 
    \[k_{i, j} = \frac{(T - \lambda_{i, 1} I)(T - \lambda_{i, 2} I)...(T - \lambda_{i, j-1} I)(T - \lambda_{i, j+1} I)...(T - \lambda_{i, d_i} I)b_i}{|(T - \lambda_{i, 1} I)(T - \lambda_{i, 2} I)...(T - \lambda_{i, j-1} I)(T - \lambda_{i, j+1} I)...(T - \lambda_{i, d_i} I)b_i|}.\]
    \item Let 
    \[S = \{(\lambda_{1, 1}, k_{1, 1}), (\lambda_{1, 2}, k_{1, 2}), ..., (\lambda_{1, d_1}, k_{1, d_1}),\]
    \[(\lambda_{2, 1}, k_{2, 1}), (\lambda_{2, 2}, k_{2, 2}), ..., (\lambda_{2, d_2}, k_{2, d_2}),\]
    \[(\lambda_{3, 1}, k_{3, 1}), (\lambda_{3, 2}, k_{3, 2}), ..., (\lambda_{3, d_3}, k_{3, d_3}),\]
    \[\vdots\]
    \[(\lambda_{n, 1}, k_{n, 1}), (\lambda_{n, 2}, k_{n, 2}), ..., (\lambda_{n, d_n}, k_{n, d_n})\}.\]
    Now since \(S\) is a set, elements representing the same eigenvalues corresponding to the same eigenvectors are merged. 
    \item Now we group elements of \(S\) by the eigenvalues, i.e., elements with the same eigenvalue are put in the same group. We label the subgroups of \(S\) by \(S_1, S_2, ..., S_m\), with corresponding eigenvalues (now distinct), after relabeling, denoted as \(\lambda_1, \lambda_2, ..., \lambda_m\). 
    \item We relabel the eigenvectors for each eigenvalue \(\lambda_i\), and denote those subgroups of \(S\) as
    \[S_1 = \{(\lambda_1, k_{1, 1}), (\lambda_1, k_{1, 2}), ..., (\lambda_1, k_{1, h_1})\};\]
    \[S_2 = \{(\lambda_2, k_{2, 1}), (\lambda_2, k_{2, 2}), ..., (\lambda_2, k_{2, h_2})\};\]
    \[S_3 = \{(\lambda_3, k_{3, 1}), (\lambda_3, k_{3, 2}), ..., (\lambda_3, k_{3, h_3})\};\]
    \[\vdots\]
    \[S_m = \{(\lambda_m, k_{m, 1}), (\lambda_m, k_{m, 2}), ..., (\lambda_m, k_{m, h_m})\}.\]
    \item Let 
    \[K_1 = \{k_{1, 1}, k_{1, 2}, ..., k_{1, h_1}\};\]
    \[K_2 = \{k_{2, 1}, k_{2, 2}, ..., k_{2, h_2}\};\]
    \[K_3 = \{k_{3, 1}, k_{3, 2}, ..., k_{3, h_3}\};\]
    \[\vdots\]
    \[K_m = \{k_{m, 1}, k_{m, 2}, ..., k_{m, h_m}\}.\]
    For each \(k_{i, j} \in K_i\), for \(j = 1, 2, ..., h_i\), if \(k_{i, j}\) can be written into a linear combination of the other vectors in \(K_i\), we update \(K_i\) with \(k_{i, j}\) removed. If not, keep \(K_i\) the same. Now after those steps of updating every \(K_i\), each \(K_i\) represents a set of linearly independent eigenvectors corresponding to \(\lambda_i\). 
    \item Recall that eigenvectors corresponding to distinct eigenvectors are linearly independent. Then 
    \[K = K_1 \bigsqcup K_2 \bigsqcup ... \bigsqcup K_m\]
    is a set of linearly independent vectors in \(V\), which means 
    \[|K| = |K_1| + |K_2| + ... + |K_m| \leq m.\]
    \item We claim that \(p(T)\) defined by
    \[p(T) = (T - \lambda_1 I)^{|K_1|} (T - \lambda_2 I)^{|K_2|} ... (T - \lambda_m I)^{|K_m|}\]
    has degree \(\leq n\), and it divides every polynomial \(p_1 (T), p_2(T), ..., p_n(T)\) defined as above. 
    \item The claim that \(p(T)\) has degree less than or equal to \(n\) is trivial. 
    \item Now recalling the first point in the proof, we can tell that, if for some \(i = 1, ..., n\), by re-labeling, we have
    \[p_i (T) = (T - \lambda_1 I)^{e_1} (T - \lambda_2 I)^{e_2} ... (T - \lambda_m I)^{e_m},\]
    then we can get \(e_j\) linearly independent eigenvectors corresponding to \(\lambda_j\), for each \(j = 1, 2, ..., m\). Therefore, if \((T - \lambda_j)\) has the highest power \(E_j\) in \(p_l(T)\), there will be at least \(E_j\) vectors in \(K_j\). 
    \item Since the polynomial we found eliminates every vector of a basis, it eliminates every vector in the vector space \(V\). 
\end{itemize}
Now we get existence, then uniqueness is trivial: Suppose there are two different monic polynomials of the same degree that can eliminate all vectors in \(V\), then their difference would also eliminate all vectors, but of a smaller degree. Contradiction. 

\textcolor{blue}{Another proof from the book:}

If \(\dim V = 0\), then \(I\) is the zero operator on \(V\) and thus we take \(p\) to be the constant polynomial \(1\).

Now use induction on \(\dim V\). Thus assume that \(\dim V > 0\) and that the desired result is true for all operators on all vector spaces of smaller dimension. Let \(u \in V\) be such that \(u \ne 0\). The list \(u, Tu, \ldots, T^{\dim V} u\) has length \(1 + \dim V\) and thus is linearly dependent. By the linear dependence lemma, there is a smallest positive integer \(m \le \dim V\) such that \(T^m u\) is a linear combination of \(u, Tu, \ldots, T^{m-1}u\). Thus there exist scalars \(c_0, c_1, c_2, \ldots, c_{m-1} \in \mathbb{F}\) such that
\[
c_0 u + c_1 Tu + \cdots + c_{m-1} T^{m-1} u + T^m u = 0. \tag{8.5.1}
\]
Define a monic polynomial \(q \in \mathcal{P}_m(\mathbb{F})\) by
\[
q(z) = c_0 + c_1 z + \cdots + c_{m-1} z^{m-1} + z^m.
\]
Then (8.5.1) implies that \(q(T)u = 0\).

If \(k\) is a nonnegative integer, then
\[
q(T)(T^k u) = T^k(q(T)u) = T^k(0) = 0.
\]
The linear dependence lemma (2.19) shows that \(u, Tu, \ldots, T^{m-1}u\) is linearly independent. Thus the equation above implies that \(\dim \operatorname{null} q(T) \ge m\). Hence
\[
\dim \operatorname{range} q(T) = \dim V - \dim \operatorname{null} q(T) \le \dim V - m.
\]
Because \(\operatorname{range} q(T)\) is invariant under \(T\), we can apply our induction hypothesis to the operator \(T|_{\operatorname{range} q(T)}\) on the vector space \(\operatorname{range} q(T)\). Thus there is a monic polynomial \(s \in \mathcal{P}(\mathbb{F})\) with
\[
\deg s \le \dim V - m \quad \text{and} \quad s(T|_{\operatorname{range} q(T)}) = 0.
\]
Hence for all \(v \in V\) we have
\[
(sq(T))(v) = s(T)(q(T)v) = 0
\]
because \(q(T)v \in \operatorname{range} q(T)\) and \(s(T)|_{\operatorname{range} q(T)} = s(T|_{\operatorname{range} q(T)}) = 0\). Thus \(sq\) is a monic polynomial such that \(\deg sq \le \dim V\) and \((sq)(T) = 0\).

The paragraph above shows that there is a monic polynomial of degree at most \(\dim V\) that when applied to \(T\) gives the \(0\) operator. Thus there is a monic polynomial of smallest degree with this property, completing the existence part of this result.

\textcolor{red}{Note: Both proofs indicate that the eliminating polynomial of the smallest degree of any nonzero vector divides the minimal polynomial of the entire space.}
\end{proof}
The previous theorem justifies the following definition:
\begin{definition}[the minimal polynomial]
Suppose \(V\) is finite-dimensional and \(T \in \mathcal{L}(V)\). Then the minimal polynomial of \(T\) is the unique monic polynomial \(p \in \mathcal{P}(\mathcal{F})\) of smallest degree such that \(p(T) = 0\). 
\end{definition}
\begin{remark}
To compute the minimal polynomial of an operator \( T \in \mathcal{L}(V) \), we need to 
find the smallest positive integer \( m \) such that the equation
\[
c_0 I + c_1 T + \cdots + c_{m-1} T^{m-1} = -T^m
\]
has a solution \( c_0, c_1, \ldots, c_{m-1} \in \mathbb{F} \). 

If we pick a basis of \( V \) and replace \( T \) in the equation above with the matrix of \( T \), then the equation above can be thought of as a system of \( (\dim V)^2 \) linear equations in the \( m \) unknowns \( c_0, c_1, \ldots, c_{m-1} \in \mathbb{F} \). Gaussian elimination or another fast method of 
solving systems of linear equations can tell us whether a solution exists, testing successive values 
\( m = 1, 2, \ldots \) until a solution exists. By our previous theorem, a solution exists for some smallest positive integer \( m \leq \dim V \). The minimal polynomial of \( T \) is then 
\( c_0 + c_1 z + \cdots + c_{m-1} z^{m-1} + z^m \).

Even faster (usually), pick \( v \in V \) with \( v \neq 0 \) and consider the equation
\[
c_0 v + c_1 T v + \cdots + c_{\dim V - 1} T^{\dim V - 1} v = -T^{\dim V} v.
\]
Use a basis of \( V \) to convert the equation above to a system of \( \dim V \) linear equations 
in \( \dim V \) unknowns \( c_0, c_1, \ldots, c_{\dim V - 1} \). If this system of equations has a 
unique solution \( c_0, c_1, \ldots, c_{\dim V - 1} \) (as happens most of the time), then the scalars 
\( c_0, c_1, \ldots, c_{\dim V - 1}, 1 \) are the coefficients of the minimal polynomial of \( T \) 
(because the degree of the minimal polynomial is at most \( \dim V \)).
\end{remark}
\begin{theorem}
Suppose \(V\) is finite-dimensional and \(T \in \mathcal{L}(V)\).
\begin{enumerate}
    \item The zeros of the minimal polynomial of \(T\) are the eigenvalues of \(T\).
    \item If \(V\) is a complex vector space, then the minimal polynomial of \(T\) has the form
    \[(z - \lambda_1) \cdots (z - \lambda_m),\]
    where \(\lambda_1, \ldots, \lambda_m\) is a list of all eigenvalues of \(T\), possibly with repetitions.
\end{enumerate}
\end{theorem}
\begin{proof}
Our first proof of the existence of the minimal polynomial have proved both of them. Here is the proof from the book: 
\begin{enumerate}
    \item Let \( p \) be the minimal polynomial of \( T \).

    First suppose \( \lambda \in \mathbb{F} \) is a zero of \( p \). Then \( p \) can be written in the form
    \[
    p(z) = (z - \lambda) q(z),
    \]
    where \( q \) is a monic polynomial with coefficients in \( \mathbb{F} \) (see 4.6). Because \( p(T) = 0 \), we have
    \[
    0 = (T - \lambda I)(q(T)v)
    \]
    for all \( v \in V \). Because \( \deg q = (\deg p) - 1 \) and \( p \) is the minimal polynomial of \( T \), there exists at least one vector \( v \in V \) such that \( q(T)v \ne 0 \). The equation above thus implies that \( \lambda \) is an eigenvalue of \( T \), as desired.

    To prove the other direction, suppose \(\lambda\) is an eigenvalue of \(T\), then there exists a vector \(v\) such that \(T v = \lambda v\). We have \(p(T) v = p(\lambda) v = 0\). Since \(p(\lambda)\) is a scalar and \(p(\lambda) v = 0\), we have \(p(\lambda) = 0\), which means \(\lambda\) is a zero of the minimal polynomial. 
    \item Omitted. 
\end{enumerate}
\end{proof}
\begin{theorem}[\(q(T) = 0 \iff q \) is a polynomial multiple of the minimal polynomial]
Suppose \( V \) is finite-dimensional, \( T \in \mathcal{L}(V) \), and \( q \in \mathcal{P}(\mathbb{F}) \). Then \( q(T) = 0 \) if and only if \( q \) is a polynomial multiple of the minimal polynomial of \( T \).
\end{theorem}
\begin{proof}
Suppose \(q\) is a polynomial multiple of the minimal polynomial. Then \(q(T) = 0\). For the other direction, suppose \(p(T)\) is the minimal polynomial of \(T\). Suppose \(p(T) = 0\), then \(q\) has a degree larger than or equal to the degree of \(p\). By division algorithm, there exists polynomials \(s(T)\) and \(r(T)\), such that \(q = s p + r\) and \(\deg r < \deg p\). Therefore, 
\[0 = q(T) = p(T) s(T) + r(T) = r(T).\]
Therefore, \(q\) is a polynomial multiple of the minimal polynomial \(p\). 
\end{proof}
\begin{theorem}
Suppose \( V \) is finite-dimensional, \( T \in \mathcal{L}(V) \), and \( U \) is a subspace of \( V \) that is invariant under \( T \). Then the minimal polynomial of \( T \) is a polynomial multiple of the minimal polynomial of \( T|_U \).
\end{theorem}
\begin{proof}
By our previous construction of the minimal polynomial, we know that any eliminating polynomial of the smallest degree of any vector in \(V\) is a factor of the minimal polynomial. 

Here is the proof from the book: Suppose \( p \) is the minimal polynomial of \( T \). Thus \( p(T)v = 0 \) for all \( v \in V \). In particular,
\[
p(T)u = 0 \quad \text{for all } u \in U.
\]
Thus \( p(T|_U) = 0 \). The previous theorem implies that \( p \) is a polynomial multiple of the minimal polynomial of \( T|_U \).
\end{proof}
\begin{theorem}
Suppose \(V\) is finite-dimensional, and \(T \in \mathcal{L}(V)\). Then \(T\) is not invertible if and only if the constant term of the minimal polynomial of \(T\) is 0. 
\end{theorem}
\begin{proof}
\(T\) is not invertible \(\Longleftrightarrow\) The kernel of \(T\) is not trivial \(\Longleftrightarrow\) zero is an eigenvalue of \(T\). 
\end{proof}
\section{More on eigenvalues and the minimal polynomial in \(\mathbb{C}\)}
Suppose \(V\) is a finite-dimensional vector space over \(\mathbb{C}\), \(T: V \to V\), with minimal polynomial 
\[p(T) = (T - \lambda_1 I)^{k_1} (T - \lambda_2 I)^{k_2} ... (T - \lambda_n I)^{k_n} \]
for eigenvalues \(\lambda_1, ..., \lambda_n \in \mathbb{C}\), and integers \(k_1, ..., k_n \in \mathbb{N}\). Here are a few theorems regarding this statement:
\begin{theorem}
\(\ker (T - \lambda_i I)^x \subseteq \ker (T - \lambda_i I)^y\) for all integers \(x \leq y\) for all \(i = 1, ..., n\). 
\end{theorem}
Proof omitted.
\begin{theorem}
Suppose 
\[v \in \ker (T - \lambda_i)^x;\]
and
\[v \notin \ker (T - \lambda_i)^{x-1}\]
for some integer \(x \geq 1\). Then 
\[v, Tv, ..., T^n v\]
are linearly dependent (proof trivial), and 
\[v, Tv, ..., T^{n-1} v\]
are linearly independent. 
\end{theorem}
\begin{proof}
Suppose there is an integer \(m < x\) such that \(v, Tv, ..., T^m v\) are linearly dependent, and \(m\) is the smallest integer to have \(v, Tv, ..., T^m v\) linearly dependent. Then there exists a monic polynomial \(p_m(T)\) of degree \(m\), such that \(p_m (T) v = 0\). Denote \(p_x (T) = (T - \lambda I)^x\), then there exists polynomials \(r(T)\) and \(s(T)\), such that 
\[p_x (T) = s(T) p_m (T) + r(T),\]
where \(\deg r < \deg p_m = m\). Therefore \(m\) is not the smallest integer to have \(v, Tv, ..., T^m v\) linearly dependent. Contradiction. Therefore, if 
\[v \in \ker (T - \lambda_i)^x\]
and
\[v \notin \ker (T - \lambda_i)^{x-1}\]
for some \(x\), then \(x\) is the smallest integer to have \(v, Tv, ..., T^x v\) linearly dependent. 
\end{proof}
\begin{theorem}
For any \(i \ne j\), 
\[\ker (T - \lambda_i I)^{k_i} \bigcap \ker (T - \lambda_j I)^{k_j}\]
is \(\{0\}\). 
\end{theorem}
\begin{proof}
Suppose there is 
\[v \in \ker (T - \lambda_i I)^{k_i} \bigcap \ker (T - \lambda_j I)^{k_j},\]
then there exists integers \(1 \leq x \leq k_i\) and \(1 \leq y \leq k_j\), such that 
\[v \in \ker (T - \lambda_i)^x;\]
\[v \notin \ker (T - \lambda_i)^{x-1};\]
\[v \in \ker (T - \lambda_j)^y;\]
\[v \notin \ker (T - \lambda_j)^{y-1}.\]
Then by our previous proof, \(x\) is the smallest integer for \(v, Tv, ..., T^x\) to be linearly independent, and \(y\) is the smallest integer for \(v, Tv, ..., T^x\) to be linearly independent, which implies \(x = y\). Therefore 
\[[(T - \lambda_i I)^x - (T - \lambda_j I)^x ] v = 0,\]
but since both polynomials are monic, the new polynomial 
\[(T - \lambda_i I)^x - (T - \lambda_j I)^x\]
must have smaller degrees than \(x\), for which we get a contradiction. Therefore we have \(v = 0\). 
\end{proof}
\begin{theorem}
Based on the discussion above, we have
\[V = \ker (T - \lambda_1 I)^{k_1} \oplus \ker (T - \lambda_2 I)^{k_2}  \oplus ... \oplus \ker (T - \lambda_n I)^{k_n}.\]
\end{theorem}
\begin{proof}
Based on the previous discussions, it is clear that we have 
\[\ker (T - \lambda_1 I)^{k_1} \oplus \ker (T - \lambda_2 I)^{k_2}  \oplus ... \oplus \ker (T - \lambda_n I)^{k_n} \subseteq V,\]
and the minimal polynomial annihilates 
\[\ker (T - \lambda_1 I)^{k_1} \oplus \ker (T - \lambda_2 I)^{k_2}  \oplus ... \oplus \ker (T - \lambda_n I)^{k_n}.\]
Suppose there exists 
\[v \in V - [\ker (T - \lambda_1 I)^{k_1} \oplus \ker (T - \lambda_2 I)^{k_2}  \oplus ... \oplus \ker (T - \lambda_n I)^{k_n}],\]
then there exists an annihilating polynomial for \(v\) with the smallest degree, denoted \(p(T)\). Since \(p\) must divide the minimal polynomial of the entire space, then we can denote \(p\) as 
\[p(T) = (T - \lambda_1 I)^{e_1}(T - \lambda_2 I)^{e_2} ... (T - \lambda_n I)^{e_n}\]
for some integers \(e_i\) satisfying \(0 \leq e_i \leq k_i\) for each \(i = 1, 2, ..., n\). 
\begin{itemize}
    \item Suppose \(\lambda_1 \times ... \times \lambda_n \ne 0\), then 
    \[(T - \lambda_2 I)^{e_2} ... (T - \lambda_n I)^{e_n} v \in \ker (T - \lambda_1)^{e_1},\]
    so there are constants \(C_l\) in \(\mathbb{C}\) such that 
    \[T^{e_2 + ... + e_n} v + C_1 T^{e_2 + ... + e_n -1} v + ... + C_{e_2 + ... + e_n - 1} T v - \lambda_2 ... \lambda_n v \in \ker (T - \lambda_1)^{e_1},\]
    but \(v \notin \ker (T - \lambda_1)^{e_1}\), so \(v\) can be written as a linear combination of
    \[T^{e_2 + ... + e_n} v, ..., T^2 v, Tv.\]
    However, this implies that the lowest degree annihilating polynomial of \(v\) has a degree smaller than \(e_1 + ... + e_n\), for which we get a contradiction. Therefore 
    \[v \in \ker (T - \lambda_1 I)^{k_1} \oplus \ker (T - \lambda_2 I)^{k_2}  \oplus ... \oplus \ker (T - \lambda_n I)^{k_n}.\]
    \item Suppose \(\lambda_i = 0\) for some \(i = 1, 2, ..., n\). Then 
    \[(T - \lambda_1 I)^{e_1}...(T - \lambda_{i - 1} I)^{e_{i - 1}} (T - \lambda_{i + 1} I)^{e_{i + 1}}... (T - \lambda_n I)^{e_n} v\]
    is in \(\ker (T - \lambda_i)^{e_i}\). Then we can proceed with a similar argument. 
\end{itemize}
\end{proof}
\section{Eigenvalues and odd-dimensional vector spaces}
\begin{theorem}[even-dimensional null space]
Suppose \( \mathbb{F} = \mathbb{R} \) and \( V \) is finite-dimensional. Suppose also that \( T \in \mathcal{L}(V) \) and \( b, c \in \mathbb{R} \) with \( b^2 < 4c \). Then \( \dim \operatorname{null}(T^2 + bT + cI) \) is an even number.
\end{theorem}
\begin{proof}
Let \(W = \ker (T^2 + bT + cI)\). Recall that \(\ker (T^2 + bT + cI)\) is invariant under \(T\), so the subspace \(W \subset V\) is invariant under \(T\). 

Assume \(T\) has an eigenvalue-eigenvector pair in \(W\), and denote it as \(v \in W\). Then \(T v = \lambda v\) for some \(\lambda \in \mathbb{R}\). Therefore we have 
\[0 = T^2 v + bTv + cv = \lambda^2 v + \lambda b v + \lambda c v = (\lambda^2 + b\lambda + c) v\]
where \(v\) is non-zero and \(\lambda^2 + b\lambda + c \neq 0\) for any \(\lambda \in \mathbb{R}\). Therefore we get a contradiction which implies \(T\) does not have any eigenvalue or eigenvector in \(W\). 

Now let us first pick a nonzero vector \(w_1\) in \(W\). Then \(Tw\) is not spanned by \(w\) according to our previous discussion, but \(T^2 w\) can be written as a linear combination of \(w_1\) and \(T w_1\). Suppose \(T^k w_1\) can be written as a linear combination of \(w_1\) and \(T w_1\) for all \(k = 2, 3, ..., m - 1\), then \(T^m w_1 = - b T^{m-1} w_1 - c T^{m-2} w_1\) which is also a linear combination of \(w_1\) and \(T w_1\). Therefore, by mathematical induction, \(T^k w_1\) is in \(\operatorname{span} \{w_1, Tw_1\}\) for all \(k \geq 2\). 

Pick \(w_2 \in W - \operatorname{span}\{w_1, T w_1\}\) that is non-zero. If we can't find such \(w_2\), we are done with the proof; if we can, then it is linearly independent from \(w_1\) and \(T w_1\). Assume \(T w_2 = \alpha w_1 + \beta T w_1\), then 
\[T^2 w_2 = \alpha T w_1 + \beta T^2 w_1\]
which means 
\[-b Tw_2 - cw_2 = \alpha T w_1 + \beta b T w_1 + \beta c w_1\]
\[\implies w_2 \in \operatorname{span} \{w_1, Tw_1\}\]
so we get a contradiction. 

By mathematical induction, suppose we get linearly independent vectors 
\[w_1, T w_1, w_2, Tw_2, ..., w_k, T w_k,\]
and now we picked a nonzero \(w_{k+1}\) that is linearly independent from the previous \(2k\) vectors. Suppose \(T w_{k+1}\) is linearly dependent with them, then 
\begin{align*}
T w_{k+1} & = a_1 w_1 + b_1 T w_1 \\
& + a_2 w_2 + b_2 T w_2 \\
& + \cdots \\
& + a_k w_k + b_k T w_k.
\end{align*}
Therefore 
\begin{align*}
T^2 w_{k+1} & = a_1 T w_1 + b_1 T^2 w_1 \\
& + a_2 T w_2 + b_2 T^2 w_2 \\
& + \cdots \\
& + a_k T w_k + b_k T^2 w_k,
\end{align*}
which is also a linear combination of 
\[w_1, T w_1, w_2, Tw_2, ..., w_k, T w_k,\]
while 
\[T^2 w_{k+1} = -b T w_{k+1} - c w_{k+1},\]
which means \(w_{k+1}\) becomes a linear combination of 
\[w_1, T w_1, w_2, Tw_2, ..., w_k, T w_k,\]
and we get a contradiction. 

Therefore, when a new vector \(w\) is picked outside of the span of the previous vectors, the vector \(T w\) is also outside of the span. 

Therefore, we get a set of linearly independent nonzero vectors 
\[w_1, Tw_1, w_2, Tw_2, ..., w_n, Tw_n\]
until \(\operatorname{span} \{w_1, Tw_1, w_2, Tw_2, ..., w_n, Tw_n\} = W\). Since \(W\) is finite-dimensional, the process terminates. Therefore \(W\) has even dimension. 
\end{proof}
\begin{remark}
Suppose \(T: V \to V\) has no eigenvalue, for \(V\) a finite-dimensional vector space over \(\mathbb{R}\). Suppose \(b, c \in \mathbb{R}\), \(b^2 < 4c\), and for some integer \(n\), we have \(v \notin \ker [(T^2 + bT + cI)^n]\) while \(v \in \ker [(T^2 + bT + cI)^{n+1}]\). 

The question to ponder is: \textcolor{blue}{Is there a possibility that 
\[T^m v, T^{m-1} v, ..., T v, v\]
are linearly dependent for some smallest \(m\), and \(m \leq 2n\)?}

Suppose there is such an \(m\), then we have 
\[p_m (T) v = 0,\]
where \(p_m (T)\) is some degree \(m\) polynomial. 

Suppose \(m\) is odd, then when we factor \(p_m (T)\) in \(\mathbb{R}\), it would factor into odd numbers of \((T - \mu_i I)\)s. However, this would mean each \(\mu_i\) is an eigenvalue, and we get a contradiction. Therefore, the polynomial \(p_m (T)\) should factor into zero \(T - \mu_i I\)s, which means \(m\) has to be an even integer. 

Since \(v \in \ker [(T^2 + bT + cI)^{n+1}]\), \((T^2 + bT + cI)^{n+1} v = 0\). Let \(p_N (T) = (T^2 + bT + cI)^{n+1}\), then there exists polynomials \(q(T)\) and \(r(T)\), such that 
\[p_N (T) = q(T) p_m (T) + r(T),\]
where \(\deg r < \deg p_m = m\). However, this implies 
\[0 = p_N (T) v = q(T) p_m (T) v + r(T) v,\]
which means \(r(T) v = 0\), and \(m\) is no longer the smallest degree of the polynomial to annihilate \(v\). We get a contradiction. 

Therefore, \(2n + 2\) is the smallest degree of the polynomial that annihilates \(v\). 
\end{remark}
\begin{remark}
Suppose \(T: V \to V\) has no eigenvalue, for \(V\) a finite-dimensional vector space over \(\mathbb{R}\). Suppose \(a, b, c, d \in \mathbb{R}\) such that \(a^2 < 4b\) and \(c^2 < 4d\), where \((a, b) \ne (c, d)\). \textcolor{blue}{The question to ponder is: For integer(s) \(m\) and \(n\), where does
\[\ker (T^2 + aT + bI)^m \subseteq V\]
and 
\[\ker (T^2 + cT + dI)^n \subseteq V\]
intersect?}

Suppose there is a nonzero \(v \in V\) such that 
\[v \in \ker (T^2 + aT + bI)^m \bigcap \ker (T^2 + cT + dI)^n.\]
By our above analysis, there exists minimum integers \(x\) and \(y\), such that 
\[v \in \ker (T^2 + aT + bI)^x,\]
\[v \notin \ker (T^2 + aT + bI)^{x-1},\]
\[v \in \ker (T^2 + cT + dI)^y,\]
and 
\[v \notin \ker (T^2 + cT + dI)^{y-1}.\]
Also by our above analysis, we know that 
\[v \in \ker (T^2 + aT + bI)^x\]
implies \(2x\) is the smallest degree of the polynomial that annihilates \(v\), and 
\[v \in \ker (T^2 + cT + dI)^y\]
implies \(2y\) is the smallest degree of the polynomial that annihilates \(v\). Therefore, we have \(x = y\). 

Since the polynomials 
\[(T^2 + aT + bI)^x\]
and 
\[(T^2 + cT + dI)^y = (T^2 + cT + dI)^x\]
are both monic, we subtract the two polynomials and get 
\[p_{2x-1} (T) v = 0\]
where \(p_{2x-1} (T)\) is a polynomial of degree at most \(2x - 1\). 

We already know that any polynomial of degree less than or equal to \(2x - 2\) cannot annihilate \(v\), so \(p_{2x-1} (T)\) has degree \(2x-1\). However, now \(p_{2x-1} (T)\) has an odd degree, and it would factor out odd numbers of eigenvalues, contradicting our assumption that \(T\) has no eigenvalues. 

We hence reach the conclusion that 
\[\ker (T^2 + aT + bI)^m \bigcap \ker (T^2 + cT + dI)^n = \{0\}.\]
\end{remark}
\begin{remark}
Suppose \(T: V \to V\) has no eigenvalue, for \(V\) a finite-dimensional vector space over \(\mathbb{R}\). Suppose \(a, b \in \mathbb{R}\), and \(a^2 < 4b\). 

We already know that \(\ker (T^2 + aT + bI)\) has even dimension. The question to ponder is: What about the dimension of \(\ker (T^2 + aT + bI)^n \subseteq V\), for some general integer \(n\)? 

First of all, we know that 
\[\ker (T^2 + aT + bI) \subseteq \ker (T^2 + aT + bI)^2 \subseteq ... \subseteq \ker (T^2 + aT + bI)^n.\]
Suppose \(\mathcal{B}_1\) is a basis for \(\ker (T^2 + aT + bI)\). By our previous theorem, this basis has even number of elements. 

Now we try to extend \(\mathcal{B}_1\) into \(\mathcal{B}_2\), such that \(\mathcal{B}_2\) is a basis for \(\ker (T^2 + aT + bI)^2\). The process is as follows: We first pick a \(v \notin \ker (T^2 + aT + bI)\) while \(v \in \ker (T^2 + aT + bI)^2\). 

By our previous analysis, we know that \(4\) is the smallest degree of the polynomial that annihilates \(v\), which means \(v, Tv, T^2 v, T^3 v\) are linearly independent. 

We first claim that \(Tv, T^2 v, T^3 v \notin \ker (T^2 + aT + bI)\). This is easy to prove, because for \(Tv \in \ker (T^2 + aT + bI)\) we would get a degree \(3\) polynomial that annihilates \(v\), and for \(T^2 v\) and \(T^3 v\) we would get zero as an eigenvalue for \(T\). 

So we know that if \(v\) is picked, then \(Tv, T^2 v, T^3 v\) would also be picked to extend \(\mathcal{B}_1\) into \(\mathcal{B}_2\). Now suppose we have to pick \(w \in V\) such that 
\[w \notin \ker (T^2 + aT + bI),\]
\[w \in \ker (T^2 + aT + bI)^2,\]
and 
\[w \notin \operatorname{span} \{v, Tv, T^2 v, T^3 v\}.\]
Clearly \(Tw, T^2 w, T^3 w \in \ker (T^2 + aT + b I)^2\) and \(Tw, T^2 w, T^3 w \notin \ker (T^2 + aT + b I)\). We want to show that \(Tw, T^2 w, T^3 w \notin \operatorname{span} \{v, Tv, T^2 v, T^3 v\}\). But this is also evident: 
\[w \notin \operatorname{span} \{v, Tv, T^2 v, T^3 v\} \Longleftrightarrow\]
\[w \text{ is not linear combination of } \{v, Tv, T^2 v, T^3 v\} \Longleftrightarrow\]
\[Tw \text{ is not linear combination of } \{Tv, T^2 v, T^3 v, T^4 v\} = \{v, Tv, T^2 v, T^3 v\},\]
and the rest follow in a similar fashion. For the following vectors we picked in \(\ker (T^2 + aT + bI)^2\), the linear independence also follows similarly. 

By mathematical induction, suppose for some integer \(m < n\), we have \(\mathcal{B}_m\) and we try to extend it into \(\mathcal{B}_{m+1}\). Therefore by re-labeling, we are picking vectors \(v\) in 
\[\ker (T^2 + aT + b I)^{m+1} - \ker (T^2 + aT + b I)^m.\]
Then 
\[T^{2m-1} v, T^{2m} v, ..., Tv \notin \ker (T^2 + aT + b I)^m\]
because otherwise we would also get \(0\) to be an eigenvalue. And in a similar approach as above, we can show that when we pick a new vector \(v_k\) in 
\[\ker (T^2 + aT + b I)^{m+1} - \ker (T^2 + aT + b I)^m,\]
we have
\[T^{2m-1} v_k, T^{2m} v_k, ..., Tv_k \notin \operatorname{span} \{v_1, Tv_1, ..., T^{2m-1} v_1, ..., v_{k-1}, ..., T^{2m-1} v_{k-1}\}.\]

\textcolor{blue}{Hence the dimension of \(\ker (T^2 + aT + bI)^n\) is also even for general integer \(n\).}
\end{remark}
\begin{theorem}
Every operator on an odd-dimensional vector space has an eigenvalue. 
\end{theorem}
\begin{proof}
Suppose \(V\) is an odd-dimensional vector space over \(\mathbb{R}\), and assume that it has no eigenvalue. Let \(\dim V = n\). 

Let 
\[\{b_1, b_2, ..., b_n\}\]
be a basis for \(V\). Therefore each vector in the basis has a monic polynomial on \(T\) of the smallest degree such that it annihilates the vector. We denote 
\[p_i (T) = T^{d_i} + a_{i, d_i - 1} T^{d_i - 1} + ... + a_{i, 1} T + a_{i, 0} I\]
such that 
\[p_i (T) b_i = 0\]
for each \(i = 1, 2, ..., n\). 

We try to factorize each \(p_i\). Suppose \(p_i\) factorizes into 
\[p_i (T) = (T - \lambda_{i, 1} I) ... (T - \lambda_{i, x_i} I) (T^2 + \alpha_{i, 1} T + \beta_{i, 1} I) ... (T^2 + \alpha_{i, y_i} T + \beta_{i, y_i} I)\]
for some \(x_i, y_i\) on \(i\) for each \(i = 1, 2, ..., n\), where every coefficient is in \(\mathbb{R}\) as we have defined. 

However, since \(T\) has no eigenvalues, and if those \((T - \lambda I)\) terms exists the \(\lambda\)s are eigenvalues, we reach the conclusion that the \((T - \lambda I)\) terms do not exist. 

Now let \(p(T)\) be the polynomial which is of the smallest degree that is the polynomial multiple of every \(p_i (T)\) for all \(i = 1, 2, ..., n\). Then after re-labeling the coefficients, we have
\[p(T) = (T^2 + \alpha_1 T + \beta_1 I)^{k_1} (T^2 + \alpha_2 T + \beta_2 I)^{k_2} ... (T^2 + \alpha_m T + \beta_m I)^{k_m}\]
for some integer \(m\), and the \((\alpha_i, \beta_i)\) pairs are all distinct. Since \(p(T)\) annihilates every vector of a basis for \(V\), it annihilates the entire V. Therefore \(V = \ker p(T)\). 

By our above discussions, we know that 
\[V = \ker (T^2 + \alpha_1 T + \beta_1 I)^{k_1} \oplus \cdots \oplus (T^2 + \alpha_m T + \beta_m I)^{k_m}.\]
Since the dimension of each 
\[\ker (T^2 + \alpha_i T + \beta_i I)^{k_i}\]
is even, the dimension of \(V\) is also even. Since \(T\) has no eigenvalue implies that \(V\) has even dimensions, we reach the conclusion that if \(V\) has odd dimension, \(T\) has an eigenvalue. 

\textcolor{red}{The proof from the book:}

Suppose \( \mathbb{F} = \mathbb{R} \) and \( V \) is finite-dimensional. Let \( n = \dim V \), and suppose \( n \) is an odd number. Let \( T \in \mathcal{L}(V) \). We will use induction on \( n \) in steps of size two to show that \( T \) has an eigenvalue. To get started, note that the desired result holds if \( \dim V = 1 \) because then every nonzero vector in \( V \) is an eigenvector of \( T \).

Now suppose that \( n \geq 3 \) and the desired result holds for all operators on all odd-dimensional vector spaces of dimension less than \( n \). Let \( p \) denote the minimal polynomial of \( T \). If \( p \) is a polynomial multiple of \( x - \lambda \) for some \( \lambda \in \mathbb{R} \), then \( \lambda \) is an eigenvalue of \( T \) and we are done. Thus we can assume that there exist \( b, c \in \mathbb{R} \) such that \( b^2 < 4c \) and \( p \) is a polynomial multiple of \( x^2 + bx + c \).

There exists a monic polynomial \( q \in \mathcal{P}(\mathbb{R}) \) such that \( p(x) = q(x)(x^2 + bx + c) \) for all \( x \in \mathbb{R} \). Now
\[
0 = p(T) = \left(q(T)\right)(T^2 + bT + cI),
\]
which means that \( q(T) \) equals \( 0 \) on \( \text{range}(T^2 + bT + cI) \). Because \( \deg q < \deg p \) and \( p \) is the minimal polynomial of \( T \), this implies that
\[
\text{range}(T^2 + bT + cI) \ne V.
\]

The fundamental theorem of linear maps tells us that
\[
\dim V = \dim \text{null}(T^2 + bT + cI) + \dim \text{range}(T^2 + bT + cI).
\]
Because \( \dim V \) is odd (by hypothesis) and \( \dim \text{null}(T^2 + bT + cI) \) is even (by the equation above), this shows that \( \dim \text{range}(T^2 + bT + cI) \) is odd.

Hence \( \text{range}(T^2 + bT + cI) \) is a subspace of \( V \) that is invariant under \( T \), and that has odd dimension less than \( \dim V \). By induction hypothesis, \( T \) restricted to \( \text{range}(T^2 + bT + cI) \) has now become \(V\) by re-labeling, and we reduce its dimension by \(2\) until we get dimension one. Therefore,  \( T \) has an eigenvalue.
\end{proof}
\section{More on eigenvalues and the minimal polynomial in \(\mathbb{R}\)}
Suppose \(V\) is a vector space over \(\mathbb{R}\), and \(T: V \to V\). Suppose the minimal polynomial is 
\[p(T) = (T - \lambda_1 I)^{k_1} ... (T - \lambda_n I)^{k_n} (T^2 + a_1 T + b_1 I)^{l_1} ... (T^2 + a_m T + b_m I)^{l_m}.\]
Note that, if the degree 2 polynomials are left un-factorized, that means \(a_j^2 < 4 b_j\) for each \(j\). 

Similar to the case in \(\mathbb{C}\), we want to prove the following results
\begin{enumerate}
    \item If \(v \in \ker (T - \lambda_i I)^x\) and \(v \notin \ker (T - \lambda_i I)^{x-1}\) for some integer \(x\) and some \(i\), then
    \[\{v, Tv, ..., T^x v\}\]
    are linearly dependent, while 
    \[\{v, Tv, ..., T^{x-1}v\}\]
    are linearly independent. 

    \textcolor{blue}{This has been proved for the \(\mathbb{C}\) case, and the proof for \(\mathbb{R}\) is basically the same, except that we may assume to factorize smallest annihilating polynomials of a vector into degree 2 polynomials with no zero and same as above, conclude that the linear combination of vectors of one subspace actually resulted in a vector in another subspace which intersects only at zero, which is impossible. Omitted. }
    \item If \(v \in \ker (T^2 + a_j T + b_j I)^{x}\) and \(v \notin \ker (T^2 + a_j T + b_j I)^{x-1}\) for some integer \(x\) and some \(j\), then 
    \[\{v, Tv, ..., T^{2x}v\}\]
    are linearly dependent, while
    \[\{v, Tv, ..., T^{2x-1}v\}\]
    are linearly independent. 

    \textcolor{blue}{This has been proved in a previous section. Omitted.}
    \item Denote 
    \[N_i = \ker (T - \lambda_i I)^{k_i}\]
    for each \(i\) and 
    \[M_j = \ker (T^2 + a_j T + b_j I)^{l_j}\]
    for each \(j\), then 
    \[M_x \bigcap M_y = \{0\} \text{ for } x, y = 1, ..., n \text{ and } x \ne y;\]
    \begin{proof}
    By relabeling, suppose there exists some nonzero \(v \in \ker (T - \lambda I)^{n_\lambda} \bigcap \ker (T - \mu I)^{n_\mu}\), then there exist smallest integers \(x \leq n_\lambda\) and \(y \leq n_\mu\) such that 
    \[v \in \ker (T - \lambda I)^x,\]
    \[v \notin \ker (T - \lambda I)^{x-1},\]
    \[v \in \ker (T - \mu I)^y,\]
    and 
    \[v \notin \ker (T - \mu I)^{y-1}.\]
    Therefore from previous discussions, we know that \(x\) is the smallest integer for 
    \[v, Tv, ..., T^x v\]
    to be linearly dependent, and so is \(y\), which implies \(x = y\). However, the annihilating polynomials 
    \[p_x (T) = (T - \lambda I)^x\]
    and 
    \[p_y (T) = (T - \mu I)^y\]
    are of the same degree and both monic, which means \(p_x (T) - p_y (T)\) can also annihilate \(v\), but it is a nonzero polynomial of a smaller degree. Therefore we reach a contradiction. 
    \end{proof}
    \[M_x \bigcap N_y = \{0\} \text{ for } x = 1, ..., n; y = 1, ..., m;\]
    \begin{proof}
    By re-labeling again, there exist smallest integers \(x\) and \(y\) such that there exists some nonzero \(v \in \ker (T - \lambda I)^x \bigcap \ker (T^2 + a T + b I)^y\). Therefore \(x = 2y\), and \(p(T) = (T - \lambda I)^x - (T^2 + aT + b I)^y\) is also an annihilating polynomial of \(v\) with a smaller degree, therefore we reach a contradiction. 
    \end{proof}
    \[N_x \bigcap N_y = \{0\}\text{ for }x, y = 1, ..., m \text{ and } x \ne y.\]
    \begin{proof}
    By re-labeling again, there exists smallest integers \(x, y\), such that there exists some nonzero \(v \in \ker (T^2 + a T + b I)^x \bigcap \ker (T^2 + c T + d I)^y\). Therefore \(x = y\) and \(p(T) = (T^2 + a T + b I)^x - (T^2 + c T + d I)^y\) is also an annihilating polynomial of \(v\) in a smaller degree, therefore we reach an contradiction. 
    \end{proof}
    \item \[V = \ker (T - \lambda_1)^{k_1} \oplus \ker (T - \lambda_2)^{k_2} \oplus ... \oplus \ker (T - \lambda_n)^{k_n}\]
    \[\oplus \ker (T^2 + a_1 T + b_1 I)^{l_1} \oplus \ker (T^2 + a_2 T + b_2 I)^{l_2} \oplus ... \oplus \ker (T^2 + a_m T + b_m I)^{l_m}.\]
    \begin{proof}
    We can clearly see that \[\ker (T - \lambda_1)^{k_1} \oplus \ker (T - \lambda_2)^{k_2} \oplus ... \oplus \ker (T - \lambda_n)^{k_n} \oplus\]
    \[\ker (T^2 + a_1 T + b_1 I)^{l_1} \oplus \ker (T^2 + a_2 T + b_2 I)^{l_2} \oplus ... \oplus \ker (T^2 + a_m T + b_m I)^{l_m} \subseteq V,\]
    and the minimal polynomial annihilates 
    \[\ker (T - \lambda_1)^{k_1} \oplus \ker (T - \lambda_2)^{k_2} \oplus ... \oplus \ker (T - \lambda_n)^{k_n} \oplus\]
    \[\ker (T^2 + a_1 T + b_1 I)^{l_1} \oplus \ker (T^2 + a_2 T + b_2 I)^{l_2} \oplus ... \oplus \ker (T^2 + a_m T + b_m I)^{l_m}.\]
    Suppose there is a \(v\) in
    \[V - \ker (T - \lambda_1)^{k_1} \oplus ... \oplus \ker (T - \lambda_n)^{k_n} \oplus \ker (T^2 + a_1 T + b_1 I)^{l_1} \oplus ... \oplus \ker (T^2 + a_m T + b_m I)^{l_m}.\]
    Since \(v\) is also annihilated by the minimal polynomial, there exists integers \(0 \leq e_i \leq k_i\) and \(0 \leq f_j \leq l_j\), such that the polynomial 
    \[(T - \lambda_1 I)^{e_1}...(T - \lambda_n I)^{e_n} (T^2 + a_1 T + b_1 I)^{f_1} ... (T^2 + a_m T + b_m I)^{f_m} v\]
    is the smallest polynomial factor that can eliminate \(v\). 
    
    If \(T\) has a zero eigenvalue \(\lambda_i = 0\), we can conclude that 
    \[(T - \lambda_1 I)^{e_1} ...(T - \lambda_{i-1})^{e_{i-1}}(T - \lambda_{i+1})^{e_{i+1}}\]
    \[...(T - \lambda_n I)^{e_n} (T^2 + a_1 T + b_1 I)^{f_1} ... (T^2 + a_m T + b_m I)^{f_m} v\]
    is in \(\ker T\). However, the term 
    \[(T - \lambda_1 I)^{e_1} ...(T - \lambda_{i-1})^{e_{i-1}}(T - \lambda_{i+1})^{e_{i+1}}\]
    \[...(T - \lambda_n I)^{e_n} (T^2 + a_1 T + b_1 I)^{f_1} ... (T^2 + a_m T + b_m I)^{f_m} v\]
    is a linear combination containing \(v\) with a nonzero coefficient, which is not in \(\ker T\). This means the term contains a linear combination that can eliminate \(v\), which means there is a polynomial of \(T\) in smaller degree than 
    \[e_1 + ... +e_{i-1}+e_{i+1}+ ... + e_n + f_1 + ... + f_m\]
    such that it annihilates \(v\). Therefore we get a contradiction. 

    If \(T\) does not have a zero eigenvalue, then any \(\lambda_i\) can do the job. Proof omitted.  
    \end{proof}
\end{enumerate}
\section{Upper-triangular matrices}
\begin{definition}[matrix of an operator, \(\mathcal{M}(T)\)]
Suppose \( T \in \mathcal{L}(V) \). The \textit{matrix of} \( T \) with respect to a basis \( v_1, \ldots, v_n \) of \( V \) is the \( n \)-by-\( n \) matrix
\[
\mathcal{M}(T) = 
\begin{pmatrix}
A_{1,1} & \cdots & A_{1,n} \\
\vdots & \ddots & \vdots \\
A_{n,1} & \cdots & A_{n,n}
\end{pmatrix}
\]
whose entries \( A_{j,k} \) are defined by
\[
Tv_k = A_{1,k}v_1 + \cdots + A_{n,k}v_n.
\]
The notation \( \mathcal{M}(T, (v_1, \ldots, v_n)) \) is used if the basis is not clear from the context.
\end{definition}
\begin{remark}
Recall when we talk about change of basis, we reached the conclusion that for matrix \(A\) representing a linear transformation \(T\) written in some basis \(\mathcal{B}\), the \(i\)-th column vector of \(A\) is \([Tv_i]_\mathcal{B}\). Hence, we have the relation
\[T v_i = A_{1, i} v_1 + A_{2, i} v_2 + ... + A_{n, i} v_n.\]
Therefore the above definition agrees with our previous findings.
\end{remark}
\begin{remark}
Suppose we have \(n^2\) coefficients 
\[\{B_{i, j}\}_{i = 1, 2, ..., n}^{j = 1, 2, ..., n}\]
satisfying the relation
\[T v_i = B_{1, i} v_1 + B_{2, i} v_2 + ... + B_{n, i} v_n\]
for all \(i = 1, 2, ..., n\), then the vector \(T v_i\) written in basis 
\[\mathcal{B} = \{v_1, ..., v_n\}\]
is
\[[B_{1, i} \quad B_{2, i} \quad ... \quad B_{n,i}]^T,\]
which means \(B_{i, j}\) are entries of the matrix of \(T\) with respect to the basis \(\mathcal{B}\). 
\end{remark}
A central goal of linear algebra is to show that given an operator \( T \) on a finite-dimensional vector space \( V \), there exists a basis of \( V \) with respect to which \( T \) has a reasonably simple matrix. To make this vague formulation a bit more precise, we might try to choose a basis of \( V \) such that \( \mathcal{M}(T) \) has many 0’s. 
\begin{theorem}
If \( V \) is a finite-dimensional complex vector space, then we can find a basis of \( V \) with respect to which the matrix of \( T \) has 0’s everywhere in the first column, except possibly the first entry. In other words, there is a basis of \( V \) with respect to which the matrix of \( T \) looks like
\[
\begin{pmatrix}
\lambda & \quad & \quad & \quad \\
0 & \\
\vdots &  \quad * & \quad \\
0 & \quad & \quad 
\end{pmatrix};
\]
here \( * \) denotes the entries in all columns other than the first column.
\end{theorem}
\begin{proof}
Since \(V\) is a finite-dimensional vector space over complex scalars, there exists an eigenvalue \(\lambda \in \mathbb{C}\) for \(T\). Therefore, we can find a nonzero vector \(v\) as the corresponding eigenvector, and let \(v_1 = v\) be the first element in the basis. Now by our previously defined relation, we have 
\[Tv_1 = A_{1, 1} v_1 + A_{1, 2} v_2 + ... + A_{1, n} v_n = \lambda v_1,\]
then we get \(A_{1, 1} = \lambda\) and all other \(A_{1, i}\)'s are zeros. 
\end{proof}
\begin{definition}[diagonal of a matrix]
The \emph{diagonal} of a square matrix consists of the entries on the line from the upper left corner to the bottom right corner.
\end{definition}
\begin{example}
For example, the diagonal of the matrix
\[
\mathcal{M}(T) = 
\begin{pmatrix}
\textcolor{red}{2} & 1 & 0 \\
0 & \textcolor{red}{5} & 3 \\
0 & 0 & \textcolor{red}{8}
\end{pmatrix}
\]
\end{example}
\begin{definition}[upper-triangular matrix]
A square matrix is called upper-triangular if all entries below the diagonal are \(0\). We typically represent an upper-triangular matrix in the form \[
\begin{pmatrix}
\lambda_1 & * \\
0 & \ddots & \\
& & \lambda_n
\end{pmatrix}.
\]
\end{definition}
\begin{theorem}[conditions for upper-triangular matrix]
Suppose \( T \in \mathcal{L}(V) \) and \( v_1, \ldots, v_n \) is a basis of \( V \). Then the following are equivalent.
\begin{itemize}
  \item[(a)] The matrix of \( T \) with respect to \( v_1, \ldots, v_n \) is upper triangular.
  \item[(b)] \( \mathrm{span}(v_1, \ldots, v_k) \) is invariant under \( T \) for each \( k = 1, \ldots, n \).
  \item[(c)] \( T v_k \in \mathrm{span}(v_1, \ldots, v_k) \) for each \( k = 1, \ldots, n \).
\end{itemize}
\end{theorem}
\begin{proof}
Suppose \(\operatorname{span} \{v_1, v_2, ..., v_k\}\) is invariant under \(T\) for all \(k = 1, 2, ..., n\). Then \(T v_k \in \operatorname{span} \{v_1, v_2, ..., v_k\}\). 

Suppose \(T v_k \in \operatorname{span} \{v_1, v_2, ..., v_k\}\) for all \(k = 1, 2, ..., n\). Pick any \(v \in \operatorname{span} \{v_1, v_2, ..., v_k\}\), which can be written as \(v = x_1 v_1 + x_2 v_2 + ... + x_k v_k\), then 
\[T v = x_1 T v_1 + x_2 T v_2 + ... + x_k T v_k \in \operatorname{span} \{v_1, v_2, ..., v_k\},\]
which means \(\operatorname{span} \{v_1, v_2, ..., v_k\}\) is invariant under \(T\) for each \(k = 1, 2, ..., n\). Now we have \((b) \Longleftrightarrow (c)\). 

Suppose the matrix of \(T\) with respect to \(v_1, ..., v_n\), denoted \(A\), is upper-triangular. Then we have \(A_{i, j} = 0\) for \(i > j\), and therefore by definition of the entries of \(A\), we have 
\[T v_1 = A_{1, 1} v_1 + A_{1, 2} v_2 + ... + A_{1, n} v_n = A_{1, 1} v_1;\]
\[T v_2 = A_{1, 2} v_1 + A_{2, 2} v_2 + ... + A_{n, 2} v_n = A_{1, 2} v_1 + A_{2, 2} v_2;\]
\[T v_3 = A_{1, 3} v_1 + A_{2, 3} v_2 + ... + A_{n, 3} v_n = A_{1, 3} v_1 + A_{2, 3} v_2 + A_{3, 3} v_3;\]
\[\vdots\]
\[T v_{n-1} = A_{1, n-1} v_1 + ... + A_{n, n-1} v_n = A_{1, n-1} v_1 + A_{2, n-1} v_2 + ... + A_{n-1, n-1} v_{n-1};\]
\[T v_n = A_{1, n} v_1 + A_{2, n} v_2 + ... + A_{n, n} v_n.\]
Clearly this implies \(T v_k \in \operatorname{span} \{v_1, v_2, ..., v_k\}\) for all \(k = 1, 2, ..., n\).

Suppose \(T v_k \in \operatorname{span} \{v_1, v_2, ..., v_k\}\) for all \(k = 1, 2, ..., n\). Then we have 
\[T v_1 = C_{1, 1} v_1;\]
\[T v_2 = C_{1, 2} v_1 + C_{2, 2} v_2;\]
\[T v_3 = C_{1, 3} v_1 + C_{2, 3} v_2 + C_{3, 3} v_3;\]
\[\vdots\]
\[T v_{n-1} = C_{1, n-1} v_1 + C_{2, n-1} v_2 + ... + C_{n-1, n-1} v_{n-1};\]
\[T v_n = C_{1, n} v_1 + C_{2, n} v_2 + ... + C_{n, n} v_n\]
for some constants \(C_{i, j}\). 

\textcolor{red}{We write those \(n\) equations about vectors into column vector representations with respect to the basis \(\mathcal{B}\)}, then we solved entries of \(A\). In other words, when we write those equations about vectors into column vector representations, we get
\[[Tv_1]_{\mathcal{B}}
\begin{bmatrix}
C_{1, 1} \\
0 \\
\vdots \\
0
\end{bmatrix};
\]
\[[Tv_2]_{\mathcal{B}}
\begin{bmatrix}
C_{1, 2} \\
C_{2, 2} \\
0 \\
\vdots \\
0
\end{bmatrix};
\]
\[\vdots\]
\[[Tv_k]_{\mathcal{B}}
\begin{bmatrix}
C_{1, k} \\
C_{2, k} \\
C_{3, k} \\
\vdots \\
C_{k-1, k} \\
C_{k, k} \\
0 \\
\vdots \\
0
\end{bmatrix};
\]
\[\vdots\]
\[[Tv_n]_{\mathcal{B}}
\begin{bmatrix}
C_{1, n} \\
C_{2, n} \\
\vdots \\
C_{n, n}
\end{bmatrix};
\]
Hence we get \((a) \Longleftrightarrow (b) \Longleftrightarrow (c)\). 
\end{proof}
\begin{theorem}
Suppose \( T \in \mathcal{L}(V) \) and \( V \) has a basis with respect to which \( T \) has an upper-triangular matrix with diagonal entries \( \lambda_1, \ldots, \lambda_n \). Then
\[
(T - \lambda_1 I) \cdots (T - \lambda_n I) = 0.
\]
\end{theorem}
\begin{proof}
Denote the basis for \(V\) as \(\mathcal{B} = \{v_1, ..., v_n\}\). One easy proof is to write \(T - \lambda_i\) into matrices, and we can see that for any column vector \(x = [x_1 \quad x_2 \quad ... \quad x_n]^T\), 
\[[T-\lambda_n]_{\mathcal{B}} \text{ is a matrix with the bottom row zero,}\]
which means 
\[[T-\lambda_n]_{\mathcal{B}}x \text{ is a column vector with the bottom entry zero.}\]
Denote that vector as \(x_n\), then since \([T-\lambda_{n-1}]_{\mathcal{B}}\) is a matrix with the \((n-1, n-1)\)-th entry zero and all \((n-1, i)\)-th entries zero for \(i < n\), 
\[[T-\lambda_{n-1}]_{\mathcal{B}}x_n\]
is a column vector with the bottom two entries zeros. Therefore by mathematical induction, 
\[[T-\lambda_1]_{\mathcal{B}} [T-\lambda_2]_{\mathcal{B}} ... [T-\lambda_{n-1}]_{\mathcal{B}}[T-\lambda_n]_{\mathcal{B}}\]
acts on every vector will result in a zero column vector. Therefore we get
\[
(T - \lambda_1 I) \cdots (T - \lambda_n I) = 0.
\]
\textcolor{red}{Another proof:}

Denote the basis for \(V\) as \(\mathcal{B} = \{v_1, ..., v_n\}\). Denote \(A = [T]_{\mathcal{B}}\). Then by definition of the entries of \(A\), we have 
\[T v_i = A_{1, i} v_1 + A_{2, i} v_2 + ... + A_{n, i} v_n \text{ for all }i = 1, 2, ..., n,\]
which implies 
\[T v_i = A_{1, i} v_1 + A_{2, i} v_2 + ... + \lambda_i v_i\]
and
\[(T - \lambda_i I)v_i = A_{1, i} v_1 + A_{2, i} v_2 + ... + A_{i-1, i}v_{i -1}\]
for all \(i = 1, 2, ..., n\). Therefore we have
\[(T - \lambda_i I)v_i \in \operatorname{span}\{v_1, ..., v_{i -1}\}\]
for all \(i = 1, 2, ..., n\). 

Then for any \(v \in V\) denoted as 
\[v = x_1 v_1 + x_2 v_2 + ... + x_n v_n,\]
so we have \(T v_1 = \lambda_1 v_1\), and therefore for any \(k = 1, 2, ..., n\), we have
\begin{align*}
&(T - \lambda_k I) v_k = A_{1, k} v_1 + A_{2, k} v_2 + ... + A_{k-1, k} v_{k-1} \in \operatorname{span} \{v_1, v_2, ..., v_{k-1}\}; \\
&(T - \lambda_{k-1} I)(T - \lambda_k) v_k \in \operatorname{span} \{v_1, v_2, ..., v_{k-2}\}; \\
&(T - \lambda_{k-2})(T - \lambda_{k-1} I)(T - \lambda_k) v_k \in \operatorname{span} \{v_1, v_2, ..., v_{k-3}\}; \\
& \vdots \\
&(T - \lambda_2 I) \cdots (T - \lambda_{k-1} I)(T - \lambda_k) v_k \in \operatorname{span} \{v_1\}; \\
&(T - \lambda_1 I)(T - \lambda_2 I) \cdots (T - \lambda_{k-1} I)(T - \lambda_k) v_k \in \operatorname{span} \{0\};
\end{align*}
Therefore, by shrinking the span one by one, we get zero at the end. Since the polynomial eliminates every vector of a basis, it eliminates the entire space. 
\end{proof}
\begin{theorem}
Suppose $T \in \mathcal{L}(V)$ has an upper-triangular matrix with respect to some basis of $V$. Then the eigenvalues of $T$ are precisely the entries on the diagonal of that upper-triangular matrix.
\end{theorem}
\begin{proof}
Denote the diagonals as \(\lambda_1, \lambda_2, ..., \lambda_n\). 

Before proving this theorem, let us recall that since 
\[
(T - \lambda_1 I) \cdots (T - \lambda_n I) = 0,
\]
\textcolor{ForestGreen}{this polynomial of \(T\) is a polynomial multiple of the minimal polynomial}. Therefore, \textcolor{ForestGreen}{all the eigenvalues are included in \(\lambda_1, \lambda_2, ..., \lambda_n\)}. So to prove this theorem, \textcolor{ForestGreen}{we only need to show that every \(\lambda_i\) is an eigenvalue}. 

Recall that, we have \(n\) equations
\begin{align*}
T v_1 &= \lambda_1 v_1 \\
T v_2 &= A_{1, 2} v_1 + \lambda_2 v_2 \\
T v_3 &= A_{1, 3} v_1 + A_{2, 3} v_2 + \lambda_3 v_3 \\
& \vdots \\
T v_k &= A_{1, k} v_1 + ... + A_{k-1, k} v_{k-1} + \lambda_k v_k \\
& \vdots \\
T v_n &= A_{1, n} v_1 + ... + A_{n-1, n} v_{n-1} + \lambda_n v_n
\end{align*}
and therefore
\begin{align*}
(T - \lambda_1 I) v_1 &= 0 \\
(T - \lambda_2 I) v_2  &= A_{1, 2} v_1  \\
(T - \lambda_3 I) v_3 &= A_{1, 3} v_1 + A_{2, 3} v_2 \\
& \vdots \\
(T - \lambda_k I) v_k &= A_{1, k} v_1 + ... + A_{k-1, k} v_{k-1} \\
& \vdots \\
(T - \lambda_n I) v_n &= A_{1, n} v_1 + ... + A_{n-1, n} v_{n-1}
\end{align*}
which means 
\[(T - \lambda_k I) \operatorname{span}\{v_1, ..., v_k\} \subseteq \operatorname{span} \{v_1, ..., v_{k-1}\}.\]
Note that the map
\[(T - \lambda_k I): \operatorname{span}\{v_1, ..., v_k\} \to \operatorname{span} \{v_1, ..., v_{k-1}\}\]
may not be full rank, but nevertheless, the map 
\[(T - \lambda_k I)\]
on the subspace 
\[\operatorname{span}\{v_1, ..., v_k\} \subset V\]
has a nontrivial kernel. Therefore, there exists nonzero \(u \in \operatorname{span}\{v_1, ..., v_k\} \subset V\), such that \((T - \lambda_k I) u = 0\), which means \(\lambda_k\) is an eigenvalue for \(T\). 
\end{proof}
\begin{theorem}
Suppose \( V \) is finite-dimensional and \( T \in \mathcal{L}(V) \). Then \( T \) has an upper-triangular matrix with respect to some basis of \( V \) if and only if the minimal polynomial of \( T \) equals \( (z - \lambda_1) \cdots (z - \lambda_m) \) for some \( \lambda_1, \ldots, \lambda_m \in \mathbb{F} \). \textcolor{red}{Note that, the integer \(m\) means the total number of factors, including repetitions.}
\end{theorem}
\begin{proof}
Suppose \(T\) has an upper-triangular matrix representation with respect to some basis of \(V\), then let \(\lambda_1, ..., \lambda_n\) be its diagonals, then by a previous theorem, the polynomial 
\[(T - \lambda_1 I)...(T - \lambda_n I) = 0,\]
which means it is a polynomial multiple of the minimal polynomial. Then by re-labeling the \(\lambda\)'s, we have the minimal polynomial equals 
\[(z - \lambda_1) \cdots (z - \lambda_m)\]
for some \( \lambda_1, \ldots, \lambda_m \in \mathbb{F} \).

For the reverse direction, we prove by induction. 

We already know that, for \(m = 1\), the result is true (omitted). 

Now suppose \( m > 1 \) and the desired result holds for all smaller positive integers. Let
\[
U = \operatorname{range}(T - \lambda_m I).
\]
Then \( U \) is invariant under \( T \). Thus \( T|_U \) is an operator on \( U \).

If \( u \in U \), then \( u = (T - \lambda_m I)v \) for some \( v \in V \) and
\[
(T - \lambda_1 I) \cdots (T - \lambda_{m-1} I)u = (T - \lambda_1 I) \cdots (T - \lambda_{m-1} I)(T - \lambda_m I)v = 0.
\]
Hence \( (z - \lambda_1) \cdots (z - \lambda_{m-1}) \) is a polynomial multiple of the minimal polynomial of \( T|_U \). Thus the minimal polynomial of \( T|_U \) is the product of at most \( m - 1 \) terms of the form \( z - \lambda_k \).

By our induction hypothesis, there is a basis \( u_1, \ldots, u_M \) of \( U \) with respect to which \( T|_U \) has an upper-triangular matrix. Thus for each \( k \in \{1, \ldots, M\} \), we have
\[
Tu_k = (T|_U)(u_k) \in \operatorname{span}(u_1, \ldots, u_k).
\]
Extend \( u_1, \ldots, u_M \) to a basis \( u_1, \ldots, u_M, v_1, \ldots, v_N \) of \( V \). If \( k \in \{1, \ldots, N\} \), then
\[
Tv_k = (T - \lambda_m I)v_k + \lambda_m v_k.
\]
The definition of \( U \) shows that \( (T - \lambda_m I)v_k \in U = \operatorname{span}(u_1, \ldots, u_M) \). Thus the equation above shows that
\[
Tv_k \in \operatorname{span}(u_1, \ldots, u_M, v_k);
\]
\[
Tv_k \in \operatorname{span}(u_1, \ldots, u_M, v_1, \ldots, v_k).
\]
We conclude that \( T \) has an upper-triangular matrix with respect to the basis 
\[u_1, \ldots, u_M, v_1, \ldots, v_N \]
of \( V \), as desired.
\end{proof}
\begin{remark}
\textcolor{ForestGreen}{Here we attempt another proof, using what we have discussed about invariant subspaces of \(V\) in the previous sections:}

Suppose \(T: V \to V\) and \(V\) is finite-dimensional. Suppose the minimal polynomial of \(T\) is 
\[(T - \lambda_1)^{k_1} ... (T - \lambda_m)^{k_m},\]
where \(\lambda_i\)'s are distinct. We want to show that there  exists a basis \(\mathcal{B}\) for \(V\), such that \([T]_{\mathcal{BB}}\) is upper-triangular. 

By our previous discussion, we know that 
\[V = \ker (T - \lambda_1 I)^{k_1} \oplus ... \oplus \ker (T - \lambda_m)^{k_m},\]
and \(T\) is invariant on \(\ker (T - \lambda_i I)^{k_i}\) for all \(i = 1, 2, ..., m\). 

We suppose \(\mathcal{B} = \mathcal{B}_1 \bigcup ... \bigcup \mathcal{B}_m\) is a basis for \(V\), where each \(\mathcal{B}_i\) is a basis for \(\ker (T - \lambda_i I)^{k_i}\), and \(|\mathcal{B}_i| = n_i\) for each \(i\). Then 
\[[T]_{\mathcal{BB}} [1, 0, ..., 0]^T,\]
the first column vector of \([T]_{\mathcal{BB}}\), is only filled in the first \(n_1\) entries. And similarly for every one of the \(1, 2, ..., n_1\)-th column vectors of \([T]_{\mathcal{BB}}\), they are only filled at the first \(n_1\) entries. 

By the same argument, the \(n_1 + 1, ..., n_1 + n_2\)-th column vectors of \([T]_{\mathcal{BB}}\) are only filled at the \(n_1 + 1\) to \(n_1 + n_2\) entries, the \(n_2 + 1, ..., n_2 + n_3\)-th column vectors of \([T]_{\mathcal{BB}}\) are only filled at the \(n_2 + 1\) to \(n_2 + n_3\) entries, and so on. Therefore, we can see that, if the basis for \(V\) is chosen such that it can be divided into the combination of bases for each \(\ker (T - \lambda_i)^{k_i}\), then the resulting matrix \([T]_{\mathcal{BB}}\) is only filled in square blocks centered at the diagonal of \([T]_{\mathcal{BB}}\). 

In other words, this is a block-diagonal matrix in the form 
\[
\begin{bmatrix}
\boxed{\begin{matrix}
\ast & \cdots & \ast \\
\vdots & \ddots & \vdots \\
\ast & \cdots & \ast
\end{matrix}}_{n_1 \times n_1} & 0 & \cdots & 0 \\[6pt]
0 & \boxed{\begin{matrix}
\ast & \cdots & \ast \\
\vdots & \ddots & \vdots \\
\ast & \cdots & \ast
\end{matrix}}_{n_2 \times n_2} & \cdots & 0 \\[6pt]
\vdots & \vdots & \ddots & \vdots \\[6pt]
0 & 0 & \cdots &
\boxed{\begin{matrix}
\ast & \cdots & \ast \\
\vdots & \ddots & \vdots \\
\ast & \cdots & \ast
\end{matrix}}_{n_m \times n_m}
\end{bmatrix}
\]

Now suppose we pick a general \(i = 1, 2, ..., m\). If we can find a basis in \(V_i = \ker (T - \lambda_i I)^{k_i}\) such that \(T|_{V_i}\) is upper-triangular with respect to it, then since \(i\) is arbitrarily picked, for every block of the big matrix we can pick a basis to make it upper-triangular, thus the proof would be done. 

By re-labeling, denote \(V = \ker (T - \lambda I)^k\) for some \(\lambda \in \mathbb{F}\), and we want to show that there exists a basis \(\mathcal{B}\) for \(V\), such that \([T]_{\mathcal{BB}}\) is upper-triangular. 

Clearly we know that 
\[\ker (T - \lambda I) \subset \ker (T - \lambda I)^2 \subset ... \subset \ker (T - \lambda I)^k,\]
and they are all subspaces of \(V\). Suppose
\[\mathcal{B}_1 = \{v_{1, 1}, v_{1, 2}, ..., v_{1, n_1}\}\]
is a basis for \(\ker (T - \lambda I)\), and \(\mathcal{B}\) is a basis for \(V\) extended from \(\mathcal{B}_1\). Then 
\[[T]_{\mathcal{BB}} [v_{1, 1}]_{\mathcal{B}}, [T]_{\mathcal{BB}} [v_{1, 2}]_{\mathcal{B}}, ..., [T]_{\mathcal{BB}} [v_{1, n_1}]_{\mathcal{B}}\]
are the first \(n_1\) column vectors of \([T]_{\mathcal{BB}}\), and since 
\[\lambda [v_{1, i}]_{\mathcal{B}} = [T]_{\mathcal{BB}} [v_{1, i}]_{\mathcal{B}},\]
they are only filled on the diagonal entries of the matrix, and the values are all \(\lambda\). 

Let 
\[\mathcal{B}_2 = \{v_{2, 1}, v_{2, 2}, ..., v_{2, n_2}\} \bigcup \mathcal{B}_1,\]
where \(\mathcal{B}_2\) form a basis for \(\ker (T - \lambda I)^2\) and it also includes the basis for \(\mathcal{B}_1\) as we have previously defined. Let \(\mathcal{B}\) be a basis for \(V\) extended from \(\mathcal{B}_2\). Then we know that the first \(n_1\) column vectors of \([T]_{\mathcal{BB}}\) are only filled in the diagonal entries of \([T]_{\mathcal{BB}}\), and the values are all \(\lambda\). For 
\[[T]_{\mathcal{BB}} [v_{2, 1}]_{\mathcal{B}}, [T]_{\mathcal{BB}} [v_{2, 2}]_{\mathcal{B}}, ..., [T]_{\mathcal{BB}} [v_{2, n_2}]_{\mathcal{B}},\]
we have 
\[(T - \lambda I)^2 v_{2, i} = 0,\]
which means 
\[(T - \lambda I) v_{2, i} \in \ker (T - \lambda I).\]
Therefore, for each \(i = 1, 2, ..., n_2\), there exists \(x_{1, i}, x_{2, i}, ..., x_{n_1, i}\), such that 
\[(T - \lambda I) v_{2, i} = x_{1, i} v_{1, 1} + x_{2, i} v_{1, 2} + ... + x_{n_1, i} v_{1, n_i} \in \ker (T - \lambda I).\]
Therefore 
\[[T]_{\mathcal{BB}} = [v_{2, i}]_{\mathcal{B}} = x_{1, i} [v_{1, 1}]_{\mathcal{B}} + ... + x_{n_1, i} [v_{1, n_1}]_{\mathcal{B}} + \lambda [v_{2, i}]_{\mathcal{B}},\]
which means the \(n_1 + 1\) to \(n_1 + n_2\) column vectors of \([T]_{\mathcal{BB}}\) are filled on at most the first \(n_1\) entries and the diagonal entry of \([T]_{\mathcal{BB}}\). Moreover, the values on the diagonal entries are all \(\lambda\). 

By the same argument, for 
\[[T]_{\mathcal{BB}} [v_{3, 1}]_{\mathcal{B}}, [T]_{\mathcal{BB}} [v_{3, 2}]_{\mathcal{B}}, ..., [T]_{\mathcal{BB}} [v_{3, n_3}]_{\mathcal{B}},\]
the \(n_2 +1 \) to \(n_2 + n_3\) column vectors of \([T]_{\mathcal{BB}}\), since 
\[(T - \lambda I) v_{3, i} \in \ker (T - \lambda I)^2,\]
they are only filled on the first \(n_1 + n_2\) entries as well as the diagonal entries. And the values on the diagonal entries are all \(\lambda\). 

Since \(V\) is finite-dimensional, this process terminates, and the matrix we get is a square and upper-triangular matrix. Therefore, when we think of 
\[V = \ker (T - \lambda_1 I)^{k_1} \oplus ... \oplus \ker (T - \lambda_m)^{k_m},\]
the big matrix is a block matrix of finitely many upper-triangular blocks, thus also an upper-triangular matrix. 
\end{remark}
\begin{theorem}
Suppose \(V\) is a finite-dimensional complex vector space and \(T \in \mathcal{L}(V)\). Then \(T\) has an upper-triangular matrix with respect to some basis of \(V\). 
\end{theorem}
Proof omitted. 
\section{Diagonal matrices}
\begin{definition}[diagonal matrix]
A diagonal matrix is a square matrix that is \(0\) everywhere except possibly on the diagonals. 
\end{definition}
\begin{corollary}
If an operator \(T\) has a diagonal matrix with respect to some basis then the entries on the diagonals are precisely the eigenvalues of the operator. 
\end{corollary}
Proof omitted. 
\begin{definition}[diagonalizable]
An operator on \(V\) is called diagonalize if the operator has a diagonal matrix with respect to some basis of \(V\). 
\end{definition}
\begin{definition}[eigenspace, \(E(\lambda, T)\)]
Suppose \( T \in \mathcal{L}(V) \) and \( \lambda \in \mathbb{F} \). The \emph{eigenspace} of \( T \) corresponding to \( \lambda \) is the subspace \( E(\lambda, T) \) of \( V \) defined by
\[
E(\lambda, T) = \text{null}(T - \lambda I) = \{ v \in V : Tv = \lambda v \}.
\]
Hence \( E(\lambda, T) \) is the set of all eigenvectors of \( T \) corresponding to \( \lambda \), along with the 0 vector.
\end{definition}
\begin{theorem}
Suppose \( T \in \mathcal{L}(V) \) and \( \lambda_1, \ldots, \lambda_m \) are distinct eigenvalues of \( T \). Then
\[
E(\lambda_1, T) + \cdots + E(\lambda_m, T)
\]
is a direct sum. Furthermore, if \( V \) is finite-dimensional, then
\[
\dim E(\lambda_1, T) + \cdots + \dim E(\lambda_m, T) \leq \dim V.
\]
\end{theorem}
\begin{proof}
We have showed that any set of eigenvectors corresponding to different eigenvalues are linearly independent. 

Therefore, in terms of dimensions, we have
\[\dim E (\lambda_1, T) + ... + \dim (\lambda_m, T) = \dim (E(\lambda_1, T) \oplus ... \oplus E(\lambda_m, T))\]
\[\leq \dim V.\]
\end{proof}
\section{Diagonalizability}
\begin{theorem}
Suppose \( V \) is finite-dimensional and \( T \in \mathcal{L}(V) \). Let \( \lambda_1, \ldots, \lambda_m \) denote the distinct eigenvalues of \( T \). Then the following are equivalent.
\begin{itemize}
  \item[(a)] \( T \) is diagonalizable.
  \item[(b)] \( V \) has a basis consisting of eigenvectors of \( T \).
  \item[(c)] \( V = E(\lambda_1, T) \oplus \cdots \oplus E(\lambda_m, T) \).
  \item[(d)] \( \dim V = \dim E(\lambda_1, T) + \cdots + \dim E(\lambda_m, T) \).
\end{itemize}
\end{theorem}
\begin{proof}
Denote \(\dim V = M\). 

Suppose \((a)\) is true. Then there exists a basis 
\[\mathcal{B} \{v_1, ..., v_M\}\]
for \(V\), such that \([T]_{\mathcal{BB}}\) is a diagonal matrix. We denote the matrix as 
\[
\begin{bmatrix}
\lambda_1 & 0         & \cdots & 0 \\
0         & \lambda_2 & \cdots & 0 \\
\vdots    & \vdots    & \ddots & \vdots \\
0         & 0         & \cdots & \lambda_M
\end{bmatrix}.
\]
Now each vector in the basis is an eigenvector corresponding to some \(\lambda_i\). Therefore \((a) \Longrightarrow (b)\). 

Suppose \((b)\) is true. Then \(V\) has a basis 
\[\mathcal{B} = \mathcal{B}_1 \bigcup \mathcal{B}_2 \bigcup ... \bigcup \mathcal{B}_m,\]
where each \(\mathcal{B}_i\) corresponds to a basis for the eigenspace \(E(\lambda_i, T)\). Then 
\[V = E(\lambda_1, T) \oplus \cdots \oplus E(\lambda_m, T).\]
Therefore
\[\dim V = \dim E(\lambda_1, T) + \cdots + \dim E(\lambda_m, T).\]
Therefore \((b) \Longrightarrow (c) \Longrightarrow (d)\). 

Suppose \((d)\) is true. Then we pick a basis \(\mathcal{B}_i\) for each \(E(\lambda_i, T)\), then 
\[\mathcal{B} = \mathcal{B}_1 \bigcup ... \bigcup \mathcal{B}_m\]
is a set of linearly independent vectors, while \(|\mathcal{B}| = \dim V\) and \(\mathcal{B} \subseteq V\). Therefore \(\mathcal{B}\) is a basis for \(V\). Therefore, denote
\[\mathcal{B} = \{v_{1, 1}, ..., v_{1, \dim E(\lambda_1, T)}, v_{2, 1}, ..., v_{2, \dim E(\lambda_2, T)}, ..., v_{m, 1}, ..., v_{m, \dim E (\lambda_m, T)}\},\]
then \([T]_{\mathcal{BB}}\) is diagonal. Therefore \(T\) is diagonalizable, which means \((d) \Longrightarrow (a)\).
\end{proof}
\begin{theorem}
Suppose \(V\) is finite-dimensional and \(T \in \mathcal{L}(V)\) has \(\dim V\) distinct eigenvalues. Then \(T\) is diagonalizable. 
\end{theorem}
\begin{proof}
Let \(v_k\) be the corresponding eigenvector to the eigenvalue \(\lambda_k\). Since the eigenvalues are distinct, the vectors \(v_1, ..., v_{\dim V}\) are linearly independent, thus a basis for \(V\). The rest is omitted. 
\end{proof}
\begin{theorem}
Suppose \(V\) is finite-dimensional and \(T \in \mathcal{L}(V)\). Then \(T\) is diagonalizable if and only if the minimal polynomial of \(T\) equals 
\[(T - \lambda_1 I) ... (T - \lambda_m I)\]
for some list of distinct numbers \(\lambda_1, ..., \lambda_m \in \mathbb{F}\). 
\end{theorem}
\begin{proof}
Suppose \(T\) is diagonalizable. Then \(T\) has a diagonal matrix representation with respect to some basis \(\mathcal{B} = \{v_1, ..., v_n\}\), where \(n = \dim V\). Then each of the basis vector \(v_k\) has a column vector representation \([0, ..., 0, 1, 0, ..., 0]^T\), where only the \(k\)-th entry is 1 and all other entries 0. Therefore, since we know that the matrix representation of \(T\) is also upper-triangular, the eigenvalues are precisely the entries on the diagonals, so \(T\) has \(n\) eigenvalues (counting multiplicities) corresponding to \(n\) basis vectors. Therefore when we pick any \(v \in V\) such that 
\[v = x_1 v_1 + ... + x_n v_n,\]
the polynomial 
\[p(T) = (T - \lambda_1 I) ... (T - \lambda_m I)\]
annihilates \(v\). Therefore \(p(T)\) is a polynomial multiple of the minimal polynomial. To show that \(p(T)\) is actually the minimal polynomial, note that when we take any non-identity factor out of \(p(T)\), the polynomial cannot annihilate any 
\[v = x_1 v_1 + ... + x_n v_n \in V\]
such that \(x_1 x_2 ... x_n \ne 0\). 

Suppose the minimal polynomial of \(T\) is 
\[p(T) = (T - \lambda_1 I) ... (T - \lambda_m I)\]
with distinct numbers \(\lambda_1, ..., \lambda_m \in \mathbb{F}\). Then \(\lambda_1, ..., \lambda_m\) are precisely the eigenvalues of \(T\). By our previous discussion, this means 
\[V = \ker (T - \lambda_1) \oplus \ker (T - \lambda_2) \oplus ... \oplus \ker (T - \lambda_m)\]
\[= E(\lambda_1, T) \oplus \cdots \oplus E(\lambda_m, T).\]
\textcolor{ForestGreen}{(In the book, this part of the proof follows from induction. See later.)} Then according to our previous theorem of equivalences, the condition 
\[V = E(\lambda_1, T) \oplus \cdots \oplus E(\lambda_m, T)\]
is equivalent to \(T\) being diagonalizable. 

\textcolor{ForestGreen}{The proof from the book:}

To prove the implication in the other direction, now suppose the minimal polynomial of \( T \) equals 
\[
(z - \lambda_1) \cdots (z - \lambda_m)
\]
for some list of distinct numbers \( \lambda_1, \ldots, \lambda_m \in \mathbb{F} \). Thus

\begin{equation*}
(T - \lambda_1 I) \cdots (T - \lambda_m I) = 0. 
\end{equation*}

We will prove that \( T \) is diagonalizable by induction on \( m \). To get started, suppose \( m = 1 \). Then \( T - \lambda_1 I = 0 \), which means that \( T \) is a scalar multiple of the identity operator, which implies that \( T \) is diagonalizable.

Now suppose that \( m > 1 \) and the desired result holds for all smaller values of \( m \). The subspace \( \operatorname{range}(T - \lambda_m I) \) is invariant under \( T \). Thus \( T \) restricted to \( \operatorname{range}(T - \lambda_m I) \) is an operator on \( \operatorname{range}(T - \lambda_m I) \).

If \( u \in \operatorname{range}(T - \lambda_m I) \), then \( u = (T - \lambda_m I)v \) for some \( v \in V \), and we have
\begin{equation*}
(T - \lambda_1 I) \cdots (T - \lambda_{m-1} I) u = (T - \lambda_1 I) \cdots (T - \lambda_m I) v = 0. 
\end{equation*}
Hence \( (z - \lambda_1) \cdots (z - \lambda_{m-1}) \) is a polynomial multiple of the minimal polynomial of \( T \) restricted to \( \operatorname{range}(T - \lambda_m I) \). Thus by our induction hypothesis, there is a basis of \( \operatorname{range}(T - \lambda_m I) \) consisting of eigenvectors of \( T \).

Suppose that \( u \in \operatorname{range}(T - \lambda_m I) \cap \operatorname{null}(T - \lambda_m I) \). Then \( Tu = \lambda_m u \). Now we can have
\[
0 = (T - \lambda_1 I) \cdots (T - \lambda_{m-1} I) u \\
= (\lambda_m - \lambda_1) \cdots (\lambda_m - \lambda_{m-1}) u.
\]
Because \( \lambda_1, \ldots, \lambda_m \) are distinct, the equation above implies that \( u = 0 \). Hence
\[
\operatorname{range}(T - \lambda_m I) \cap \operatorname{null}(T - \lambda_m I) = \{0\}.
\]
Thus \( \operatorname{range}(T - \lambda_m I) + \operatorname{null}(T - \lambda_m I) \) is a direct sum whose dimension is \( \dim V \). Hence
\[
\operatorname{range}(T - \lambda_m I) \oplus \operatorname{null}(T - \lambda_m I) = V.
\]
Every nonzero vector in \( \operatorname{null}(T - \lambda_m I) \) is an eigenvector of \( T \) with eigenvalue \( \lambda_m \). Earlier in this proof we saw that there is a basis of \( \operatorname{range}(T - \lambda_m I) \) consisting of eigenvectors of \( T \). Adjoining to that basis a basis of \( \operatorname{null}(T - \lambda_m I) \) gives a basis of \( V \) consisting of eigenvectors of \( T \). The matrix of \( T \) with respect to this basis is a diagonal matrix, as desired.
\end{proof}
\begin{remark}
Now we know a connection between diagonalizability of the matrix representation of \(T: V \to V\), and its minimal polynomials. To be precise, if the minimal polynomial 
\[p(T) = (T - \lambda_1 I)(T - \lambda_2 I)...(T - \lambda_m I)\]
factors into distinct \(\lambda_1, ..., \lambda_m\), then \(T\) is diagonalizable. If the minimal polynomial factors into \(\lambda_i\)'s with repetitions, then \(T\) has an upper-triangular matrix representation. \textcolor{red}{The diagonalizability of \(T\) is not sure from this context.} 
\end{remark}
\begin{theorem}
Suppose \(\mathcal{L}(V)\) is diagonalizable and \(U\) is a subspace of \(V\) that is invariant under \(T\). Then \(T|_{U}\) is a diagonalizable operator on \(U\). 
\end{theorem}
\begin{proof}
Suppose \(T\) is diagonalizable. Then let \(n = \dim V\), and there exists a basis \(\mathcal{B}\) for \(V\) such that \(\mathcal{B} = \{v_1, ..., v_n\}\) where the matrix representation of \(T\) with respect to \(\mathcal{B}\) is a diagonal matrix, which implies each \(v_k\) is an eigenvector with respect to some eigenvalue. Therefore the minimal polynomial of \(T\) is in the form 
\[p(T) = (T - \mu_1 I)...(T - \mu_m I),\]
where the \(\mu\)'s are distinct eigenvalues. Therefore \(p(T)\) is a polynomial multiple of the minimal polynomial of \(T|_{U}\). Therefore the minimal polynomial of \(T|_{U}\) also factors into \((T - \mu)\) for distinct \(\mu\)'s, which means, by our previous theorem, \(T|_{U}\) is diagonalizable. 
\end{proof}
\begin{example}
The Fibonacci sequence \( F_0, F_1, F_2, \ldots \) is defined by
\[
F_0 = 0,\quad F_1 = 1,\quad \text{and} \quad F_n = F_{n-2} + F_{n-1} \quad \text{for } n \geq 2.
\]

Define \( T \in \mathcal{L}(\mathbb{R}^2) \) by \( T(x, y) = (y, x + y) \).

\begin{itemize}
\item[(a)] Show that \( T^n(0, 1) = (F_n, F_{n+1}) \) for each nonnegative integer \( n \).
\begin{proof}
First of all, \(T[x, y] = [y, x+y]\) means the matrix representation of \(T\) is 
\[\begin{bmatrix}
0 & 1 \\
1 & 1
\end{bmatrix}\]
and we know that \(T (0, 1) = (1, 1) = (F_1, F_2)\). Suppose \(T^{n-1}(0, 1) = (F_{n-1}, F_n)\), then by mathematical induction, we indeed have \(T^n (0, 1) = T T^{n-1}(0, 1) = T (F_{n-1}, F_n) = (F_n, F_{n-1}+ F_n) = (F_n, F_{n+1})\). 
\end{proof}
\item[(b)] Find the eigenvalues of \( T \).
We suppose for the eigenvector(s), the ratio between the first and the second entry is \(x\) and the corresponding eigenvalue is \(\lambda\), then we have  
\[\begin{bmatrix}
0 & 1 \\
1 & 1
\end{bmatrix} 
\begin{bmatrix}
x  \\
1 
\end{bmatrix} = 
\begin{bmatrix}
1  \\
1 + x
\end{bmatrix} =
\begin{bmatrix}
\lambda x  \\
\lambda
\end{bmatrix}.\]
Therefore we get \(x^2 + x - 1 = 0\), which means 
\[x = -\frac{1}{2} + \frac{\sqrt{5}}{2}\]
or 
\[x = -\frac{1}{2} - \frac{\sqrt{5}}{2}.\]
And we have, for eigenvector 
\[
\begin{bmatrix}
-\frac{1}{2} + \frac{\sqrt{5}}{2}  \\
1 
\end{bmatrix},
\]
the corresponding eigenvalue is \(\frac{1}{2} + \frac{\sqrt{5}}{2}\); while for the eigenvector 
\[
\begin{bmatrix}
-\frac{1}{2} - \frac{\sqrt{5}}{2}  \\
1 
\end{bmatrix},
\]
the corresponding eigenvalue is \(\frac{1}{2} - \frac{\sqrt{5}}{2}\). 
\item[(c)] Find a basis of \( \mathbb{R}^2 \) consisting of eigenvectors of \( T \).
\begin{proof}
The two corresponding eigenvectors found in the previous step can form a basis. 
\end{proof}
\item[(d)] Use the solution to (c) to compute \( T^n(0, 1) \). Conclude that
\[
F_n = \frac{1}{\sqrt{5}} \left[ \left( \frac{1 + \sqrt{5}}{2} \right)^n - \left( \frac{1 - \sqrt{5}}{2} \right)^n \right]
\]
for each nonnegative integer \( n \).
\begin{proof}
Suppose \(v = x_1 v_1 + x_2 v_2\) where \(v_1\) and \(v_2\) are the corresponding eigenvectors. Then we know that \(T v = x_1 T v_1 + x_2 T v_2\), and denoting the corresponding eigenvalues as \(\lambda_1\) and \(\lambda_2\), we have \(T v = x_1 \lambda_1 v_1 + x_2 \lambda_2 v_2\), and \(T^2 v = x_1 \lambda_1^2 v_1 + x_2 \lambda_2^2 v_2\), therefore by mathematical induction, \(T^n v = x_1 \lambda_1^n v_1 + x_2 \lambda_2^n v_2\). We know that 
\[
\begin{bmatrix}
0  \\
1 
\end{bmatrix} = 
\frac{1}{\sqrt{5}} \left[ \left(\frac{1 + \sqrt{5}}{2}\right) v_1 + \left(\frac{- 1 + \sqrt{5}}{2}\right) v_2 \right]
\]
so 
\[T^n
\begin{bmatrix}
0  \\
1 
\end{bmatrix} = 
\frac{1}{\sqrt{5}} \left[ \left(\frac{1 + \sqrt{5}}{2}\right) \left(\frac{1 + \sqrt{5}}{2}\right)^n v_1 + \left(\frac{- 1 + \sqrt{5}}{2}\right) \left(\frac{1 - \sqrt{5}}{2}\right)^n v_2 \right]
\]
\[= 
\begin{bmatrix}
F_n  \\
F_{n+1} 
\end{bmatrix}.
\]
Therefore plug in values of \(v_1\) and \(v_2\) we get 
\[F_n = \frac{1}{\sqrt{5}} \left[ \left( \frac{1 + \sqrt{5}}{2} \right)^n - \left( \frac{1 - \sqrt{5}}{2} \right)^n \right].\]
\end{proof}
\item[(e)] Use (d) to conclude that if \( n \) is a nonnegative integer, then the Fibonacci number \( F_n \) is the integer that is closest to
\[
\frac{1}{\sqrt{5}} \left( \frac{1 + \sqrt{5}}{2} \right)^n.
\]
\end{itemize}

\textcolor{ForestGreen}{Each \( F_n \) is a nonnegative integer, even though the right side of the formula in (d) does not look like an integer. The number
\[
\frac{1 + \sqrt{5}}{2}
\]
is called the \textbf{golden ratio}.}
\begin{proof}
Omitted. 
\end{proof}
\end{example}
\section{Gershgorin Disk theorem}
\begin{theorem}[Gershgorin disks]
Suppose \( T \in \mathcal{L}(V) \) and \( v_1, \ldots, v_n \) is a basis of \( V \). Let \( A \) denote the matrix of \( T \) with respect to this basis. A \textit{Gershgorin disk} of \( T \) with respect to the basis \( v_1, \ldots, v_n \) is a set of the form
\[
\left\{ z \in \mathbb{F} : |z - A_{j,j}| \leq \sum_{\substack{k = 1 \\ k \ne j}}^n |A_{j,k}| \right\},
\]
where \( j \in \{1, \ldots, n\} \).
\end{theorem}
\begin{remark}
For \(\dim V = n\), there are \(n\) choices for \(j\) in the definition above, so \(T\) has \(n\) Gershgorin disks. If \(\mathbb{F} = \mathbb{C}\), then for each \(j \in \{1, 2, ..., n\}\), the corresponding Gershgorin disk is a closed disk in \(\mathbb{C}\) centered at \(A_{j, j}\). If \(\mathbb{F} = \mathbb{R}\), then the Gershgorin disks are closed intervals in \(\mathbb{R}\). 
\end{remark}
\begin{theorem}[Gershgorin disk theorem]
Suppose \( T \in \mathcal{L}(V) \) and \( v_1, \ldots, v_n \) is a basis of \( V \). Then each eigenvalue of \( T \) is contained in some Gershgorin disk of \( T \) with respect to the basis \( v_1, \ldots, v_n \).
\end{theorem}
\begin{proof}
Suppose \(\mathcal{B} = \{v_1, \ldots, v_n\}\) is a basis for \(V\), and let \(A = [T]_{\mathcal{BB}}\). We have 
\[
T v_k = \sum_{i = 1}^n A_{i, k} v_i.
\]
Suppose
\[
v = \sum_{i = 1}^n x_i v_i
\]
is an eigenvector corresponding to some eigenvalue \(\lambda\), then we have
\[
\lambda v = T v,
\]
and therefore
\[
\lambda \sum_{i = 1}^n x_i v_i = \sum_{i = 1}^n x_i T v_i 
= \sum_{i = 1}^n x_i \sum_{j = 1}^n A_{j, i} v_j 
= \sum_{i = 1}^n \sum_{j = 1}^n x_i A_{j, i} v_j 
= \sum_{i = 1}^n \sum_{j = 1}^n x_j A_{i, j} v_i.
\]
Since \(v_i\) form a basis, we have, for any \(i = 1, 2, \ldots, n\),
\[
\lambda x_i v_i = \sum_{j = 1}^n x_j A_{i, j} v_i,
\]
which implies
\[
\lambda x_i = \sum_{j = 1}^n x_j A_{i, j}
\]
for all \(i = 1, 2, \ldots, n\). We now pick the \(i \in \{1, 2, \ldots, n\}\) such that 
\[
\left| x_i \right| = \max \left( \left| x_1 \right|, \left| x_2 \right|, \ldots, \left| x_n \right| \right).
\]
Then we have
\[
(\lambda - A_{i,i}) x_i = \sum_{j = 1,\, j \ne i}^n x_j A_{i,j},
\]
which implies
\[
\lambda - A_{i,i} = \sum_{j = 1,\, j \ne i}^n \frac{x_j}{x_i} A_{i,j},
\]
and
\[
\left| \lambda - A_{i,i} \right| \leq \sum_{j = 1,\, j \ne i}^n \left| \frac{x_j}{x_i} A_{i,j} \right|,
\]
where each \( \left| \frac{x_j}{x_i} \right| \leq 1 \). Therefore we have
\[
\left| \lambda - A_{i,i} \right| \leq \sum_{j = 1,\, j \ne i}^n \left| \frac{x_j}{x_i} A_{i,j} \right| \leq \sum_{j = 1,\, j \ne i}^n \left| A_{i,j} \right|.
\]
\end{proof}
\section{Commuting operators}
\begin{definition}
\begin{itemize}
    \item Two operators \(S\) and \(T\) on the same vector space commute if \(ST = TS\).
    \item Two square matrices \(A\) and \(B\) of the same size commute if \(AB = BA\). 
\end{itemize}
\end{definition}
\begin{example}
Partial differentiation operators commute. 
\end{example}
\begin{theorem}
Suppose \( S, T \in \mathcal{L}(V) \) and \( v_1, \ldots, v_n \) is a basis of \( V \). Then \( S \) and \( T \) commute if and only if 
\[
\mathcal{M}(S, (v_1, \ldots, v_n)) \quad \text{and} \quad \mathcal{M}(T, (v_1, \ldots, v_n))
\]
commute.
\end{theorem}
\begin{proof}
\begin{align*}
S \text{ and } T \text{ commute} &\iff ST = TS \\
&\iff \mathcal{M}(ST) = \mathcal{M}(TS) \\
&\iff \mathcal{M}(S)\mathcal{M}(T) = \mathcal{M}(T)\mathcal{M}(S) \\
&\iff \mathcal{M}(S) \text{ and } \mathcal{M}(T) \text{ commute}.
\end{align*}
\end{proof}
\begin{theorem}
Suppose \(S\), \(T\) \(: V \to V\) commute and \(\lambda \in \mathbb{F}\). Then \(E(\lambda, S)\) is invariant under \(T\).
\end{theorem}
\begin{proof}
Suppose \(v \in E(\lambda, S)\), then \(S(T v) = T S v = T (\lambda v) = \lambda (Tv)\), which means \(Tv \in E(\lambda, S)\) as well, which implies \(E(\lambda, S)\) is invariant under \(T\).  
\end{proof}
\begin{theorem}
Two diagonalizable operators on the same vector space have diagonal matrices with respect to the same basis if and only if the two operators commute.
\end{theorem}
\begin{proof}
Let \(T, S \in \mathcal{L}(V)\) be diagonalizable operators. 

Suppose \(T\) and \(S\) commute. Denote distinct eigenvalues of \(S\) as \(\lambda_1, ..., \lambda_m\). 

Recall that if \(T: V \to V\) is diagonalizable, and \(U \subset V\) is an invariant subspace under \(T\), then \(T|_{U}\) is also diagonalizable. Since \(T\) is invariant on \(E(\lambda_i, S)\) for \(i = 1, 2, ..., m\), \(T\) is diagonalizable on \(E(\lambda_i, S)\) for all \(i\). 

For each \(i = 1, 2, ..., m\), we pick a basis \(\mathcal{B}_i\) for \(E(\lambda_i, S)\), such that 
\[[T|_{E(\lambda_i, S)}]_{\mathcal{B}_i \mathcal{B}_i} \]
is a diagonal matrix. Then denoting
\[\mathcal{B}_i = \{v_{i, 1}, v_{i, 2}, ..., v_{i, k_i}\},\]
there exists eigenvalues \(\mu_{i, j}\) such that \(T v_{i, j} = \mu_{i, j} v_{i, j}\). Now we denote
\[\mathcal{B} = \mathcal{B}_1 \bigcup \mathcal{B}_2 \bigcup ... \bigcup \mathcal{B}_m,\]
then \(\mathcal{B}\) is a basis for \(V\), and with respect to which the matrix of \(T\) is a diagonal matrix with diagonals 
\[\mu_{1, 1}, ..., \mu_{1, k_1}, ..., \mu_{m, 1}, ..., \mu_{m ,k_m}.\]
On the other hand, the matrix of \(S\) with respect to \(\mathcal{B}\) is also a diagonal matrix with diagonal entries \(\lambda_1, ..., \lambda_m\) repeated. 

Suppose \(S\) and \(T\) have diagonal matrices with respect to the same basis, then we denote the basis as 
\[\mathcal{B} = \{v_1, ..., v_N\}\]
for \(N = \dim V\). Therefore \([T]_{\mathcal{BB}}\) and \([S]_{\mathcal{BB}}\) are both diagonal matrices, which means they commute. Therefore \(T\) and \(S\) commute as linear operators. 
\end{proof}
\begin{theorem}
Every pair of commuting operators on a finite-dimensional nonzero complex vector space has a common eigenvector. 
\end{theorem}
\begin{proof}
Suppose \(V\) is a finite-dimensional vector space over \(\mathbb{C}\). Recall that for finite dimensional complex vector spaces, \(S\) and \(T\) indeed have at least one eigenvalue. 

Suppose \(S\) has an eigenvalue \(\lambda\), then since \(S\) and \(T\) commute, \(E(\lambda, S)\) is invariant under \(T\). Therefore \(T|_{E(\lambda, S)}\) has at least one eigenvalue and corresponding eigenvectors. Therefore the eigenvector, which is in \(E(\lambda, S)\), is an eigenvector for \(S\) as well. Therefore \(T\) and \(S\) have a common eigenvector. 
\end{proof}
\begin{theorem}
Suppose \( V \) is a finite-dimensional complex vector space and \( S, T \) are commuting operators on \( V \). Then there is a basis of \( V \) with respect to which both \( S \) and \( T \) have upper-triangular matrices.
\end{theorem}
\begin{proof}
\textcolor{ForestGreen}{The proof from the book:}

Let \( n = \dim V \). We will use induction on \( n \). The desired result holds if \( n = 1 \) because all \( 1\)-by-\(1\) matrices are upper triangular. Now suppose \( n > 1 \) and the desired result holds for all complex vector spaces whose dimension is \( n - 1 \).

Let \( v_1 \) be any common eigenvector of \( S \) and \( T \). Hence \( S v_1 \in \mathrm{span}(v_1) \) and \( T v_1 \in \mathrm{span}(v_1) \). Let \( W \) be a subspace of \( V \) such that
\[
V = \mathrm{span}(v_1) \oplus W;
\]
Define a linear map \( P : V \to W \) by
\[
P(a v_1 + w) = w
\]
for each \( a \in \mathbb{C} \) and each \( w \in W \). \textcolor{blue}{Note that this definition means, for any vector \(v \in V\), \(P v\) is its projection in \(W\). Since \(V = W \oplus \operatorname{span} \{v_1\}\), the decomposition of \(v\) into components in \(W\) and \(\operatorname{span}\{v_1\}\) is unique. }

Define \( \hat{S}, \hat{T} \in \mathcal{L}(W) \) by
\[
\hat{S}w = P(Sw) \quad\text{and}\quad \hat{T}w = P(Tw)
\]
for each \( w \in W \). To apply our induction hypothesis to \( \hat{S} \) and \( \hat{T} \), we must first show that these two operators on \( W \) commute. To do this, suppose \( w \in W \). Then there exists \( a \in \mathbb{C} \) such that
\[
(\hat{S} \hat{T}) w = \hat{S} (P(Tw)) = \hat{S}(Tw - a v_1) = P(S(Tw - a v_1)) = P\big(S(Tw) - a S v_1\big) = P((ST) w),
\]
where the last equality holds because \( v_1 \) is an eigenvector of \( S \) and \( P v_1 = 0 \).  

Similarly,
\[
(\hat{T} \hat{S}) w = P((TS) w).
\]
Because the operators \( S \) and \( T \) commute, the last two displayed equations show that \( (\hat{S} \hat{T}) w = (\hat{T} \hat{S}) w \). Hence \( \hat{S} \) and \( \hat{T} \) commute.

Thus we can use our induction hypothesis to state that there exists a basis \( v_2, \dots, v_n \) of \( W \) such that \( \hat{S} \) and \( \hat{T} \) both have upper-triangular matrices with respect to this basis. The list \( v_1, \dots, v_n \) is a basis of \( V \).

If \( k \in \{2, \dots, n\} \), then there exist \( a_k, b_k \in \mathbb{C} \) such that
\[
S v_k = a_k v_1 + \hat{S} v_k \quad\text{and}\quad T v_k = b_k v_1 + \hat{T} v_k.
\]
Because \( \hat{S} \) and \( \hat{T} \) have upper-triangular matrices with respect to \( v_2, \dots, v_n \), we know that \( \hat{S} v_k \in \mathrm{span}(v_2, \dots, v_k) \) and \( \hat{T} v_k \in \mathrm{span}(v_2, \dots, v_k) \). Hence the equations above imply that
\[
S v_k \in \mathrm{span}(v_1, \dots, v_k) \quad\text{and}\quad T v_k \in \mathrm{span}(v_1, \dots, v_k).
\]
Thus \( S \) and \( T \) have upper-triangular matrices with respect to \( v_1, \dots, v_n \), as desired.
\end{proof}
\begin{remark}
Another proof:

Suppose the minimal polynomial for \(T\) is 
\[(T - \lambda_1 I)^{k_1} ... (T - \lambda_m I)^{k_m},\]
for distinct \(\lambda_1, ..., \lambda_m\). Then 
\[V = \ker (T - \lambda_1 I)^{k_1} \oplus ... \oplus \ker (T - \lambda_m I)^{k_m}.\]
Since \(T\) and \(S\) commute, every \(\ker (T - \lambda_i I)^{k_i}\) is invariant under \(S\) for \(i = 1, 2, ..., m\). 

If we can show that, for each \(\ker (T - \lambda_i I)^{k_i}\), there exists a basis \(\mathcal{A}_i\) such that 
\[[T|_{\ker (T - \lambda_i I)^{k_i}}]_{\mathcal{A}_i} \text{ and } [S|_{\ker (T - \lambda_i I)^{k_i}}]_{\mathcal{A}_i}\]
are both upper-triangular, then we are done. 

By re-labeling, denote \(V = \ker (T - \lambda I)^k\), the proof would be the same as showing that there exists a basis \(\mathcal{B}\) for \(V\), such that \([T]_{\mathcal{BB}}\) and \([S]_{\mathcal{BB}}\) are both upper-triangular. 

We know that 
\[\ker (T - \lambda I) \subseteq \ker (T - \lambda I)^2 \subseteq ... \subseteq \ker (T - \lambda I)^k = V,\] and they are all layers of subspaces of \(V\). For simplicity, we denote \(V_i = \ker (T - \lambda I)^i\) for all \(i = 1, 2, ..., k\). 

Since \(T\) and \(S\) commute, \(S\) is invariant on all \(V_i\). 

We know that, if we pick a basis \(\mathcal{B}_1\) for \(V_1\), and extend it into a basis \(\mathcal{B}_2\) for \(V_2\), and further extend it into a basis \(\mathcal{B}_3\) for \(V_3\), etc, until we get to a basis \(\mathcal{B}\) for \(V\), then the matrix of \(T\) with respect to \(\mathcal{B}\) is upper-triangular. 

Suppose the minimal polynomial of \(S|_{V_1}\) is 
\[(S - \mu_1 I)^{e_{1, 1}} (S - \mu_2 I)^{e_{2, 1}} ... (S - \mu_n I)^{e_{n, 1}},\]
the minimal polynomial of \(S|_{V_2}\) is 
\[(S - \mu_1 I)^{e_{1, 2}} (S - \mu_2 I)^{e_{2, 2}} ... (S - \mu_n I)^{e_{n, 2}},\]
\[\vdots\]
and the minimal polynomial of \(S|_{V}\) is 
\[(S - \mu_1 I)^{e_{1, k}} (S - \mu_2 I)^{e_{2, k}} ... (S - \mu_n I)^{e_{n, k}},\]
for some integers \(e_{i, j}\) such that
\[0 \leq e_{1, 1} \leq e_{1, 2} \leq ... \leq e_{1, k-1} \leq e_{1, k};\]
\[0 \leq e_{2, 1} \leq e_{2, 2} \leq ... \leq e_{2, k-1} \leq e_{2, k};\]
\[\vdots\]
\[0 \leq e_{n, 1} \leq e_{n, 2} \leq ... \leq e_{n, k-1} \leq e_{n, k}.\]
Now we can find a basis \(\mathcal{B}_1 (\mu_1)\) for \(\ker (S - \mu_1 I)\), and extend it into a basis \(\mathcal{B}_2 (\mu_1)\) for \(\ker (S - \mu_1 I)^2\), and further extend it into a basis \(\mathcal{B}_3 (\mu_1)\) for \(\ker (S - \mu_1 I)^3\), etc, until we get a basis \(\mathcal{B}_{e_{1, k}} (\mu_1)\) for \(\ker (S - \mu_1 I)^{e_{1, k}}\). Similarly, we can find a basis \(\mathcal{B}_1 (\mu_2)\) for \(\ker (S - \mu_2 I)\), and extend it into a basis \(\mathcal{B}_2 (\mu_2)\) for \(\ker (S - \mu_2 I)^2\), and further extend it into a basis \(\mathcal{B}_3 (\mu_2)\) for \(\ker (S - \mu_2 I)^3\), etc, until we get a basis \(\mathcal{B}_{e_{2, k}} (\mu_1)\) for \(\ker (S - \mu_1 I)^{e_{2, k}}\). In general, we can find a basis \(\mathcal{B}_1 (\mu_i)\) for \(\ker (S - \mu_i I)\), and extend it into a basis \(\mathcal{B}_2 (\mu_i)\) for \(\ker (S - \mu_i I)^2\), and further extend it into a basis \(\mathcal{B}_3 (\mu_i)\) for \(\ker (S - \mu_i I)^3\), etc, until we get a basis \(\mathcal{B}_{e_{i, k}} (\mu_i)\) for \(\ker (S - \mu_i I)^{e_{i,k}}\) for all \(i = 1, 2, ..., n\).

Let 
\[\mathcal{B} = \mathcal{B}_{e_{1, k}} (\mu_1) \bigcup \mathcal{B}_{e_{2, k}} (\mu_2) \bigcup ... \bigcup \mathcal{B}_{e_{n, k}} (\mu_n),\]
then the matrices of \(T\) and \(S\) with respect to \(\mathcal{B}\) are both upper-triangular. 
\end{remark}
\begin{theorem}
Suppose \( V \) is a finite-dimensional complex vector space and \( S, T \) are commuting operators on \( V \). Then
\begin{itemize}
    \item every eigenvalue of \( S + T \) is an eigenvalue of \( S \) plus an eigenvalue of \( T \),
    \item every eigenvalue of \( ST \) is an eigenvalue of \( S \) times an eigenvalue of \( T \).
\end{itemize}
\end{theorem}
\begin{proof}
There is a basis of \( V \) with respect to which both \( S \) and \( T \) have upper-triangular matrices. With respect to that basis,
\[
\mathcal{M}(S + T) = \mathcal{M}(S) + \mathcal{M}(T)
\quad\text{and}\quad
\mathcal{M}(ST) = \mathcal{M}(S) \, \mathcal{M}(T),
\]
and the rest is omitted. 
\end{proof}
\newpage
\chapter{Inner Product Spaces}
\section{Inner products}
\begin{definition}
For \( x, y \in \mathbb{R}^n \), the \emph{dot product} of \( x \) and \( y \), denoted by \( x \cdot y \), is defined by
\[
x \cdot y = x_1 y_1 + \cdots + x_n y_n,
\]
where \( x = (x_1, \ldots, x_n) \) and \( y = (y_1, \ldots, y_n) \).
\end{definition}
\begin{corollary}
There are a few properties of dot product:
\begin{itemize}
    \item \( x \cdot x \ge 0 \) for all \( x \in \mathbb{R}^n \).
    \item \( x \cdot x = 0 \) if and only if \( x = 0 \).
    \item For \( y \in \mathbb{R}^n \) fixed, the map from \( \mathbb{R}^n \) to \( \mathbb{R} \) that sends \( x \in \mathbb{R}^n \) to \( x \cdot y \) is linear.
    \item \( x \cdot y = y \cdot x \) for all \( x, y \in \mathbb{R}^n \).
\end{itemize}
\end{corollary}
\begin{corollary}
For $ z = (z_1, \dots, z_n) \in \mathbb{C}^n $, we define the norm of $z$ by
\[
\|z\| = \sqrt{|z_1|^2 + \cdots + |z_n|^2}.
\]
The absolute values are needed because we want $\|z\|$ to be a nonnegative number. Note that
\[
\|z\|^2 = z_1\overline{z_1} + \cdots + z_n\overline{z_n}.
\]
We think of $\|z\|^2$ as the inner product of $z$ with itself, as in $\mathbb{R}^n$. This suggests that the inner product of $ w = (w_1, \dots, w_n) \in \mathbb{C}^n $ with $z$ should equal
\[
w_1\overline{z_1} + \cdots + w_n\overline{z_n}.
\]
\end{corollary}
\begin{definition}[Inner product]
An \emph{inner product} on $V$ is a function that takes each ordered pair $(u,v)$ of elements of $V$ to a number $\langle u,v \rangle \in \mathbb{F}$ and has the following properties:
\begin{enumerate}
    \item \textbf{Positivity:} $\langle v,v \rangle \geq 0$ for all $v \in V$.
    \item \textbf{Definiteness:} $\langle v,v \rangle = 0$ if and only if $v = 0$.
    \item \textbf{Additivity in first slot:} $\langle u+v,w \rangle = \langle u,w \rangle + \langle v,w \rangle$ for all $u,v,w \in V$.
    \item \textbf{Homogeneity in first slot:} $\langle \lambda u,v \rangle = \lambda \langle u,v \rangle$ for all $\lambda \in \mathbb{F}$ and all $u,v \in V$.
    \item \textbf{Conjugate symmetry:} $\langle u,v \rangle = \overline{\langle v,u \rangle}$ for all $u,v \in V$.
\end{enumerate}
\end{definition}
\begin{definition}[Inner product space]
An inner product space \(V\) is a vector space \(V\) along with an inner product on it. 
\end{definition}
For the rest of this chapter, and the next chapter, \(V\) and \(W\) will be used to denote inner product spaces. 
\begin{theorem}[Basic properties of an inner product]
\quad
\begin{enumerate}[label=(\alph*)]
    \item For each fixed $v \in V$, the function that takes $u \in V$ to $\langle u,v \rangle$ is a linear map from $V$ to $\mathbb{F}$.
    \item $\langle 0, v \rangle = 0$ for every $v \in V$.
    \item $\langle v, 0 \rangle = 0$ for every $v \in V$.
    \item $\langle u, v + w \rangle = \langle u, v \rangle + \langle u, w \rangle$ for all $u, v, w \in V$.
    \item $\langle u, \lambda v \rangle = \overline{\lambda} \langle u, v \rangle$ for all $\lambda \in \mathbb{F}$ and all $u, v \in V$.
\end{enumerate}
\end{theorem}
Proof omitted. 
\section{Norms}
\begin{definition}
For $v \in V$, the \emph{norm} of $v$, denoted by $\|v\|$, is defined by  
\[
\|v\| = \sqrt{\langle v, v \rangle}.
\]
\end{definition}
\begin{theorem}[Basic properties of the norm]
Suppose $v \in V$.  
\begin{enumerate}
    \item $\|v\| = 0$ if and only if $v = 0$.
    \item $\|\lambda v\| = |\lambda| \|v\|$ for all $\lambda \in \mathbb{F}$.
\end{enumerate}
\end{theorem}
Proof omitted. 
\begin{definition}[Orthogonal]
Two vectors \(u, v\) are orthogonal if \[\langle u, v \rangle = 0.\]
\end{definition}
\begin{corollary}
\quad
\begin{enumerate}
    \item $0$ is orthogonal to every vector in $V$.
    \item $0$ is the only vector in $V$ that is orthogonal to itself.
\end{enumerate}
\end{corollary}
\begin{theorem}[Pythagorean theorem]
Suppose \( u, v \in V \). If \( u \) and \( v \) are orthogonal, then
\[
\|u + v\|^2 = \|u\|^2 + \|v\|^2.
\]
\end{theorem}
\begin{proof}
Suppose \(\langle u, v \rangle = 0\). Then
\[
\|u + v\|^2 = \langle u + v, u + v \rangle
= \langle u, u \rangle + \langle u, v \rangle + \langle v, u \rangle + \langle v, v \rangle
= \|u\|^2 + \|v\|^2.
\]
\end{proof}
\begin{theorem}
Suppose \(u, v \in V\), with \(v \neq 0\). Set 
\[
c = \frac{\langle u, v \rangle}{\|v\|^2} 
\quad \text{and} \quad 
w = u - \frac{\langle u, v \rangle}{\|v\|^2} v.
\]
Then
\[
u = c v + w 
\quad \text{and} \quad 
\langle w, v \rangle = 0.
\]
\end{theorem}
Proof by direct calculation. Omitted. 
\begin{theorem}
Suppose $u, v \in V$. Then
\[
\|u + v\| \leq \|u\| + \|v\|.
\]
This inequality is an equality if and only if one of $u, v$ is a nonnegative real multiple of the other.
\end{theorem}
Proof omitted. 
\begin{theorem}[triangle inequality]
Suppose $u, v \in V$. Then
\[
\|u + v\| \leq \|u\| + \|v\|.
\]
This inequality is an equality if and only if one of $u, v$ is a nonnegative real multiple of the other.
\end{theorem}
Proof omitted. 
\begin{theorem}
Suppose $u, v \in V$. Then
\[
\|u + v\|^2 + \|u - v\|^2 = 2(\|u\|^2 + \|v\|^2).
\]
\end{theorem}
Proof by direct calculation. Omitted. 
\section{Orthonormal bases}
\begin{definition}[Orthonormal]
A list of vectors \( e_1, \ldots, e_m \) in a vector space \( V \) is said to be orthonormal if:
\begin{itemize}
  \item Each vector \( e_j \) has norm 1, i.e., \( \|e_j\| = 1 \).
  \item Each pair of distinct vectors is orthogonal, i.e., \( \langle e_j, e_k \rangle = 0 \) for \( j \ne k \).
\end{itemize}
This condition can be expressed compactly as:
\[
\langle e_j, e_k \rangle = 
\begin{cases} 
1 & \text{if } j = k, \\
0 & \text{if } j \ne k 
\end{cases}
\quad \text{for all } j, k \in \{1, \ldots, m\}.
\]
\end{definition}
\begin{theorem}
Suppose \( e_1, \ldots, e_m \) is an orthonormal list of vectors in \( V \). Then
\[
\left\| a_1 e_1 + \cdots + a_m e_m \right\|^2 = |a_1|^2 + \cdots + |a_m|^2
\]
for all \( a_1, \ldots, a_m \in \mathbb{F} \).
\end{theorem}
Proof omitted. 
\begin{corollary}
Every orthonormal list of vectors is linearly independent.
\end{corollary}
\begin{proof}
Suppose \(e_1, ..., e_n\) is an orthonormal list of vectors. Suppose there exists a linear combination 
\[a_1 e_1 + \cdots + a_n e_n = 0.\]
Then we have 
\[
\left\| a_1 e_1 + \cdots + a_n e_n \right\|^2 = |a_1|^2 + \cdots + |a_n|^2 = 0.
\]
Therefore all \(a_i\) must be zero. 
\end{proof}
\begin{theorem}[Bessel's inequality]
Suppose \( e_1, \ldots, e_m \) is an orthonormal list of vectors in \( V \). If \( v \in V \), then
\[
| \langle v, e_1 \rangle |^2 + \cdots + | \langle v, e_m \rangle |^2 \leq \| v \|^2.
\]
\end{theorem}
\begin{proof}
If 
\[\{e_1, ..., e_m\}\]
form a basis of the vector space, then there exists 
\[a_1, a_2, ..., a_m \in \mathbb{F}\]
such that 
\[v = a_1 e_1 + ... + a_m e_m,\]
which means 
\[|\langle v, e_1 \rangle |^2 + \cdots + | \langle v, e_m \rangle |^2 = \| v \|^2.\]
If, on the other hand, there exists \(n > m\) such that 
\[\{e_1, ..., e_n\}\]
form a basis, then there exists
\[a_1, a_2, ..., a_n \in \mathbb{F}\]
such that 
\[v = a_1 e_1 + ... + a_n e_n,\]
and we have 
\[|\langle v, e_1 \rangle |^2 + \cdots + | \langle v, e_m \rangle |^2 = |a_1|^2 + \cdots + |a_m|^2\]
\[\leq |a_1|^2 + \cdots + |a_n|^2 = \| v \|^2.\]
\end{proof}
\begin{definition}[Orthonormal basis]
An orthonormal basis of \(V\) is an orthonormal list of vectors in \(V\) that is also a basis of \(V\). 
\end{definition}
\begin{corollary}
Suppose \( e_1, \ldots, e_n \) is an orthonormal basis of \( V \) and \( u, v \in V \). Then
\begin{itemize}
  \item[(a)] \( v = \langle v, e_1 \rangle e_1 + \cdots + \langle v, e_n \rangle e_n \);
  \item[(b)] \( \|v\|^2 = |\langle v, e_1 \rangle|^2 + \cdots + |\langle v, e_n \rangle|^2 \);
  \item[(c)] \( \langle u, v \rangle = \langle u, e_1 \rangle \overline{\langle v, e_1 \rangle} + \cdots + \langle u, e_n \rangle \overline{\langle v, e_n \rangle} \).
\end{itemize}
\end{corollary}
Proof omitted. 
\begin{theorem}
The inner product of two vectors does not depend on the choice of the orthonormal basis. 
\end{theorem}
\begin{proof}
Suppose \(\mathcal{F} = \{f_1, ..., f_n\}\) is an orthonormal basis, and \(v = x_1 f_1 + ... x_n f_n\), \(u = y_1 f_1 + ... + y_n f_n\). If \(\mathcal{E} = \{e_1, ..., e_n\}\) is another orthonormal basis, then there exists \((a_{i, j})_{i = 1, 2, ..., n}^{j = 1, 2, ..., n}\), such that 
\[f_i = a_{1, i} e_1 + ... + a_{n, i} e_n\]
for each \(i\), and we have relations 
\[|a_{1, i}|^2 + ... + |a_{n, i}|^2 = 1\]
for all \(i\), and 
\[0 = \langle f_i, f_j \rangle = a_{1, i} \overline{a_{1, j}} + ... + a_{n, i} \overline{a_{n, j}}\]
for any pair of distinct \(i, j\). 

Then we can write \(v\) and \(u\) into linear combinations of \(\mathcal{E}\), and the rest follows from simple calculation. Omitted. 
\end{proof}
\section{Gram-Schmidt orthogonalization}
\begin{definition}[Gram-Schmidt procedure]
Suppose \( v_1, \ldots, v_m \) is a linearly independent list of vectors in \( V \). Let \( f_1 = v_1 \). For \( k = 2, \ldots, m \), define \( f_k \) inductively by
\[
f_k = v_k - \frac{\langle v_k, f_1 \rangle}{\|f_1\|^2} f_1 - \cdots - \frac{\langle v_k, f_{k-1} \rangle}{\|f_{k-1}\|^2} f_{k-1}.
\]
For each \( k = 1, \ldots, m \), let \( e_k = \frac{f_k}{\|f_k\|} \). Then \( e_1, \ldots, e_m \) is an orthonormal list of vectors in \( V \) such that
\[
\text{span}(v_1, \ldots, v_k) = \text{span}(e_1, \ldots, e_k)
\]
for each \( k = 1, \ldots, m \). 
\end{definition}
\begin{remark}
We can show that each \(f_i, f_j\) are orthogonal for different \(i, j\), and after dividing by their norm they are all normal. The argument that those orthonormal vectors are all in the span of vectors \(v_1, ..., v_m\) is trivial. 
\end{remark}
\begin{corollary}
Every finite-dimensional inner product space has an orthonormal basis. 
\end{corollary}
Proof omitted. 
\begin{corollary}
Suppose \(V\) is finite-dimensional. Then every orthonormal list of vectors in \(V\) can be extended to an orthonormal basis of \(V\). 
\end{corollary}
\begin{theorem}
Suppose \( V \) is finite-dimensional and \( T \in \mathcal{L}(V) \). Then \( T \) has an upper-triangular matrix with respect to some orthonormal basis of \( V \) if and only if the minimal polynomial of \( T \) equals
\[
(z - \lambda_1)\cdots(z - \lambda_m)
\]
for some \( \lambda_1, \ldots, \lambda_m \in \mathbb{F} \).
\end{theorem}
\begin{proof}
Suppose \(\mathcal{E} = \{e_1, ..., e_n\}\) is an orthonormal basis of \(V\), and \([T]_{\mathcal{EE}}\) is upper-triangular. Then let \(\lambda_1, ..., \lambda_n\) be the diagonal of the matrix, we have 
\[(T - \lambda_1 I) (T - \lambda_2 I) ... (T - \lambda_n I) = 0,\]
which means it is a polynomial multiple of the minimal polynomial, and this implies, after re-labeling, the minimal polynomial is in the form 
\[
(z - \lambda_1)\cdots(z - \lambda_m)
\]
for some \( \lambda_1, \ldots, \lambda_m \in \mathbb{F} \).

Suppose the minimal polynomial of \(T\) is in the form 
\[
(z - \lambda_1)\cdots(z - \lambda_m)
\]
for some \( \lambda_1, \ldots, \lambda_m \in \mathbb{F} \). Then there exists a basis \(\mathcal{B}\) for \(V\) such that the matrix of \(T\) with respect to which is upper-triangular. Therefore, denote 
\[\mathcal{B} = \{v_1, ..., v_n\},\]
and we have 
\[T v_1 = a_{1, 1} v_1 \in \operatorname{span}\{v_1\};\]
\[T v_2 = a_{1, 2} v_1 + a_{2, 2} v_2 \in \operatorname{span}\{v_1, v_2\};\]
\[\vdots\]
\[T v_{n-1} = a_{1,n-1} v_1 + a_{2, n-1} v_2 + ... + a_{n-1, n-1} v_{n-1} \in \operatorname{span}\{v_1, ..., v_{n-1}\};\]
\[T v_n = a_{1, n} v_1 + a_{2, n} v_n + ... + a_{n, n} v_n \in \operatorname{span}\{v_1, ..., v_n\}.\]
Therefore, there exists \(b_{i, j} \in \mathbb{F}\), such that 
\[T v_1 = b_{1, 1} e_1 \in \operatorname{span}\{e_1\} = \operatorname{span}\{v_1\};\]
\[T v_2 = b_{1, 2} e_1 + b_{2, 2} e_2 \in \operatorname{span}\{e_1, e_2\} =\operatorname{span}\{v_1, v_2\};\]
\[\vdots\]
\[T v_{n-1} = b_{1,n-1} e_1 + b_{2, n-1} e_2 + ... + b_{n-1, n-1} e_{n-1} \in \operatorname{span}\{e_1, ..., e_{n-1}\} = \operatorname{span}\{v_1, ..., v_{n-1}\};\]
\[T v_n = b_{1, n} e_1 + b_{2, n} e_n + ... + b_{n, n} e_n \in \operatorname{span}\{e_1, ..., e_n\} =\operatorname{span}\{v_1, ..., v_n\}.\]
\end{proof}
\begin{theorem}[Schur's theorem]
Every operator on a finite-dimensional complex inner product space has an upper-triangular matrix with respect to some orthonormal basis. 
\end{theorem}
\begin{proof}
Every operator on a complex finite-dimensional inner product space has a minimal polynomial in the form 
\[
(z - \lambda_1)\cdots(z - \lambda_m).
\]
Therefore by our previous theorem, it has an upper-triangular matrix with respect to some orthonormal basis.
\end{proof}
\section{Linear functionals on inner product spaces}
\begin{definition}
\begin{itemize}
    \item A \textit{linear functional} on $V$ is a linear map from $V$ to $F$.
    \item The \textit{dual space} of $V$, denoted by $V'$, is the vector space of all linear functionals on $V$. In other words, $V' = \mathcal{L}(V, F)$.
\end{itemize}
\end{definition}
\begin{theorem}
Suppose \( V \) is finite-dimensional and \( \varphi \) is a linear functional on \( V \). Then there is a unique vector \( u \in V \) such that
\[
\varphi(v) = \langle v, u \rangle
\]
for every \( v \in V \).
\end{theorem}
\begin{proof}
Suppose \(n = \dim V\) and 
\[\{e_1, ..., e_n\}\]
and is an orthonormal basis for \(V\). Then there exists an unique \[[v_1, ..., v_n]^T \in \mathbb{F}^n\] such that \[v = e_1 v_1 + ... + e_n v_n.\] Since \(\varphi\) is a linear functional, there exists a unique \[[x_1, ..., x_n]^T \in \mathbb{F}^n,\] such that \(\varphi (e_i) = x_i\) for all \(i = 1, 2, ..., n\). Therefore, if we denote \[u = \overline{x_1} e_1 + ... + \overline{x_n} e_n,\] we will have \(\varphi (v) = \langle v, u \rangle\). 
\end{proof}
\begin{remark}
Another proof is by showing that (\textcolor{red}{with \(v\) and \(u\) exchanged})
\[
\begin{aligned}
\varphi(u) &= \varphi\big( \langle u, e_{1} \rangle e_{1} + \cdots + \langle u, e_{n} \rangle e_{n} \big) \\
&= \langle u, e_{1} \rangle \varphi(e_{1}) + \cdots + \langle u, e_{n} \rangle \varphi(e_{n}) \\
&= \left\langle u, \overline{\varphi(e_{1})} e_{1} + \cdots + \overline{\varphi(e_{n})} e_{n} \right\rangle
\end{aligned}
\]
and by setting
\[v = \overline{\varphi (e_1)} e_1 + ... + \overline{\varphi(e_n)} e_n,\]
we have \(\varphi (u) = \langle u, v \rangle\) for every \(u \in V\) as desired. Then uniqueness of such \(v\) is omitted. 
\end{remark}
\section{Orthogonal complements}
\begin{definition}[Orthogonal complement, \(U^{\perp}\)]
If \( U \) is a subset of \( V \), then the \textit{orthogonal complement} of \( U \), denoted by \( U^\perp \), is the set of all vectors in \( V \) that are orthogonal to every vector in \( U \):
\[
U^\perp = \{ v \in V : \langle u, v \rangle = 0 \text{ for every } u \in U \}.
\]
\end{definition}
\begin{corollary}
\begin{enumerate}
    \item If \( U \) is a subset of \( V \), then \( U^\perp \) is a subspace of \( V \).
    \item \( \{0\}^\perp = V \).
    \item \( V^\perp = \{0\} \).
    \item If \( U \) is a subset of \( V \), then \( U \cap U^\perp \subseteq \{0\} \).
    \item If \( G \) and \( H \) are subsets of \( V \) and \( G \subseteq H \), then \( H^\perp \subseteq G^\perp \).
\end{enumerate}
\end{corollary}
\begin{proof}
\((a), (b), (c), (d)\) are omitted. For \((e)\), \(G \subseteq H\) such that there exists orthonormal bases \(\mathcal{A, B}\) for \(G\) and \(H\), respectively, such that \(\mathcal{A} \subset \mathcal{B}\). We extend \(\mathcal{B}\) into \(\mathcal{D}\), an orthonormal basis for \(V\), then \(H^{\perp} = \operatorname{span} (\mathcal{D - B}) \subseteq \operatorname{span} (\mathcal{D - A}) = G^{\perp}\). 

For \(V\) with infinite dimensions, we prove in the following way: \(\forall x \in H^{\perp}\), for any \(h \in H\), we have \(\langle x, h \rangle = 0\), therefore \(\langle x, g \rangle = 0\) for all \(g \in G\), which means \(x \in G^{\perp}\). Therefore \(H^{\perp} \subseteq G^{\perp}\). 
\end{proof}
\begin{theorem}
Suppose \(U\) is a finite-dimensional subspace of \(V\). Then \[V = U \oplus U^{\perp}.\]
\end{theorem}
Proof omitted. 
\begin{theorem}
Suppose \(V\) is finite-dimensional and \(U\) is a subspace of \(V\), then \[\dim U^{\perp} = \dim V - \dim U.\]
\end{theorem}
Proof omitted. 
\begin{theorem}
Suppose \(U\) is a finite-dimensional subspace of \(V\). Then \[U = (U^{\perp})^{\perp}.\]
\end{theorem}
Proof omitted. 
\begin{theorem}
Suppose \(U\) is a finite-dimensional subspace of \(V\), then \[U^{\perp} = \{0\} \Longleftrightarrow U = V.\]
\end{theorem}
Proof omitted. 
\begin{definition}[Orthogonal projection]
Suppose $U$ is a finite-dimensional subspace of $V$. The \textit{orthogonal projection}
of $V$ onto $U$ is the operator $P_U \in \mathcal{L}(V)$ defined as follows:  
For each $v \in V$, write $v = u + w$, where $u \in U$ and $w \in U^\perp$.  
Then let $P_U v = u$.
\end{definition}
\begin{corollary}
Suppose $U$ is a finite-dimensional subspace of $V$. Then  
\begin{itemize}
    \item $P_U \in \mathcal{L}(V)$;
    \item $P_U u = u$ for every $u \in U$;
    \item $P_U w = 0$ for every $w \in U^\perp$;
    \item $\operatorname{range} P_U = U$;
    \item $\operatorname{null} P_U = U^\perp$;
    \item $v - P_U v \in U^\perp$ for every $v \in V$;
    \item $P_U^2 = P_U$;
    \item $\|P_U v\| \le \|v\|$ for every $v \in V$;
    \item if $e_1, \dots, e_m$ is an orthonormal basis of $U$ and $v \in V$, then  
    \[
    P_U v = \langle v, e_1 \rangle e_1 + \cdots + \langle v, e_m \rangle e_m.
    \]
\end{itemize}
\end{corollary}
Proof omitted. 
\begin{theorem}[Riesz representation theorem, revisited]
Suppose $V$ is finite-dimensional. For each $v \in V$, define $\varphi_v \in V'$ by
\[
\varphi_v(u) = \langle u, v \rangle
\]
for each $u \in V$. Then $v \mapsto \varphi_v$ is a one-to-one function from $V$ onto $V'$.
\end{theorem}
\begin{remark}
\textcolor{red}{\textit{Caution:} The function \( v \mapsto \varphi_v \) is a linear mapping from \( V \) to \( V' \) if \( \mathbf{F} = \mathbb{R} \). However, this function is not linear if \( \mathbf{F} = \mathbb{C} \) because \(\varphi_{\lambda v} = \overline{\lambda} \, \varphi_v\) if \(\lambda \in \mathbb{C}\).}
\end{remark}
\begin{proof}
To show that \( v \mapsto \varphi_v \) is surjective, suppose \( \varphi \in V' \).  If \( \varphi = 0 \), then \( \varphi = \varphi_0 \).  

Thus assume \( \varphi \neq 0 \). Hence \(\mathrm{null} \, \varphi \neq V\),  which implies that \((\mathrm{null} \, \varphi)^\perp \neq \{ 0 \}\). Let \( w \in (\mathrm{null} \, \varphi)^\perp \) be such that \( w \neq 0 \).

Let  
\[
v = \frac{\overline{\varphi(w)}}{\|w\|^2} \, w.
\]
Then \( v \in (\mathrm{null} \, \varphi)^\perp \).

Also, \( v \neq 0 \) (because \( w \notin \mathrm{null} \, \varphi \)).

Taking the norm of both sides,
\[
\|v\| = \frac{|\varphi(w)|}{\|w\|}.
\]
Applying \(\varphi\) to both sides, and use the previous equation, we have 
\[\varphi (v) = \frac{|\varphi (w)|^2}{\|w\|^2} = \|v\|^2.\]
Now suppose \( u \in V \). Using the equation above, we have
\[
u = \left( u - \frac{\varphi(u)}{\varphi(v)} v \right) 
    + \frac{\varphi(u)}{\|v\|^2} v.
\]
The first term in parentheses above is in \(\mathrm{null} \, \varphi\) and hence is orthogonal to \(v\). Thus taking the inner product of both sides of the equation above with \(v\) shows that
\[
\langle u, v \rangle 
= \frac{\varphi(u)}{\|v\|^2} \langle v, v \rangle 
= \varphi(u).
\]
Thus \(\varphi = \varphi_v\), showing that \( v \mapsto \varphi_v \) is surjective, as desired.
\end{proof}
\section{Minimization problems}
\begin{theorem}[minimizing distance to a subspace]
Suppose \( U \) is a finite-dimensional subspace of \( V \), \( v \in V \), and \( u \in U \). Then
\[
\| v - P_U v \| \leq \| v - u \|.
\]
Furthermore, the inequality above is an equality if and only if \( u = P_U v \).
\end{theorem}
\begin{proof}
\[
\|v - P_U v\|^2 \leq \|v - P_U v\|^2 + \|P_U v - u\|^2
\]
\[
= \|(v - P_U v) + (P_U v - u)\|^2
\]
where \(v - P_U v \in U^{\perp}\) and \(P_U v - u \in U\), so we have this equals to 
\[
\|v - u\|^2.
\]
\end{proof}
\section{Pseudoinverse}
Suppose \( T \in \mathcal{L}(V, W) \) and \( w \in W \). Consider the problem of finding \( v \in V \) such that
\[
Tv = w.
\]
If \( T \) is invertible, then the unique solution to the equation above is \( v = T^{-1} w \). However, if \( T \) is not invertible, then for some \( w \in W \) there may not exist any solutions of the equation above, and for some \( w \in W \) there may exist infinitely many solutions of the equation above.

If \( T \) is not invertible, then we can still try to do as well as possible with the equation above. For example, if the equation above has no solutions, then instead of solving the equation \( Tv - w = 0 \), we can try to find \( v \in V \) such that \( \|Tv - w\| \) is as small as possible. As another example, if the equation above has infinitely many solutions \( v \in V \), then among all those solutions we can try to find one such that \( \|v\| \) is as small as possible.
\begin{theorem}
Suppose $V$ is finite-dimensional and $T \in \mathcal{L}(V,W)$. Then $T|_{(\text{null}\,T)^\perp}$ is an injective map of $(\text{null}\,T)^\perp$ onto $\text{range}\,T$.
\end{theorem}
\begin{remark}
Note that "onto" means the map is surjective. 
\end{remark}
\begin{proof}
Suppose that $v \in (\text{null}\,T)^\perp$ and $T|_{(\text{null}\,T)^\perp} v = 0$.

Hence $Tv = 0$ and thus $v \in (\text{null}\,T) \cap (\text{null}\,T)^\perp$, which implies that $v = 0$. Hence $\text{null}\,T|_{(\text{null}\,T)^\perp} = \{0\}$, which implies that $T|_{(\text{null}\,T)^\perp}$ is injective, as desired.

Clearly $\text{range}\,T|_{(\text{null}\,T)^\perp} \subseteq \text{range}\,T$. 

To prove the inclusion in the other direction, suppose $w \in \text{range}\,T$.

Hence there exists $v \in V$ such that $w = Tv$. There exist $u \in \text{null}\,T$ and $x \in (\text{null}\,T)^\perp$ such that $v = u + x$. Now
\[
T|_{(\text{null}\,T)^\perp} x = Tx = Tv - Tu = w - 0 = w,
\]
which shows that $w \in \text{range}\,T|_{(\text{null}\,T)^\perp}$. Hence $\text{range}\,T \subseteq \text{range}\,T|_{(\text{null}\,T)^\perp}$, completing the proof that \[\text{range}\,T|_{(\text{null}\,T)^\perp} = \text{range}\,T.\]
\end{proof}
Now we can define the pseudoinverse \( T^{\dagger} \) (pronounced “\( T \) dagger”) of a linear map \( T \). In the next definition (and from now on), think of \( T_{\mid (\operatorname{null} T)^{\perp}} \) as an invertible linear map from \( (\operatorname{null} T)^{\perp} \) onto \( \operatorname{range} T \), as is justified by the result above. 
\begin{definition}[pseudoinverse \( T^{\dagger}\)]
Suppose that \( V \) is finite-dimensional and \( T \in \mathcal{L}(V, W) \). The \emph{pseudoinverse} \( T^{\dagger} \in \mathcal{L}(W, V) \) of \( T \) is the linear map from \( W \) to \( V \) defined by  
\[
T^{\dagger} w = \left( T_{\mid (\operatorname{null} T)^{\perp}} \right)^{-1} P_{\operatorname{range} T} w
\]
for each \( w \in W \).
\end{definition}
\begin{remark}
Intuitively this makes a lot of sense, because we need to project \(w \in W\) onto \(\operatorname{range} T\) before proceeding with the inverse of the isomorphic map defined above. 
\end{remark}
\begin{corollary}[algebraic properties of the pseudoinverse]
Suppose \( V \) is finite-dimensional and \( T \in \mathcal{L}(V, W) \).
\begin{itemize}
    \item[(a)] If \( T \) is invertible, then \( T^{\dagger} = T^{-1} \).
    \item[(b)] \( TT^{\dagger} = P_{\mathrm{range} \, T} \) = the orthogonal projection of \( W \) onto \(\mathrm{range} \, T\).
    \item[(c)] \( T^{\dagger} T = P_{(\mathrm{null} \, T)^{\perp}} \) = the orthogonal projection of \( V \) onto \((\mathrm{null} \, T)^{\perp}\).
\end{itemize}
\end{corollary}
\begin{proof}
Proof of \((a)\) is omitted. As for \((b)\), pick any \(w \in W\), then there exists unique \(w_x\) and \(w_y\) in \(\operatorname{range} T\) and \((\operatorname{range} T)^{\perp}\), such that \(w = w_x + w_y\). Then 
\[T T^\dagger w = T \left( T_{\mid (\operatorname{null} T)^{\perp}} \right)^{-1} P_{\operatorname{range} T} w = T \left( T_{\mid (\operatorname{null} T)^{\perp}} \right)^{-1} w_x.\]
Since \(\left( T_{\mid (\operatorname{null} T)^{\perp}} \right)^{-1}\) is invertible, there exists a unique \(v \in (\ker T)^\perp\), such that \(\left( T_{\mid (\operatorname{null} T)^{\perp}} \right) v = w_x\). Thus we have \(\left( T_{\mid (\operatorname{null} T)^{\perp}} \right)^{-1} w_x = v\), and \[T v = T_{\mid (\operatorname{null} T)^{\perp}} v = w_x = P_{\operatorname{range} T} w.\]
For the proof of \((c)\), for all \(v \in V\), there exists unique \(v_x, v_y\) in \(\ker T\) and \((\ker T)^\perp\), respectively, such that \(v = v_x + v_y\). Then \(T v = T (v_x + v_y) = T v_y\). Since \(T v_y \in \operatorname{range} T\), \(P_{\operatorname{range} T} T v_y = T v_y\). Since 
\[\left( T_{\mid (\operatorname{null} T)^{\perp}} \right)^{-1}: \operatorname{range} T \to T|_{(\ker T)^\perp}\]
is an isomorphism, for any \(w \in \operatorname{range} T\), there exists an unique \(v_0 \in (\ker T)^\perp\), such that \(T v_0 = w\). Since \(T v_y \in \operatorname{range} T\) and \(v_y \in (\ker T)^\perp\), \( T^{\dagger} T v = v_y\) is the projection of \(v\) onto \((\ker T)^\perp\). 
\end{proof}
\begin{theorem}[pseudoinverse provides best approximate solution or best solution]
Suppose $V$ is finite-dimensional, $T \in \mathcal{L}(V, W)$, and $w \in W$.
\begin{enumerate}[label=(\alph*)]
    \item If $v \in V$, then
    \[
        \| T(T^{\dagger} w) - w \| \le \| T v - w \|,
    \]
    with equality if and only if $v \in T^{\dagger} w + \mathrm{null}\,T$.
    \item If $v \in T^{\dagger} w + \mathrm{null}\,T$, then
    \[
        \| T^{\dagger} w \| \le \| v \|,
    \]
    with equality if and only if $v = T^{\dagger} w$.
\end{enumerate}
\end{theorem}
\begin{proof}
As we have shown, \(T T^\dagger w\) is the projection of \(w\) onto \(\operatorname{range} T\), then the first inequality follows from a previous theorem. Furthermore, the inequality becomes equality if and only if \(T v =  T(T^{\dagger} w)\), which means \(v -  T^{\dagger} w \in \ker T\), which is equivalent to $v \in T^{\dagger} w + \mathrm{null}\,T$. 

We have
\[
W \xrightarrow{P_{\operatorname{range} T}} \operatorname{range} T \subseteq W \xrightarrow{(T|_{(\ker T)^\perp})^{-1}} (\ker T)^\perp \subseteq V
\]
which means \(T^\dagger w \in (\ker T)^\perp\), and since \(v \in T^{\dagger} w + \ker T\), there exists unique \(v_y \in \ker T\), such that \(v = T^{\dagger} w + v_y\), and \(v_y \perp T^{\dagger} w\). Therefore, \(\|v\|^2 = \|v_y\|^2 + \|T^{\dagger} w\|^2\), and we get the second inequality, with equality if and only if \(v_y = 0 \Longleftrightarrow v = T^{\dagger} w\). 
\end{proof}
\section{Adjoints}
\begin{definition}[adjoint]
Suppose \( T \in \mathcal{L}(V, W) \). The \emph{adjoint} of \( T \) is the function \( T^* : W \to V \) such that  
\[
\langle Tv, w \rangle = \langle v, T^* w \rangle
\]
for every \( v \in V \) and every \( w \in W \). 
\end{definition}
\begin{remark}
Now, why does this definition makes sense? Note that for orthonormal bases \(\mathcal{B} = \{v_1, ..., v_n\}\) and \(\mathcal{A} = \{w_1, ..., w_m\}\) of \(V\) and \(W\) respectively, \(T\) is defined by which linear combinations of \(w_1, ..., w_m\) it maps \(v_1, ..., v_n\) to. 

Suppose 
\[T v_i = a_{1, i} w_1 + a_{2, i} w_2 + ... + a_{m, i} w_m\]
for all \(i = 1, 2, ..., n\), Then \(\langle Tv_i, w_j\rangle = a_{j, i}\) for all \(i, j\), then we know that \(\langle v_i, T^* w_j \rangle = a_{j, i}\) for all \(i, j\), which means \(T^*\) is defined by 
\[T^* w_j = \overline{a_{j, 1}} v_1 + \overline{a_{j, 2}} v_2 + ... + \overline{a_{j, n}} v_n\]
for all \(j = 1, 2, ..., m\). 
\end{remark}
\begin{remark}
To see why the definition above makes sense, suppose \( T \in \mathcal{L}(V, W) \). Fix \( w \in W \). Consider the linear functional  
\[
v \mapsto \langle Tv, w \rangle
\]
on \( V \) that maps \( v \in V \) to \( \langle Tv, w \rangle \); this linear functional depends on \( T \) and \( w \).  

By the Riesz representation theorem, there exists a unique vector in \( V \) such that this linear functional is given by taking the inner product with it.  

We call this unique vector \( T^* w \). In other words, \( T^* w \) is the unique vector in \( V \) such that  
\[
\langle Tv, w \rangle = \langle v, T^* w \rangle
\]
for every \( v \in V \).
\end{remark}
\begin{corollary}
Adjoint of a linear map is also a linear map. 
\end{corollary}
\begin{proof}
Suppose \( T \in \mathcal{L}(V, W) \). If \( v \in V \) and \( w_1, w_2 \in W \), then  
\[
\langle Tv, w_1 + w_2 \rangle 
    = \langle Tv, w_1 \rangle + \langle Tv, w_2 \rangle
    = \langle v, T^* w_1 \rangle + \langle v, T^* w_2 \rangle
    = \langle v, T^* w_1 + T^* w_2 \rangle.
\]
The equation above shows that  
\[
T^*(w_1 + w_2) = T^* w_1 + T^* w_2.
\]  
If \( v \in V \), \( \lambda \in \mathbf{F} \), and \( w \in W \), then  
\[
\langle Tv, \lambda w \rangle 
    = \overline{\lambda} \langle Tv, w \rangle
    = \overline{\lambda} \langle v, T^* w \rangle
    = \langle v, \lambda T^* w \rangle.
\]
The equation above shows that  
\[
T^*(\lambda w) = \lambda T^* w.
\]
Thus \( T^* \) is a linear map, as desired.
\end{proof}
\begin{corollary}[properties of the adjoint]
Suppose \( T \in \mathcal{L}(V, W) \). Then
\begin{itemize}
    \item[(a)] \( (S + T)^* = S^* + T^* \) for all \( S \in \mathcal{L}(V, W) \);
    \item[(b)] \( (\lambda T)^* = \overline{\lambda} \, T^* \) for all \( \lambda \in \mathbb{F} \);
    \item[(c)] \( (T^*)^* = T \);
    \item[(d)] \( (ST)^* = T^* S^* \) for all \( S \in \mathcal{L}(W, U) \) (here \( U \) is a finite-dimensional inner product space over \( \mathbb{F} \));
    \item[(e)] \( I^* = I \), where \( I \) is the identity operator on \( V \);
    \item[(f)] If \( T \) is invertible, then \( T^* \) is invertible and \( (T^*)^{-1} = (T^{-1})^* \).
\end{itemize}
\end{corollary}
Proof omitted. 
\begin{theorem}[null space and range of $T^*$]
Suppose $T \in \mathcal{L}(V, W)$. Then
\begin{enumerate}[label=(\alph*)]
    \item $\mathrm{null}\,T^* = (\mathrm{range}\,T)^{\perp}$;
    \item $\mathrm{range}\,T^* = (\mathrm{null}\,T)^{\perp}$;
    \item $\mathrm{null}\,T = (\mathrm{range}\,T^*)^{\perp}$;
    \item $\mathrm{range}\,T = (\mathrm{null}\,T^*)^{\perp}$.
\end{enumerate}
\end{theorem}
\begin{proof}
The first statement: 

Suppose \(w \in \ker T^*\), then \(\forall v \in V\), \(\langle Tv, w \rangle = \langle v, T^* w \rangle = 0\). Therefore, for any \(y \in \operatorname{range} T\), \(\langle y, w, \rangle = 0\). Therefore, \(w \perp \operatorname{range} T\), which implies \(w \in (\operatorname{range} T)^\perp\), and \(\ker T^* \subseteq (\operatorname{range} T)^\perp\). 

Suppose \(w \in (\operatorname{range}T)^\perp\), then for any \(y \in \operatorname{range} T\), \(\langle y, w\rangle = 0\), which means for any \(x \in V\), \(\langle Tx, w \rangle = 0\) \(\Longrightarrow \forall x \in V\), \(\langle x, T^* w \rangle = 0\). Let \(x = T^* w\), then we get \(\|T^* w\|= 0\) \(\Longrightarrow w \in \ker T^*\) \(\Longrightarrow (\operatorname{range} T)^\perp \subseteq \ker T^*\). 

\textcolor{red}{We take the orthogonal complement of both sides, and get the last statement. }

\textcolor{red}{Replace \(T\) and \(T^*\), we get the third statement; and replacing \(T\) and \(T^*\) of the last statement we will get the second statement. }
\end{proof}
\begin{definition}[conjugate transpose]
The \textit{conjugate transpose} of an $m$-by-$n$ matrix $A$ is the $n$-by-$m$ matrix $A^*$ 
obtained by interchanging the rows and columns and then taking the complex conjugate of each entry. 
In other words, if $j \in \{1, \ldots, n\}$ and $k \in \{1, \ldots, m\}$, then
\[
(A^*)_{j,k} = \overline{A_{k,j}}.
\]
\end{definition}
\begin{theorem}
Let $T \in \mathcal{L}(V, W)$. Suppose $e_1, \ldots, e_n$ is an orthonormal basis of $V$ 
and $f_1, \ldots, f_m$ is an orthonormal basis of $W$. Then 
\[
\mathcal{M}(T^*, (f_1, \ldots, f_m), (e_1, \ldots, e_n))
\]
is the conjugate transpose of 
\[
\mathcal{M}(T, (e_1, \ldots, e_n), (f_1, \ldots, f_m)).
\]
In other words,
\[
\mathcal{M}(T^*) = \left( \mathcal{M}(T) \right)^*.
\]
\end{theorem}
We have already prove this in one of our previous remarks. So proof omitted. 
\section{Self-adjoint operators}
\begin{definition}[self-adjoint]
An operator \(T \in \mathcal{L}(V)\) is self-adjoint if \(T = T^*\). 
\end{definition}
\begin{corollary}
By our previous discussions, if \(\mathcal{E}\) is an orthonormal basis for \(V\), then \(T\) is self-adjoint if and only if
\[[T^*]_{\mathcal{EE}} = [T]_{\mathcal{EE}}.\]
\end{corollary}
\begin{theorem}
Every eigenvalue of a self-adjoint operator is real.
\end{theorem}
\begin{proof}
Suppose \(T\) is self-adjoint ans \(\lambda\) is one of its eigenvalues. Then there exists a nonzero vector \(v \in V\), such that \(T v = \lambda v\). Therefore 
\[\langle Tv, v \rangle = \langle \lambda v, v \rangle = \lambda \langle v, v \rangle,\]
and 
\[\langle Tv, v \rangle = \langle v, T^* v \rangle = \langle v, Tv \rangle = \langle v, \lambda v \rangle = \overline{\lambda} \langle v, v \rangle,\]
therefore \(\lambda = \overline{\lambda}\), which means \(\lambda\) is a real number. 
\end{proof}
\begin{theorem}[$Tv$ is orthogonal to $v$ for all $v \;\;\Longleftrightarrow\;\; T = 0$ (assuming $\mathbb{F} = \mathbb{C}$)]
Suppose $V$ is a complex inner product space and $T \in \mathcal{L}(V)$. Then
\[
\langle Tv, v \rangle = 0 \quad \text{for every } v \in V 
\;\;\Longleftrightarrow\;\; T = 0.
\]
\end{theorem}
\begin{proof}
If \(\mathbb{F} = \mathbb{C}\), then \(T\) has at least one eigenvalue, and nonzero eigenvectors. The rest is omitted. 
\end{proof}
\begin{remark}
Another proof from the book:

If $u, w \in V$, then
\[
\langle Tu, w \rangle 
= \frac{\langle T(u+w), u+w \rangle - \langle T(u-w), u-w \rangle}{4} \]
\[+ \frac{\langle T(u+iw), u+iw \rangle - \langle T(u-iw), u-iw \rangle}{4} i,
\]
as can be verified by computing the right side. Note that each term on the right
side is of the form $\langle Tv, v \rangle$ for appropriate $v \in V$.

Now suppose $\langle Tv, v \rangle = 0$ for every $v \in V$. Then the equation above implies that $\langle Tu, w \rangle = 0$ for all $u, w \in V$, which then implies that $Tu = 0$ for every $u \in V$ (take $w = Tu$). Hence $T = 0$, as desired.
\end{remark}
\begin{theorem}[\(\langle Tv, v \rangle \text{ is real for all } v \;\;\Longleftrightarrow\;\; T \text{ is self-adjoint } \; (\text{assuming } \mathbf{F} = \mathbb{C})\)]
Suppose $V$ is a complex inner product space and $T \in \mathcal{L}(V)$. Then  
\[
T \text{ is self-adjoint } \;\;\Longleftrightarrow\;\; 
\langle Tv, v \rangle \in \mathbf{R} \;\; \text{for every } v \in V.
\]
\end{theorem}
\begin{proof}
Same as above, if \(\mathbb{F} = \mathbb{C}\) then \(T\) has at least one eigenvalue. The rest is omitted. 

Another proof from the book is as follows:

We know that \(\langle Tv, v \rangle = \overline{\langle v, Tv \rangle}\). If \(\langle Tv, v \rangle \in \mathbb{R}\) for all \(v \in V\), we will have \(\langle Tv, v \rangle = \langle v, Tv \rangle\). Since \(\langle Tv, v \rangle = \langle v, T^* v \rangle\), we get \(\langle v, (T^* - T) v \rangle = 0\) for all \(v \in V\), for which, according to the previous theorem, we have \(T^* = T\), which means \(T\) is self-adjoint. 

On the other hand, if \(T\) is self-adjoint, \(\langle Tv, v \rangle = \langle v, T^* v \rangle = \langle v, Tv \rangle\), and \(\langle Tv, v \rangle = \overline{\langle v, Tv \rangle}\). Therefore \(\langle v, Tv \rangle\) is real for all \(v \in V\), which implies \(\langle Tv, v \rangle = \langle v, Tv \rangle\) is real for all \(v \in V\). 
\end{proof}
\begin{theorem}
In real inner product spaces, suppose \(T\) is self-adjoint. Then we have
\[T = 0 \Longleftrightarrow \langle Tv, v \rangle = 0 \text{ for all } v \in V.\]
\end{theorem}
\begin{proof}
We know that
\[
\langle Tu, w \rangle 
= \frac{\langle T(u+w),\,u+w \rangle - \langle T(u-w),\,u-w \rangle}{4},
\]
computed by calculating the right hand side, and now we know that if \(\langle Tv, v \rangle = 0\) for all \(v \in V\), then \(\langle T u, w \rangle = 0\) for all \(u, w \in V\), which, by setting \(w = T v\), we reach the conclusion that \(T = 0\). 
\end{proof}
\begin{remark}
If \(p(T)\) is a polynomial of a self-adjoint linear operator \(T\) with real coefficients, then \(p(T)\) is also self-adjoint. Proof omitted. 
\end{remark}
\section{Normal operators}
\begin{definition}[normal operator]
\quad
\begin{itemize}
    \item An operator on an inner product space is called \textit{normal} if it commutes with its adjoint.
    \item In other words, $T \in \mathcal{L}(V)$ is normal if $TT^* = T^*T$.
\end{itemize}
\end{definition}
\begin{remark}
Therefore, each self-adjoint operator is normal. 
\end{remark}
\begin{theorem}
Suppose $T \in \mathcal{L}(V)$. Then
\[
T \text{ is normal} \;\;\Longleftrightarrow\;\; \|Tv\| = \|T^*v\| \quad \text{for every } v \in V.
\]
\end{theorem}
\begin{proof}
Suppose \(\|Tv\| = \|T^* v\|\), then \(\langle Tv, Tv \rangle = \langle T^*v, T^* v \rangle\) \(\Longrightarrow \langle v, T^* T v \rangle = \langle v, T T^* v \rangle\) \(\Longrightarrow\) \(T^* T = TT^*\), therefore \(T\) is normal. 

Suppose \(T\) is normal, then \(T^* T = TT^*\), which means \(\langle v, T^* T v \rangle = \langle v, TT^* v \rangle\) for all \(v \in V\), which implies \(\langle Tv, Tv \rangle = \langle T^* v, T^* v \rangle\) \(\Longrightarrow \|Tv \| = \|T^* v \|\). 
\end{proof}
\begin{theorem}
Suppose $T \in \mathcal{L}(V)$ is normal. Then  
\begin{enumerate}
    \item $\operatorname{null} T = \operatorname{null} T^*$;
    \item $\operatorname{range} T = \operatorname{range} T^*$;
    \item $V = \operatorname{null} T \oplus \operatorname{range} T$;
    \item $T - \lambda I$ is normal for every $\lambda \in \mathbb{F}$;
    \item if $v \in V$ and $\lambda \in \mathbb{F}$, then $Tv = \lambda v$ if and only if $T^* v = \overline{\lambda} v$.
\end{enumerate}
\end{theorem}
\begin{proof}
\quad
\begin{enumerate}
    \item Suppose \(T\) is normal, then for all \(v \in \ker T\), then \(\|Tv\| = \|T^* v \| = 0\), therefore \(\ker T \subseteq \ker T^*\). On the other hand, \(\ker T^* \subseteq \ker T\). Therefore we have \(\ker T = \ker T^*\). 
    \item As we have previously shown, \(\operatorname{range} T = (\ker T^*)^\perp = (\ker T)^\perp = \operatorname{range} T^*\). 
    \item Since \(\operatorname{range} T = (\ker T)^\perp\), we have \(V = \operatorname{range} T \oplus \ker T\). 
    \item \[(T - \lambda I) (T - \lambda I)^* = (T - \lambda I) (T^* - \lambda I^*)\]
    \[= (T - \lambda I) (T^* - \lambda I) = TT^* - \lambda T - \lambda T^* + \lambda^2 I\]
    by normality of \(T\), this is
    \[T^* T - \lambda T - \lambda T^* + \lambda^2 I = (T^* - \lambda I^*)(T - \lambda I)\]
    \[= (T - \lambda I)^* (T - \lambda I).\] Therefore \((T - \lambda I)\) is also normal for any \(\lambda\). 
    \item If \(T v = \lambda v\), then for the case \(v = 0\), we indeed have \(T^* v = \overline{\lambda} v\). For the case \(v \ne 0\), \(v\) would be an eigenvector and \(\lambda\) an eigenvalue for \(T\). Therefore by calculation, we have \[\langle (T^* - \overline{\lambda} I) v, v \rangle = 0\] for all \(v \in V\). Therefore by a previous argument, \(T^* v = \overline{\lambda} v\). Suppose \(T^* v = \overline{\lambda} v\), then we have \((T^*)^* v = \overline{\overline{\lambda}}v\) which leads to the former argument. 
\end{enumerate}
\end{proof}
\begin{theorem}
Suppose $T \in \mathcal{L}(V)$ is normal. Then eigenvectors of $T$ corresponding to distinct eigenvalues are orthogonal.
\end{theorem}
\begin{proof}
We know \(\langle Tu, w \rangle = \langle u, T^* w \rangle\), therefore 
\[\langle T u, w \rangle - \langle u, T^* w \rangle = 0\]
\[\Longrightarrow \lambda \langle u, w \rangle - \mu \langle u, w \rangle = 0\]
\[\Longrightarrow \langle u, w \rangle = 0.\]
\end{proof}
\begin{theorem}
Suppose $\mathbb{F} = \mathbb{C}$ and $T \in \mathcal{L}(V)$. Then $T$ is normal if and only if there exist commuting self-adjoint operators $A$ and $B$ such that  
\[
T = A + iB.
\]
\end{theorem}
\begin{proof}
Suppose \(A\) and \(B\) are linear operators in \(\mathcal{L}(V)\) that commute, and are both self-adjoint. Suppose \(T = A + iB\), then there exists \(T^*\) that is the adjoint of \(T\). We have, for all \(v, w \in V\), \(\langle T v, w \rangle = \langle v, T^* w \rangle\), which means 
\[\langle (A + iB) v, w \rangle = \langle A v, w \rangle + \langle iBv, w \rangle = \langle v, A^* w \rangle + \langle v, -i B^* w \rangle.\]
Since both \(A\) and \(B\) are self-adjoint, we have 
\[\langle v, T^* w \rangle = \langle v, (A - i B) w \rangle,\]
which implies \(T^* = A - i B\). Therefore, by commutativity between \(A\) and \(B\), we have \(T^* T = (A - i B) (A + i B) = A^2 + B^2\), which is also \((A+iB)(A-iB) = TT^*\). Therefore \(T\) is normal. 

On the other hand, if we know that \(T\) is normal, we can define \(A\) by 
\[A = \frac{1}{2}\left(T + T^*\right),\]
and define \(B\) by 
\[B = \frac{1}{2i} (T - T^*),\]
and a simple calculation shows that \(AB = BA\). 
\end{proof}
\section{Real spectral theorem}
We know that, for \(b, c \in \mathbb{R}\) such that \(b^2 < 4c\), we have 
\[
x^2 + bx + c = \left(x + \tfrac{b}{2}\right)^2 + \left(c - \tfrac{b^2}{4}\right) > 0.
\]
In particular, $x^2 + bx + c$ is an invertible real number (a convoluted way of saying that it is not $0$).  

Replacing the real number $x$ with a self-adjoint operator (recall the analogy between real numbers and self-adjoint operators) leads to the next result.
\begin{theorem}
Suppose \( T \in \mathcal{L}(V) \) is self-adjoint and \( b, c \in \mathbb{R} \) are such that 
\( b^2 < 4c \). Then
\[
T^2 + bT + cI
\]
is an invertible operator.
\end{theorem}
\begin{proof}
We do not try to construct an operator and argue that it is the inverse of \(T^2 + bT + cI\). Instead, we try the following strategy: we show that \(T^2 + bT + cI\) maps any nonzero vector \(v\) into a nonzero \((T^2 + bT + cI)v \in V\), thus showing that \(T^2 + bT + cI\) is injective, and since \(T^2 + bT + cI\) maps \(V\) into itself, injectivity of \(T^2 + bT + cI\) implies it is invertible. 

We have 
\[\langle (T^2 + bT + cI) v, v \rangle = \langle T^2 v, v \rangle + b \langle Tv, v \rangle + c \|v\|^2\]
\[= \|Tv\|^2 + c \|v\|^2 + b \langle Tv, v \rangle \geq \|Tv\|^2 + c \|v\|^2 - |b| \|Tv\|\|v\| > 0.\]
Therefore, \(\langle (T^2 + bT + cI)v, v \rangle >0\) for all nonzero \(v\), which means \(\|(T^2 + bT + cI)v\|\|v\| > 0\) for all nonzero \(v\), thus \(\|(T^2 + bT + cI)v\|>0\) for all nonzero \(v\), which means \(T^2 + bT + cI\) is injective, thus also an isomorphism. 
\end{proof}
\begin{theorem}
Suppose $T \in \mathcal{L}(V)$ is self-adjoint. Then the minimal polynomial of $T$ equals
\[
(z - \lambda_1)\cdots(z - \lambda_m) \quad \text{for some } \lambda_1, \ldots, \lambda_m \in \mathbb{R}.
\]
\end{theorem}
\begin{proof}
In general, for a linear operator \(T: V \to V\) where \(V\) is an inner product space over \(\mathbb{R}\), the minimal polynomial of \(T\) is in the form 
\[p(T) = (T^2 + b_1 T + c_1 I) ... (T^2 + b_n T + c_n I) (T - \lambda_1 I) ... (T - \lambda_m I),\]
where \(b_i^2 < 4c_i\) for all \(i = 1, 2, ..., n\). Here we want to show that the previous \(n\) terms does not exists. 

By re-labeling, the minimal polynomial of \(T\) is in the form 
\[p(T) = (T^2 + b_1 T + c_1 I)^{l_1} ... (T^2 + b_n T + c_n I)^{l_n} (T - \lambda_1 I)^{k_1} ... (T - \lambda_m I)^{k_m},\]
where the \(\lambda\)'s and \((b, c)\) pairs are distinct. In a previous section, we have shown that this means 
\[V = \ker (T^2 + b_1 T + c_1 I)^{l_1} \oplus ... \oplus \ker (T^2 + b_n T + c_n I)^{l_n} \oplus \ker (T - \lambda_1 I)^{k_1} \oplus ... \oplus \ker (T - \lambda_m I)^{k_m},\]
and for each \(i = 1, 2, ..., n\) and \(j = 1, 2, ..., m\), we have 
\[\ker (T^2 + b_i T + c_i I) \subseteq \ker (T^2 + b_i T + c_i I)^2 \subseteq ... \subseteq \ker (T^2 + b_i T + c_i I)^{l_i}\]
and 
\[\ker (T - \lambda_j I) \subseteq \ker (T - \lambda_j I)^2 \subseteq ... \subseteq \ker (T - \lambda_j I)^{k_j}.\]
Since \(T\) is self-adjoint, \((T^2 + b_i T + c_i I)^{l_i}\) cannot annihilate any nonzero vector, so \(\ker (T^2 + b_i T + c_i I)^{l_i} = \{0\}\). Therefore those previous \(n\) terms does not exist in the minimal polynomial. 
\end{proof}
\begin{theorem}[Real spectral theorem]
Suppose \( \mathbb{F} = \mathbb{R} \) and \( T \in \mathcal{L}(V) \). Then the following are equivalent.
\begin{enumerate}
    \item[(a)] \( T \) is self-adjoint.
    \item[(b)] \( T \) has a diagonal matrix with respect to some orthonormal basis of \( V \).
    \item[(c)] \( V \) has an orthonormal basis consisting of eigenvectors of \( T \).
\end{enumerate}
\end{theorem}
\begin{proof}
Suppose \((a)\) is true, then the minimal polynomial of \(T\) would be in the form 
\[p(T) = (T - \lambda_1 I)^{k_1} ... (T - \lambda_n I)^{k_n}\]
for distinct \(\lambda_1, ..., \lambda_n\). Then we have 
\[V = \ker (T - \lambda_1 I)^{k_1} \oplus ... \oplus \ker (T - \lambda_n I)^{k_n},\]
and if we specify bases \(\mathcal{B}_i\) for \(\ker (T - \lambda_i I)^{k_i}\) for each \(i = 1, 2, ..., n\), then \(\mathcal{B} = \mathcal{B}_1 \bigcup ... \bigcup \mathcal{B}_n\) is a basis for \(V\), and since \(T\) is invariant on \(\ker (T - \lambda I)^k\) for any \(\lambda\) and any \(k\), \([T]_{\mathcal{BB}}\) is a block-diagonal matrix. 

\textcolor{red}{Proof One:} We have shown that, there exists an orthonormal basis \(\mathcal{B}\), such that the matrix of \(T\) with respect to \(\mathcal{B}\) is upper-triangular. Therefore \([T^*]_{\mathcal{BB}} = [T^T]_{\mathcal{BB}}\) would be lower-triangular. However, since \(T = T^*\), the matrix of \(T\) would be both upper-triangular and lower-triangular, which implies it is diagonal. Therefore we have \((a) \Longrightarrow (b)\) and \((a) \Longrightarrow (c)\). Now \((b) \Longrightarrow (a)\) and \((c) \Longrightarrow (a)\) are trivial. 

\textcolor{red}{Proof Two:} We pick one of the \(n\) subspaces \(\ker (T - \lambda_i I)^{k_i}\) of \(V\), and relabel it as \(\ker (T - \lambda I)^k\).

Assume there is a vector \(v \in \ker (T - \lambda I)^k\) such that \(v \notin \ker (T - \lambda I)^{k-1}\). 

Suppose \(k\) is even, then there exists \(l\) such that \(2l = k\), and we have 
\[\langle v, (T - \lambda I)^k v \rangle = \langle (T -  \lambda I)^l v, (T -  \lambda I)^l v \rangle = \| (T -  \lambda I)^l v \|^2 = 0,\]
which leads to a contradiction. For now the conclusion is that for every \(\ker (T - \lambda_i I)^{k_i}\), we have 
\[\ker (T - \lambda_i I) = \ker (T - \lambda_i I)^2 \subseteq \ker (T - \lambda_i I)^3 = ... \subseteq \ker (T - \lambda_i I)^{k_i}.\]
Suppose \(k\) is odd, then assume there exists \(v \in \ker (T - \lambda I)^k\) while \(v \notin \ker (T - \lambda I)^{k - 1}\), then \((T - \lambda I) v \in \ker (T - \lambda I)^{k - 1} = \ker (T - \lambda I)^{k - 2}\), then \((T - \lambda I)^{k - 2} (T - \lambda I) v = 0\). Contradiction. Therefore, in the minimal polynomial of \(T\), all the factorization terms have power one. The rest is omitted. 
\end{proof}
\begin{remark}
\textcolor{ForestGreen}{A conclusion here: For self-adjoint operators on real inner product spaces, the terms \((T^2 + bT+ cI)\) with \(b^2 < 4c\) in the minimal polynomial disappear because they are invertible (therefore does not annihilate anything), and the terms \((T - \lambda I)\) with distinct \(\lambda\) all have degree one because we can either show that \(\ker (T - \lambda I)^k\) are trivial for \(k > 1\), or we can show by representing them into matrices and show that they are diagonal because they are both upper-triangular and lower-triangular.}
\end{remark}
\begin{remark}
Another remark regarding the proof: For the eigenspace \(\ker (T - \lambda I)^k\) with index \(k\), if \(k\) is even, we can reduce it by half; if \(k\) is odd, we reduce \(k+1\) by half. And we get \(\ker (T - \lambda I)^k = \ker (T - \lambda I)\) nevertheless. 
\end{remark}
\section{Complex spectral theorem}
\begin{theorem}
Suppose $\mathbb{F} = \mathbb{C}$ and $T \in \mathcal{L}(V)$. Then the following are equivalent.
\begin{enumerate}
    \item[(a)] $T$ is normal.
    \item[(b)] $T$ has a diagonal matrix with respect to some orthonormal basis of $V$.
    \item[(c)] $V$ has an orthonormal basis consisting of eigenvectors of $T$.
\end{enumerate}
\end{theorem}
\begin{proof}
\((b) \Longleftrightarrow (c)\) is trivial. 

As for \((a)\), suppose \((a)\) holds, then by Schur's theorem, there is an orthonormal basis \(\mathcal{E} = \{e_1, ..., e_n\}\) of \(V\) such that \([T]_{\mathcal{EE}}\) is an upper-triangular matrix. 

Denote the entries as \(a_{i, j}\) for \(i \leq j\), and the rest as \(0\). Then we have 
\[\|T e_1 \|^2 = \|a_{1, 1} e_1 \|^2 = \|a_{1, 1} \|^2,\]
and since \(\mathcal{E}\) is a basis consisting of orthonormal vectors, \([T^*]_{\mathcal{EE}}\) is the conjugate transpose of  \([T]_{\mathcal{EE}}\), with entries \(a_{j, i}\). Therefore 
\[\|T^* e_1 \|^2 = |a_{1, 1}|^2 + |a_{1, 2}|^2 + ... + |a_{1, n}|^2. \]
But since \(\|T e_1\|^2 = \|T^* e_1 \|^2\), we get that 
\[|a_{1, 2}|^2 + ... + |a_{1, n}|^2 = 0,\]
so every one of them is zero. Similarly, \(\|T e_2\|^2 = \|T^* e_2 \|^2\), implying 
\[|a_{2, 3}|^2 + ... + |a_{2, n}|^2 = 0.\]
The other non-diagonal entries follow the same argument. The rest of the proof is omitted. 
\end{proof}
\begin{remark}
\textcolor{ForestGreen}{A conclusion here: For normal operators (no need to be self-adjoint) on complex inner product space, since \(Tv\) and \(T^* v\) have the same norm for all \(v \in V\), by representing the operators as matrices and calculating the norms of the column vectors, we get that the minimal polynomial is in the form \((T - \lambda_1 I)...(T - \lambda_m I)\) for distinct \(\lambda\).}
\end{remark}
\section{Positive operators}
\begin{definition}
An operator $T \in \mathcal{L}(V)$ is called \emph{positive} if $T$ is self-adjoint and
\[
\langle Tv, v \rangle \geq 0
\]
for all $v \in V$.
\end{definition}
\begin{definition}
An operator \(R\) is called a square root of an operator \(T\) if \(R^2 = T\). 
\end{definition}
\begin{theorem}[characterizations of positive operators]
Let $T \in \mathcal{L}(V)$. Then the following are equivalent.
\begin{enumerate}
    \item[(a)] $T$ is a positive operator.
    \item[(b)] $T$ is self-adjoint and all eigenvalues of $T$ are nonnegative.
    \item[(c)] With respect to some orthonormal basis of $V$, the matrix of $T$ is a diagonal matrix with only nonnegative numbers on the diagonal.
    \item[(d)] $T$ has a positive square root.
    \item[(e)] $T$ has a self-adjoint square root.
    \item[(f)] $T = R^* R$ for some $R \in \mathcal{L}(V)$.
\end{enumerate}
\end{theorem}
\begin{proof}
Suppose \((a)\) is true, then \(T\) is self-adjoint and \(\langle Tv, v \rangle \geq 0\) for all \(v \in V\). Suppose \(v\) is an eigenvector of \(T\), then there exists a corresponding eigenvalue of \(T\), denoted \(\lambda\). Then \(\langle Tv, v \rangle = \langle \lambda v, v \rangle = \lambda \|v\|^2 \geq 0\). Therefore \(\lambda\) is nonnegative.

Now \(T\) is self-adjoint also implies that the minimal polynomial of \(T\) is in the form 
\[(T - \lambda_1 I) ... (T - \lambda_m I)\]
for distinct \(\lambda_1, ..., \lambda_m\), therefore eigenvectors corresponding to distinct eigenvalues are perpendicular, which means 
\[\ker (T - \lambda_i I) \perp \ker (T - \lambda_j I)\]
for each pair of distinct \(i, j = 1, 2, ..., m\). Therefore by choosing orthonormal bases in each \(\ker (T - \lambda_i I) \subseteq V\), we get an orthonormal basis for \(V\) where each eigenvector is an eigenvector, and the matrix of \(T\) with respect to this basis is diagonal. 

Denote the orthonormal basis as 
\[\mathcal{E} = \{e_1, e_2, ..., e_n\},\]
and \([T]_{\mathcal{EE}} = \operatorname{diag}\{\mu_1, \mu_2, ..., \mu_n\}\) for nonnegative \(\mu\) with potential multiplicities. Define \(R: V \to V\) such that \(R e_i = \sigma_i e_i\), where \(\sigma_i = \sqrt{\mu_i}\) for each \(i\), then for any vector \(x = x_1 e_1 + ... + x_n e_n\) in \(V\), \(R x = x_1 \sigma_1 e_1 + ... + x_n \sigma_n e_n\), and so 
\[R^2 x = R(Rx) = x_1 \sigma_1^2 e_1 + ... + x_n \sigma_n^2 e_n = x_1 \mu_1 e_1 + ... + x_n \mu_n e_n = T x.\]
Therefore \(T = R^2\), and since \(R\) is positive, \(T\) has a positive square root. 

We know that \(R\) is self-adjoint as well (proof omitted), so \(T\) has a self-adjoint square root. Therefore \(T = R^* R\) for some \(R \in \mathcal{L}(V)\). 

Suppose \(T = R^* R\) for some \(R \in \mathcal{L}(V)\), then for any \(v \in V\), 
\[\langle Tv, v \rangle = \langle Rv, Rv \rangle = \|Rv\|^2 \geq 0,\]
therefore \(T\) is a positive operator, we get \((a)\). 
\end{proof}
\begin{theorem}
Every positive operator on \(V\) has a unique positive square root. 
\end{theorem}
\begin{remark}
If we do not make the constraint that the square root is positive, there may be multiple square roots. For example, \(-I\) and \(I\) are both square roots of \(I\). 
\end{remark}
\begin{proof}
Suppose \(R\) is a positive square root of \(T\). Since \(R\) is a positive operator, there exists an orthonormal basis of \(V\), denoted 
\[\mathcal{E} = \{e_1, ..., e_n\},\]
such that each \(e_i\) is an eigenvector of \(R\), corresponding to a positive eigenvalue \(\sigma_i\). Therefore \(T e_i = R^2 e_i = \sigma_i^2 e_i\) for each \(i = 1, 2, ..., n\). Then \(T\) written in a matrix with respect to \(\mathcal{E}\) is a diagonal matrix with diagonals \(\sigma_i^2\). Therefore each positive operator has only one positive square root. 
\end{proof}
\begin{remark}
For a positive operator \(T\), \(\sqrt{T}\) denotes the unique positive square root of \(T\). 
\end{remark}
\begin{theorem}
Suppose \(T\) is a positive operator on \(V\) and \(v \in V\) such that \(\langle Tv, v \rangle = 0\). Then \(Tv = 0\). 
\end{theorem}
\begin{proof}
\(\langle Tv, v \rangle = 0\) implies that \(\langle \sqrt{T}v, \sqrt{T}v \rangle = 0\), which further implies that \(\|\sqrt{T}v\|^2 = 0\), and \(\sqrt{T}v = 0\) \(\Longrightarrow Tv = \sqrt{T} \sqrt{T} v = 0\). 
\end{proof}
\section{Isometries}
\begin{definition}[isometry]
A linear map $S \in \mathcal{L}(V,W)$ is called an \textit{isometry} if
\[
\|Sv\| = \|v\|
\]
for every $v \in V$. In other words, a linear map is an isometry if it preserves norms.
\end{definition}
\begin{corollary}
Every isometry is injective. Proof omitted.
\end{corollary}
\begin{theorem}
Suppose $S \in \mathcal{L}(V,W)$. Suppose $e_1, \ldots, e_n$ is an orthonormal basis of $V$ and 
$f_1, \ldots, f_m$ is an orthonormal basis of $W$. Then the following are equivalent.  
\begin{enumerate}
    \item $S$ is an isometry.
    \item $S^* S = I$.
    \item $\langle Su, Sv \rangle = \langle u, v \rangle$ for all $u,v \in V$.
    \item $Se_1, \ldots, Se_n$ is an orthonormal list in $W$.
    \item The columns of $\mathcal{M}(S, (e_1, \ldots, e_n), (f_1, \ldots, f_m))$ form an orthonormal list 
    in $\mathbb{F}^m$ with respect to the Euclidean inner product.
\end{enumerate}
\end{theorem}
\begin{remark}
Note that \((S^* S)^* = S^* (S^*)^* = S^* S\), therefore \(S^*S\) is self-adjoint. 
\end{remark}
\begin{proof}
Suppose \(S\) is an isometry, then for any \(v \in V\), \(\|Sv\|^2 = \|v\|^2\), which implies \(\langle Sv, Sv \rangle = \langle v, v \rangle\), therefore \(\langle (S^* S - I) v, v \rangle = 0\) for all \(v \in V\). Since \(S^* S - I\) is self-adjoint, this implies \(S^* S - I = 0\). Therefore \((1) \Longrightarrow (2)\). 

Now suppose \((2)\) is true, then \((3)\) is also true (proof omitted). 

Suppose \((3)\) is true. Suppose \(e_1, ..., e_n\) is an orthonormal list in \(V\), then \(\|Se_i\|^2 = \langle Se_i, Se_i \rangle = \langle e_i, e_i \rangle = 1\) for all \(i = 1, 2, ..., n\), and for al distinct pairs of \(i, j = 1, 2, ..., n\), \(\langle Se_i, Se_j \rangle = \langle e_i, e_j \rangle = 0\). Therefore \(Se_1, ..., Se_n\) is an orthonormal list in \(W\). So \((3) \Longrightarrow (4)\). 

Suppose \((4)\) is true, then we know that $\mathcal{M}(S, (e_1, \ldots, e_n), (f_1, \ldots, f_m))$ is the matrix whose column vectors are \(Se_1, ..., Se_n\) written in the basis \(f_1, ..., f_m\). Therefore the matrix's \(i\)-th column vector is \(Se_i\) written in basis \(f_1, ..., f_m\). Denote 
\[[Se_i]_{\{f_1, ..., f_m\}} = [y_1^i, y_2^i, ..., y_m^i]^T\]
for some \(y_1^i, y_2^i, ..., y_m^i \in \mathbb{F}\), then we have 
\[Se_i = y_1^i f_1 + y_2^i f_2 + ... + y_m^i f_m.\]
\(\|Se_i\|\) has norm one implies that 
\[\|y_1^i f_1 + y_2^i f_2 + ... + y_m^i f_m\|^2 = |y_1^i|^2 + |y_2^i|^2 + ... + |y_m^i|^2 = 1,\]
and \(Se_i\) is orthogonal to \(Se_j\) for \(i \ne j\) implies that 
\[0 = \langle Se_i, Se_j \rangle = \langle y_1^i f_1 + y_2^i f_2 + ... + y_m^i f_m, y_1^j f_1 + y_2^j f_2 + ... + y_m^j f_m \rangle\]
\[= y_1^i \overline{y_1^j} + y_2^i \overline{y_2^j} + ... + y_m^i \overline{y_m^j}.\]
Therefore, the columns form an orthonormal list in \(\mathbb{F}^m\) with respect to the Euclidean inner product. 

\((5) \Longrightarrow (1)\) follows from direct calculation. 
\end{proof}
\section{Unitary operators}
\begin{definition}[unitary operator]
An operator is called unitary if \(S: V \to V\) is an invertible isometry. 
\end{definition}
\begin{remark}
Although the words "unitary" and "isometry" mean the same thing for operators on finite-dimensional inner product spaces, remember that a unitary operator maps a vector space to itself, while an isometry maps a vector space to another (possibly different) vector space.
\end{remark}
\begin{theorem}
Suppose $S \in \mathcal{L}(V)$. Suppose $e_{1}, \ldots, e_{n}$ is an orthonormal basis of $V$. 
Then the following are equivalent.
\begin{enumerate}
    \item $S$ is a unitary operator.
    \item $S^{*} S = SS^{*} = I$.
    \item $S$ is invertible and $S^{-1} = S^{*}$.
    \item $Se_{1}, \ldots, Se_{n}$ is an orthonormal basis of $V$.
    \item The rows of $\mathcal{M}(S, (e_{1}, \ldots, e_{n}))$ form an orthonormal basis of $\mathbb{F}^{n}$ with respect to the Euclidean inner product.
    \item $S^{*}$ is a unitary operator.
\end{enumerate}
\end{theorem}
\begin{proof}
\((1) \Longrightarrow (2) \Longrightarrow (3) \Longrightarrow (4)\) is trivial. Now suppose we know \((4)\), then column vectors of the matrix representation of \(S\), denoted \(N\), form an orthonormal basis. Therefore let \(M = N^*\) be the matrix representation of the transpose of \(N\), then we have \(M N = I\). Therefore, \(M\) is the inverse of \(N\), which means \(M\) is the matrix representation of \(S^*\). Therefore \(N M = I\) as well. Denote rows of \(N\) as \(v_1, ..., v_n\), then columns of \(M\) are also \(v_1, ..., v_n\), which means \(\langle v_i, v_i \rangle = 1\) for all \(i\) and \(\langle v_i, v_j \rangle = 0\) for all distinct pairs of \(i, j = 1, 2, ..., n\). Therefore rows of the matrix representation of \(S\) also forms an orthonormal basis of \(\mathbb{F}^n\). Therefore \((4) \Longrightarrow (5)\). 

Now suppose \((5)\) is true, then rows and columns of the matrix representation of \(S^*\) also form orthonormal bases, which means \(S^*\) is also a unitary operator. And by the same argument we know that \(S = (S^*)^*\) is a unitary operator. So \((5) \Longrightarrow (6) \Longrightarrow (1)\). 
\end{proof}
\begin{remark}
Recall that in matrices, the notation \(A^*\) means conjugate transpose, while in operators the notation \(T^*\) means adjoint. 
\end{remark}
\begin{theorem}
Suppose \(\lambda\) is an eigenvalue of an unitary operator, then \(|\lambda| = 1\). 
\end{theorem}
Proof omitted. 
\begin{theorem}
Suppose $\mathbb{F} = \mathbb{C}$ and $S \in \mathcal{L}(V)$. 
Then the following are equivalent.
\begin{enumerate}
    \item $S$ is a unitary operator.
    \item There is an orthonormal basis of $V$ consisting of eigenvectors of $S$ whose corresponding eigenvalues all have absolute value $1$.
\end{enumerate}
\end{theorem}
\begin{proof}
First of all, \((2) \Longrightarrow (1)\) is evident. 

Suppose \((1)\) is true, then \(S\) is normal. The rest is omitted. 
\end{proof}
\section{QR Factorization}
\begin{definition}[unitary matrix]
An \(n\) by \(n\) matrix is unitary if its columns form an orthonormal list in \(\mathbb{F}^n\). 
\end{definition}
\begin{theorem}
Suppose \( Q \) is an \( n \times n \) matrix. Then the following are equivalent.
\begin{enumerate}
    \item \( Q \) is a unitary matrix.
    \item The rows of \( Q \) form an orthonormal list in \( \mathbb{F}^n \).
    \item \( \|Qv\| = \|v\| \) for every \( v \in \mathbb{F}^n \).
    \item \( Q^{*}Q = QQ^{*} = I \), the \( n \times n \) matrix with 1’s on the diagonal and 0’s elsewhere.
\end{enumerate}
\end{theorem}
\begin{proof}
\((1) \Longleftrightarrow (4)\) is trivial: Suppose \((1)\) is true, then columns of \(Q\) is an orthonormal basis of \(\mathbb{F}^n\), we denote them as \(q_1, ..., q_n\). Then \(Q^* Q\) has entries \((Q^*Q)_{i, j} = \langle q_i, q_j\rangle = \delta_{i, j}\), therefore \(Q^* Q = I\). Since \(Q\) is a square matrix, this means \(Q\) is invertible, therefore \(QQ^* = I\) as well. Therefore \((1) \Longrightarrow (4)\). Suppose \((4)\) is true, then denote column vectors of \(Q\) as \(q_1, ..., q_n\), since \(Q^* Q = I\), we have \(\langle q_i, q_j\rangle = \delta_{i, j}\). Therefore \(Q\) is a unitary matrix, which means \((4) \Longrightarrow (1)\). 

\((4) \Longleftrightarrow (3)\) is trivial. Omitted.

Suppose we have \((1), (3), (4)\). Let \(A = Q^*\), then since \(A^* = Q\), we have \(AA^* = A^* A = I\). By equivalence of \((4)\) and \((1)\), \(A\) is a unitary matrix, so columns of \(A\) form an orthonormal list in \(\mathbb{F}^n\). Therefore row of \(Q\), which are conjugates of the columns of \(A\), form an orthonormal list in \(\mathbb{F}^n\).
\end{proof}
\begin{theorem}
Suppose $A$ is a square matrix with linearly independent columns. Then there exist unique matrices $Q$ and $R$ such that $Q$ is unitary, $R$ is upper triangular with only positive numbers on its diagonal, and
\[
A = QR.
\]
\end{theorem}
\begin{proof}
Suppose column vectors of \(A\) are denoted as \(v_1, ..., v_n\), and since they are linearly independent, we can do Gram-Schmidt decomposition on this list of vectors, after which we got a list of orthonormal vectors, denoted \(q_1, ..., q_n\). Then we have 
\[v_1 \in \operatorname{span}\{q_1\};\]
\[v_2 \in \operatorname{span}\{q_1, q_2\};\]
\[v_3 \in \operatorname{span}\{q_1, q_2, q_3\};\]
\[\vdots\]
\[v_{n-1} \in \operatorname{span}\{q_1, ..., q_{n-1}\};\]
\[v_n \in \operatorname{span}\{q_1, ..., q_n\}.\]
Therefore, for each \(i = 1, 2, ..., n\), there exists scalars \(x_1^i, x_2^i, ..., x_i^i\), such that 
\[v_i = x_1^i q_1 + x_2^i q_2 + ... + x_i^i q_i.\]
Therefore, let \(x_i^j\) be the \(i, j\)-th entry of \(R\), and let \(q_i\) be the column vectors of \(Q\), we get the QR decomposition. 

Recalling the process of Gram-Schmidt decomposition, we know that each \(v_i\) is a linear combination of \(q_1, ..., q_i\) with \(q_i\) paired with a positive scalar. Therefore the proof is complete. 
\end{proof}
\begin{remark}
If a QR factorization is available, then it can be used to solve a corresponding system of linear equations without using Gaussian elimination. Specifically, suppose $A$ is an $n$-by-$n$ square matrix with linearly independent columns. Suppose that $b \in \mathbb{F}^n$ and we want to solve the equation $Ax = b$ for $x = (x_1, \ldots, x_n) \in \mathbb{F}^n$.

Suppose $A = QR$, where $Q$ is unitary and $R$ is upper triangular with only positive numbers on its diagonal ($Q$ and $R$ are computable from $A$ using just the Gram-Schmidt procedure). The equation $Ax = b$ is equivalent to the equation $QRx = b$. Multiplying both sides of this last equation by $Q^*$ on the left and we have
\[
Rx = Q^* b.
\]
The matrix $Q^*$ is the conjugate transpose of the matrix $Q$. Thus computing $Q^* b$ is straightforward. Because $R$ is an upper-triangular matrix with positive numbers on its diagonal, the system of linear equations represented by the equation above can quickly be solved by first solving for $x_n$, then for $x_{n-1}$, and so on.
\end{remark}
\section{Cholesky Factorization}
\begin{definition}[positive invertible operator]
A self-adjoint operator \(T \in \mathcal{L}(V)\) is positive invertible operator if and only if \(\langle Tv, v \rangle > 0\) for all nonzero \(v \in V\). 
\end{definition}
\begin{definition}[positive definite]
A matrix $B \in \mathbb{F}^{n,n}$ is called \emph{positive definite} if $B^* = B$ and 
\[
\langle Bx, x \rangle > 0
\]
for every nonzero $x \in \mathbb{F}^n$.
\end{definition}
\begin{theorem}[Cholesky factorization]
Suppose $B$ is a positive definite matrix. Then there exists a unique upper-triangular matrix $R$ with only positive numbers on its diagonal such that  
\[
B = R^* R.
\]
\end{theorem}
\begin{proof}
Since \(B\) is positive definite, it is positive and self-adjoint. Therefore there exists a basis \(\mathcal{B}\) of \(V\) with respect to which \(B\) is a diagonal matrix. Since \(B\) is strictly positive, every diagonal entry is strictly positive. Let \(A\) be the diagonal matrix with strictly positive diagonals such that \(A^2 = [B]_{\mathcal{BB}}\), then let \(T\) be the operator of \(A\) and we have \(B = T^2 = T^* T\). Since \(T\) is invertible, then there exists a unitary \(Q\) and an upper-triangular \(R\) with only positive numbers on its diagonal such that \(T = QR\). Therefore \(B = T^* T = R^* Q^* Q R = R^* R\). 
\end{proof}
\section{Singular Value Decomposition}
\begin{theorem}
Suppose $T \in \mathcal{L}(V,W)$. Then  
\begin{enumerate}
\item[(a)] $T^{*}T$ is a positive operator on $V$;
\item[(b)] $\operatorname{null} T^{*}T = \operatorname{null} T$;
\item[(c)] $\operatorname{range} T^{*}T = \operatorname{range} T^{*}$;
\item[(d)] $\dim \operatorname{range} T = \dim \operatorname{range} T^{*} 
= \dim \operatorname{range} T^{*}T$.
\end{enumerate}
\end{theorem}
\begin{proof}
\((a)\) and \((b)\) are omitted. For \((c)\), we have 
\[\operatorname{range} T^* T = (\ker T^* T)^\perp = (\ker T)^\perp = \operatorname{range} T^*.\]
\((d)\) is proved by \((c)\). Omitted. 
\end{proof}
\begin{remark}
The last equation, 
\[(\ker T)^\perp = \operatorname{range} T^*\]
is proved by a previous theorem. 

\textcolor{ForestGreen}{Another way of showing that \((\ker T)^\perp = \operatorname{range} T^*\) is as follows:} 
\[\operatorname{range} T^* \subseteq (\ker T)^\perp\]
is trivial: for any \(w \in W\), and any \(x \in \ker T\), \(\langle T^* w, x \rangle = \langle w, Tx \rangle = 0\), therefore \(w \in (\ker T)^\perp\). 

Now we suppose \(v \in (\ker T)^\perp\), then \(v \in (\ker T^* T)^\perp = \operatorname{range} T^* T\), therefore there exists \(x\), such that \(v = T^* T x\). Therefore \(v \in \operatorname{range} T^*\), which implies
\[(\ker T)^\perp \subseteq \operatorname{range} T^*.\]
\textcolor{red}{We can see that this proof makes use of the fact that for self-adjoint linear operator \(T^* T\), there exists a basis for \(V\) with respect to which the matrix representation of \(T^* T\) is a diagonal matrix with non-negative entries, therefore \(\operatorname{range} T^* T \perp \ker (T^* T)\) and \(\operatorname{range}T^* T \oplus \ker T^* T = V\).} 
\end{remark}
\begin{definition}[singular values]
Suppose $T \in \mathcal{L}(V,W)$. The \emph{singular values} of $T$ are the nonnegative square roots of the eigenvalues of $T^{*}T$, listed in decreasing order, each included as many times as the dimension of the corresponding eigenspace of $T^{*}T$.
\end{definition}
\begin{remark}
\textcolor{blue}{For a self-adjoint linear operator, our conclusion is that all the eigenspaces are in the form \(\ker (T^* T - \lambda_i I)\), which means the term \((T^* T - \lambda_i I)\) always has degree one. For a positive linear operator, our conclusion is that all the eigenvalues are non-negative.} Now recall that for a self-adjoint operator, eigenvectors corresponding to distinct eigenvalues are orthogonal, therefore \textcolor{blue}{there exists an orthonormal basis of \(V\) such that with respect to which \(T^* T\) is a diagonal matrix.} \textcolor{red}{Therefore, following our argument, there exists an orthonormal basis of \(V\), with respect to which \(T^* T\) has a diagonal matrix representation, with non-negative entries. }
\end{remark}
\begin{theorem}
Suppose that $T \in \mathcal{L}(V,W)$. Then  
\begin{enumerate}
\item[(a)] $T$ is injective $\iff 0$ is not a singular value of $T$;
\item[(b)] the number of positive singular values of \(T\) equals $\dim \operatorname{range} T$;
\item[(c)] $T$ is surjective $\iff$ number of positive singular values of $T$ equals $\dim W$.
\end{enumerate}
\end{theorem}
\begin{proof}
Proof of \((a)\): 

Suppose \(0\) is not a singular value of \(T\), then all singular values of \(T\) are positive \(\Longrightarrow\) all eigenvalues of \(T^* T\) are positive \(\Longrightarrow\) \(T^* T\) are invertible \(\Longrightarrow\) \(\ker T^* T = \{0\}\) \(\Longrightarrow\) \(\ker T \subseteq \ker T^* T = \{0\}\) \(\Longrightarrow\) \(\ker T = \{0\}\) \(\Longrightarrow\) \(T\) is injective. 

Suppose \(T\) is injective. Assume \(T^* T\) maps some nonzero vector \(v \in V\) to zero, then 
\[\|Tv\|^2 = \langle Tv, Tv \rangle = \langle T^* Tv, v \rangle = 0,\]
\(\Longrightarrow T\) is not injective, therefore we get a contradiction. Therefore if \(T\) is injective, \(T^* T\) is also injective, which implies \(0\) is not a singular value of \(T\).

Proof of \((b)\):

Suppose \(\mathcal{B}\) is an orthonormal basis of \(V\), with respect to which the matrix representation of \(T^* T\) is diagonal. Then number of positive singular values of \(T =\) number of positive diagonals of \([T^* T]_{\mathcal{BB}} = \) \(\dim \operatorname{range} T^* T\). We claim that
\[T^*: \operatorname{range} T \to \operatorname{range} T^* T\]
is injective and surjective, then we will have number of positive singular values of \(T =\) number of positive diagonals of \([T^* T]_{\mathcal{BB}} = \) \(\dim \operatorname{range} T^* T = \dim \operatorname{range} T\). First of all, this mapping is of course surjective by notation. Second, suppose \(T^* x = 0\) for some \(x \in \operatorname{range} T\), then there exists a \(v \in V\) such that \(x = Tv\). Now \(T^* Tv = 0\) implies \(\langle T^* Tv, v \rangle = \langle Tv, Tv \rangle = \|Tv\|^2 = 0\), therefore \(v \in \ker T\), which means \(x = 0\). Therefore the map 
\[T^*: \operatorname{range} T \to \operatorname{range} T^* T\]
is injective. 

Proof of \((c)\):

We have proved in the previous discussion that the map 
\[T^*: \operatorname{range} T \to \operatorname{range} T^* T\]
is invertible. 

Suppose \(T\) is surjective, then
\[\dim W = \dim \operatorname{range}T = \dim \operatorname{range}T^* T = \text{number of positive singular values of }T.\]
Suppose number of positive singular values of \(T\) equals \(\dim W\), then 
\[\dim W = \dim \operatorname{range}T^* T = \dim \operatorname{range} T,\]
therefore \(T\) is surjective. 
\end{proof}
\begin{tabular}{|p{6cm}|p{6cm}|}
\hline
\textbf{list of eigenvalues} & \textbf{list of singular values} \\
\hline
context: vector spaces & context: inner product spaces \\
\hline
defined only for linear maps from a vector space to itself &
defined for linear maps from an inner product space to a possibly different inner product space \\
\hline
can be arbitrary real numbers (if $F = \mathbb{R}$) or complex numbers (if $F = \mathbb{C}$) &
are nonnegative numbers \\
\hline
can be the empty list if $F = \mathbb{R}$ &
length of list equals dimension of domain \\
\hline
includes $0 \iff$ operator is not invertible &
includes $0 \iff$ linear map is not injective \\
\hline
no standard order, especially if $F = \mathbb{C}$ &
always listed in decreasing order \\
\hline
\end{tabular}
\begin{theorem}
Suppose \(S \in \mathcal{L}(V, W)\), then \(S\) is an isometry \(\Longleftrightarrow\) all singular values of \(S\) equals one. 
\end{theorem}
Proof omitted. 
\section{SVD for linear maps and for matrices}
\begin{theorem}[singular value decomposition]
Suppose $T \in \mathcal{L}(V,W)$ and the positive singular values of $T$ are $s_{1}, \ldots, s_{m}$. Then there exist orthonormal lists $e_{1}, \ldots, e_{m}$ in $V$ and $f_{1}, \ldots, f_{m}$ in $W$ such that 
\[
Tv = s_{1} \langle v, e_{1} \rangle f_{1} + \cdots + s_{m} \langle v, e_{m} \rangle f_{m}
\]
for every $v \in V$. 
\end{theorem}
\begin{proof}
Since positive singular values of \(T\) are \(s_1, ..., s_m\), there exists an orthonormal basis \(\mathcal{B} = \{e_1, ..., e_m, e_{m+1}, ..., e_n\}\), such that \([T^*T]_{\mathcal{BB}} = \operatorname{diag}\{s_1^2, ..., s_m^2, 0, ..., 0\}\), which has \(n - m\) zeros on the diagonal. Then \(\ker T = \ker T^*T = \operatorname{span}\{e_{m+1}, ..., e_n\}\), and \(\operatorname{range} T = \operatorname{span}\{Te_1, ..., Te_m\}\). Let 
\[f_i = \frac{Te_i}{s_i},\]
for all \(i = 1, 2, ..., m\), then 
\[\|f_i\|^2 = \langle f_i, f_i \rangle =\frac{1}{s_i^2} \langle Te_i, Te_i\rangle = \frac{1}{s_i^2} \langle T^* T e_i, e_i \rangle = 1,\]
and 
\[\langle f_i, f_j \rangle =\frac{1}{s_i s_j} \langle T^* T e_i, e_j \rangle = \frac{1}{s_i s_j} \langle s_i^2 e_i, e_j \rangle = 0.\]
Therefore 
\[
Tv = s_{1} \langle v, e_{1} \rangle f_{1} + \cdots + s_{m} \langle v, e_{m} \rangle f_{m}
\]
for every $v \in V$. 
\end{proof}
\begin{definition}[non-square diagonal matrix]
An $M$-by-$N$ matrix $A$ is called a \textit{diagonal matrix} if all entries of the matrix are $0$ except possibly $A_{k,k}$ for $k = 1, \ldots, \min\{M,N\}$.
\end{definition}
\begin{tabular}{|p{6cm}|p{6cm}|}
\hline
\textbf{spectral theorem} & \textbf{singular value decomposition} \\
\hline
describes only self-adjoint operators (when $F = \mathbb{R}$) or normal operators (when $F = \mathbb{C}$) & 
describes arbitrary linear maps from an inner product space to a possibly different inner product space \\
\hline
produces a single orthonormal basis & 
produces two orthonormal lists, one for domain space and one for range space, that are not necessarily the same even when range space equals domain space \\
\hline
different proofs depending on whether $F = \mathbb{R}$ or $F = \mathbb{C}$ & 
same proof works regardless of whether $F = \mathbb{R}$ or $F = \mathbb{C}$ \\
\hline
\end{tabular}
\begin{theorem}
Suppose $T \in \mathcal{L}(V,W)$ and the positive singular values of $T$ are $s_{1}, \ldots, s_{m}$. Suppose $e_{1}, \ldots, e_{m}$ and $f_{1}, \ldots, f_{m}$ are orthonormal lists in $V$ and $W$ such that
\[
Tv = s_{1}\langle v, e_{1}\rangle f_{1} + \cdots + s_{m}\langle v, e_{m}\rangle f_{m}
\]
for every $v \in V$. Then
\[
T^{*}w = s_{1}\langle w, f_{1}\rangle e_{1} + \cdots + s_{m}\langle w, f_{m}\rangle e_{m}
\]
and
\[
T^{\dagger}w = \frac{\langle w, f_{1}\rangle}{s_{1}} e_{1} + \cdots + \frac{\langle w, f_{m}\rangle}{s_{m}} e_{m}
\]
for every $w \in W$.
\end{theorem}
\begin{proof}
Proof of the first result: Pick any \(v \in V\) and \(w \in W\), we have 
\[\langle Tv, w \rangle = \langle s_1 \langle v, e_1 \rangle f_1 + ... + s_m \langle v, e_m \rangle f_m, w \rangle\]
\[= s_1 \langle v, e_1 \rangle \langle f_1, w \rangle + ... + s_m \langle v, e_m \rangle \langle f_m, w \rangle\]
\[= \langle v, s_1 e_1 \overline{\langle f_1, w \rangle} + ... + s_m e_m \overline{\langle f_m, w \rangle}\]
\[= \langle v, s_1 \langle w, f_1 \rangle e_1 + ... + s_m \langle w, f_m \rangle e_m \rangle\]
\[= \langle v, T^* w \rangle.\]
Therefore, for any \(w \in W\), we have 
\[T^* w = s_1 \langle w, f_1 \rangle e_1 + ... + s_m \langle w, f_m \rangle e_m.\]
Proof of the second result: Plug in \(v = e_i\) for all \(i = 1, 2, ..., m\), we have \(Te_i = s_i f_i\) for all \(i = 1, 2, ..., m\). Therefore 
\[\ker T = \operatorname{span}\{e_{m+1}, ..., e_n\},\]
and 
\[\operatorname{range}T = \operatorname{span}\{f_1, ..., f_m\}\]
\[= \operatorname{span}\{Te_1, ..., Te_m\}.\]
We get 
\[T: \operatorname{span}\{e_1, ..., e_m\} \to \operatorname{range}T = \operatorname{span}\{Te_1, ..., Te_m\}\]
is an isomorphism, and 
\[\operatorname{span}\{e_1, ..., e_m\} (\ker T)^\perp.\]
Therefore 
\[(T|_{(\ker T)^\perp})^{-1} f_i = \frac{e_i}{s_i}\]
for all \(i = 1, 2, ..., m\), and 
\[T^\dagger w = (T|_{(\ker T)^\perp})^{-1} P_{\operatorname{range}T} w \]
\[= (T|_{(\ker T)^\perp})^{-1} \left( \langle w, f_1 \rangle f_1 + \langle w, f_2 \rangle f_2 +... + \langle w, f_m \rangle f_m \right)\]
\[=\frac{\langle w, f_{1}\rangle}{s_{1}} e_{1} + \cdots + \frac{\langle w, f_{m}\rangle}{s_{m}} e_{m}\]
for every \(w \in W\). 
\end{proof}
\begin{theorem}[matrix version of SVD]
Suppose $A$ is a $p$-by-$n$ matrix of rank $m \geq 1$. Then there exist a $p$-by-$m$ matrix $B$ with orthonormal columns, an $m$-by-$m$ diagonal matrix $D$ with positive numbers on the diagonal, and an $n$-by-$m$ matrix $C$ with orthonormal columns such that
\[
A = BDC^*.
\]
\end{theorem}
\begin{proof}
Define \(V\) as the vector space of \(n\)-dimensional column vectors with entries in \(\mathbb{F}\), and \(W\) the vector space of \(p\)-dimensional column vectors with entries in \(\mathbb{F}\). Then \(A: V \to W\), a linear operator from \(V\) to \(W\). 

Since \(A\) has rank \(m\), we have \(\dim \operatorname{range} A = m\). Let \(s_1, ..., s_m\) be the positive singular values of \(A\), then by singular value decomposition theorem, there exists orthonormal lists \(e_1, ..., e_m\) in \(V\) and \(f_1, ..., f_m\) in \(W\), such that for every \(v \in V\), we have 
\[A v = s_1 \langle v, e_1 \rangle f_1 + ... + s_m \langle v, e_m \rangle f_m.\]
Let
\[
\begin{aligned}
B &= \text{the $p$-by-$m$ matrix whose columns are } f_1, \ldots, f_m, \\
D &= \text{the $m$-by-$m$ diagonal matrix whose diagonal entries are } s_1, \ldots, s_m, \\
C &= \text{the $n$-by-$m$ matrix whose columns are } e_1, \ldots, e_m.
\end{aligned}
\]
Then we have \(Av = BDC^* v\) for all \(v \in V\). Therefore, \(A = BDC^*\). 
\end{proof}
\section{Norms of linear maps}
\begin{theorem}
Suppose $T \in \mathcal{L}(V,W)$. Let $s_1$ be the largest singular value of $T$. Then
\[
\|Tv\| \leq s_1 \|v\|
\]
for all $v \in V$.
\end{theorem}
\begin{proof}
Suppose \(s_1, s_2, ..., s_m\) are the singular values, including repetitions, in descending order. 
\end{proof}
\section{Approximation by linear maps with lower-dimensional range}

\section{Polar decomposition}

\section{Operators applied to Ellipsoids and Parallelepipeds}

\section{Volume via Singular Value}

\section{Properties of an operator as determined by its eigenvalues}

\newpage
\chapter{Operators on Complex Vector Spaces}
\section{Null spaces of powers of an operator}

\section{Generalized eigenvectors}

\section{Nilpotent operators}

\section{Generalized eigenspaces}

\section{Multiplicity of an eigenvalue}

\section{Block diagonal matrices}

\section{Square roots of operators}

\section{Jordan Form}

\section{Trace: A connection between matrices and operators}

\newpage
\chapter{Multilinear Algebra}
\section{Bilinear forms}

\section{Symmetric bilinear forms}

\section{Quadratic forms}

\section{Multilinear forms}

\section{Alternating multilinear forms}

\section{Permutations}

\newpage
\chapter{Determinants}
\section{Defining the determinant}

\section{Properties of determinants}

\newpage
\chapter{Tensor Products}
\section{Tensor product of two vector spaces}

\section{Tensor product of inner product spaces}

\section{Tensor product of multiple vector spaces}

\end{document}

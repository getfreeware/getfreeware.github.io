---
layout: default
title: Variable and Function Naming Convention
published: true
author: gro
comments: true
date: 2010-09-19 10:09:34
tags: [ ]
categories:
    - app
permalink: /2010/09/19/variable-and-function-naming-convention.html
---
source: http://faculty.ed.umuc.edu/~jrugg/policy/vrbl_naming_convention.htm

  1. Fundamental naming convention rules:

  * First and foremost, be consistent.
  * Always use self-describing names., i.e., slashIndex instead of j or nodeCount instead of cnt.
  * If you are going to use non-standard abbreviations in the your naming conventions, explain your abbreviations in the main program comment block.
  * Class names should be nouns unless you have a good reason for it not to be a noun.
  * Method or function names should be verbs or verb phrases to show the action the method / function is providing or performing. 
      * Function convertMilesToKilometers(ByVal dMiles as Double) as Double
      * double convertToKilometers(double dMiles);
      * Function convertMilesToKilometers(ByVal dMiles as Double) as Double
      * double convertMlesToKilometers(double dMiles);
For example:

  * Methods or functions returning a boolean type should generally start with verbs like, is, has, can or have, etc. 
      * bool isValidString(string strInput);
      * boolean hasAllAttributes();
      * bool canUpdate();
      * boolean haveAllDate();
For example:

  * Distinguish multiple words in a name either by separating the words with an underscore, i.e., number\_of\_words, or using Camel Case notation, i.e., numberOfWords. This applies to class as well as method, function and variable names.
  * Constant variable names should me in all capital letters and separate words in the name with the underscore, i.e., DEFAULT\_PRICE\_PER_POUND.
  * In the Java Naming Convention, class names always start with a capital letter and method names always start with a lower case letter. Again, I see nothing wrong with applying this to other languages as long as you are consistent.

  1. Hungarian Naming Convention

  * Over the years I have become a fan of the Hungarian Naming Convention. The combination of this convention, explained shortly plus self-describing variable names conveys more than just intended use for any variable, but also includes type and scope. This naming convention is independent of programming language. If used consistently throughout the program it will add tremendously to the readability and understandability of the code and even reduce the amount of commenting required because the names read as comments.   **NOTE**: just because I am explaining the Hungarian Naming Convention does not mean I am insisting on you using this naming convention. I will accept any naming convention as long as it following the fundamental rules listed above.
  * The implementation of the Hungarian Naming Convention I have settled into has three parts to a variable name: scope, type and usage. I use the format: scope_typeUsage. Where:
  * scope &#8211; scope of declaration of this variable 
      * global &#8211; g
      * class &#8211; m
      * local &#8211; no prefix
  * type &#8211; abbreviation of the type. Some common abbreviations are: 
      * bool or boolean &#8211; b
      * integer &#8211; n or i
      * unsigned integer &#8211; u
      * long &#8211; l
      * unsigned long &#8211; ul
      * float &#8211; f
      * double &#8211; d
      * string or String &#8211; str
      * char* &#8211; lpsz or lp
      * char[] &#8211; sz
      * DWORD &#8211; dw (DWORD is a typedef for an unsigned long)
      * any pointer &#8211; p
  * usage &#8211; a self-describing name using lower / upper case letters to combine words or even underscores (\_) to combine words. For example, nTotalCount or nTotal\_Count
  * For GUI components this can extended. Some common ones I use are:

>   * Label &#8211; lbl
>   * Checkbox &#8211; cb or chk
>   * Editbox &#8211; ed
>   * JTextBox or JTextArea- txt
>   * RichTextEdit &#8211; rtf
>   * Image &#8211; img
>   * Listbox &#8211; lb
>   * CAnyString &#8211; as or any (This is a home grown class of mine)

  * Name all controls and variables that have a natural association in a consistent manner. For example, if a Label, Checkbox, Image and an integer place holder are suppose work together at local scope than I would name them as follows to show the association and make your code easier to follow for both you and me. 
      * JLable for user input: lblUserInput
      * JComboBox listing possible input options: cbUserInput
      * JImage associated with the input dialog: imgUserInput
      * int for the actual converted input: nUserInput
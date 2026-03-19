# AI driven workflow to generate the paper

This document outlines how the paper titled "Financial Forecasting using the Chronos Time Series Foundation Models" was produced with AI.

There are three co-authors, Professor Sanjiv Das and two MS students, Tarang Goyal and Mohini Yadav. We all are at Santa Clara University. 

**Caveat**: The paper was informally begin in January, when Sanjiv outlined the work to the students on the back of an envelope. The students returned the completed code in a single Google Colab notebook in end February. We are assuming the "formal" process of the paper began here. The students used Gemini to help write the code. Then, the professor modified the code (to use a GPU and rerun the analyses). After that he used OpenAI Prism to write the paper, which took another few hours of interaction. Finally, a few hours were spent on editing. Detailed use of AI is explained below. Note that this caveat has been specifically added as the conference instructions are unclear as to the definition of what "formal" work means. 

## Detailed workflow step by step

1. Students are given an outline on the back of an envelope. 
2. Students prepare a Colab notebook using Gemini assistance. 
3. Professor updates the notebook, breaking it into separate notebooks, updating the code, also with some assistance of Gemini for coding. 
4. The results are now ready in the Colab notebooks, and comprise printed out tables (dataframes), plots, and also textual results. 
5. The LaTeX shell of the paper is set up in OpenAI Prism (https://openai.com/prism/). 
6. No sections are written but the blank sections are set up: Introduction, Methodology, Results, Concluding Discussion, each including subsections. So the outline is set up. 
7. Using the printed dataframes from Colab, these are put into Gemini and the prompt is to convert these to LaTeX tables. These are then cut and paste into the Results section. 
8. The figures are added to the project folder and LaTeX code to include the figures is added. 
9. Prism is then requested to write text into the Results section that explains the tables and figures, which it does and then editing is undertaken. Interestingly, the LLM behind Prism (GPT-5.2) infers results from the tables on its own and writes it up. 
10. The Chronos-1 and Chronos-2 papers are then uploaded to Gemini, along with some text from the Colab notebook that describes the experiments. Gemini is used to generate the Methodology section from this content, which is then copied over. 
11. A separate subsection on leakage is then added with provided reasoning, but allowing the LLM to write it. 
12. Next, the bibtex file generated from Zotero (https://www.zotero.org/) is uploaded. Prism is then prompted to generate a literature review from the bibtex as it pertains to the Methodology and Results sections. 
13. An earlier papers on the same topic that was already published is uploaded and Prism is prompted to generate the Introduction and update the literature review. 
14. Using the entire current paper as context, Prism generates the Conclusions. 
15. Prism is prompted to add an abstract. 
16. Finally, human editing via a few passes through the document is undertaken to improve the writing, reformat the paper layout, etc., using knowledge of LaTeX. 

Gemini was also asked to generate a referee report for the paper (review.pdf). This was then used to craft an outline of responses to the referee (responses.md) with the following prompt: “Please read the file ‘review.pdf‘ which is a referee report on the paper ‘chronos2.pdf‘ – then suggest changes and improvements to the paper in a document titled ‘response.md‘ that outlines the changes in response to cited sections of ‘review.pdf‘ as a response note to the review.”

The last item is an "extra" and was not prepared for the submission to the conference. 

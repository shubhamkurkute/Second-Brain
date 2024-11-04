## 4 Methods of Prompt Engineering.

1.  RAG(Retrieval Augmented Generation):                                                                                     Retriever provides the domain knowledge to the Generator in order to get the desired answer to the question asked by the user.  Retriever provides knowledge to LLM, retriever can be a direct database of the domain knowledge.!
	![[Pasted image 20241009163437.png]]

2.  COT(Chain of Thought):
	In this method break your big problem in to tasks and then ask the LLM and combine the answers to get whole answer. Rather being a descriptive break into small problem and be prescise.
	![[Pasted image 20241009163936.png]]

3.  ReACT: 
	In this approach if LLM doesn't have sufficient knowledge of the domain that is stored in your private database than the LLM should have the ability to access the knowledge stored inside the public database and combine together to give the desired result.
	
	![[Pasted image 20241009164512.png]]

4.  DSP(Directional stimulus prompting ):
	In this method ask specific questions to LLM. For example asking the weather for a specific region rather asking for entire world.
	![[Pasted image 20241009165136.png]]


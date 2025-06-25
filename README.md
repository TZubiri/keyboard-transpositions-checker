This project is two things.

1- First a little script that chatgpt vibe coded for me to test my keyboard and its timing precision when fast typing.
2- A Proof of Concept for LLM as source code. I am of the position that the "code" is now target code and not source code. My strongest source for this claim is Stallman's classical definition of Source Code which is the "preferred way to modify the program".

In this source code approach we:
1- Upload the conversation with ChatGPT as source code
2- Upload the relevant separate prompts that we believe are key to the generation of this program (Which coincidentally can also be used to generate a program by giving them as requirements to a programmer.
3- We do not upload the source code in the repo, rather we will attempt to upload it as a build artifact.

Limitations:

1- This doesn't apply very well to tab completed copilots, in that case it would be ideal for the uploaded code to be only the human written code, and the tab character to be explicityl used for completions.
2- Since we are using a consumer interface, and not an api, (first we have no guarantees that the code will not be used for training, so there's no IP protection, but also), we don't have much reproducibility, robust publishing should use API access and publish exact model with revision as well as seed (and even then we are not guaranteed reproducibility.

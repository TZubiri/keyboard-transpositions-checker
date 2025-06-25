# This project is two things.

- 1: First a little script that chatgpt vibe coded for me to test my keyboard and its timing precision when fast typing.
- 2: A Proof of Concept for LLM as source code. I am of the position that the "code" is now target code and not source code. My strongest source for this claim is Stallman's classical definition of Source Code which is the "preferred way to modify the program".
 
# In this source code approach we:

- 1: Upload the conversation with ChatGPT as source code
- 2: Upload the relevant separate prompts that we believe are key to the generation of this program (Which coincidentally can also be used to generate a program by giving them as requirements to a programmer.
- 3: We do not upload the source code in the repo, rather we will attempt to upload it as a build artifact.

# Limitations:

- 1: This doesn't apply very well to tab completed copilots, in that case it would be ideal for the uploaded code to be only the human written code, and the tab character to be explicityl used for completions.
- 2: Since we are using a consumer interface, and not an api, (first we have no guarantees that the code will not be used for training, so there's no IP protection, but also), we don't have much reproducibility, robust publishing should use API access and publish exact model with revision as well as seed (and even then we are not guaranteed reproducibility.


# Usage
- 1: Download python script from releases
- 2: Run python script with any python3 version, in linux
- 3: Type the keys "j", "h" and "g" in order, in a loop. The keys are chosen because of their central-right location in a loop, and the order is such that you can prone your wrist and hit the three keys in a single stroke. (If you are left handed I recommend switching the order of the keys in the source code, and maybe changing to "asd".
- 4: Press q to exit.

# Building

Two methods

- 1: Open the link in prompts.html and copy and paste the code as is
- 2: Take the input prompts from either prompts.html or prompts/*.txt and run them through your LLM of choice, with any modification you wish for.

Finally, run the resulting python script.

# Contributing

After building, add a new prompt to ask for changes to the LLM, within the context window of your LLM instance.
If you want to modify something yourself, you can upload a sed script or something that modifies the source code, but then you have to sync the LLM to make sure that the LLM has access to the new version (at least you need to do that if you want to weave in LLM changes and human changes). You can do this by either uploading a sed or similar script to the github. When building you can either pass the script to the LLM, or just pass them the whole new script as context.
Finally, if the context window gets too large, you can always use a new context window and ask for modifications on a clean slate, but this should be made obvious in the source code

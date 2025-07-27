<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Chat With Your Bot in the Terminal

**Project Link:** [View Project](http://learn.nextwork.org/projects/ai-rag-cloudshell)

**Author:** Abdulrahman Abdulkadir  
**Email:** abdabdulkadir62@gmail.com

---

## Interacting With My RAG Chatbot in the Terminal

![Image](http://learn.nextwork.org/confident_turquoise_quiet_hyena/uploads/ai-rag-cloudshell_1i2j3k4l)

---

## Introducing Today's Project!

In this project, I will build a chatbot using Amazon Bedrock that can answer questions based on information I upload. I'm doing this project to learn how to store data in S3, create a Knowledge Base, choose the right AI models, and interact with the chatbot through AWS CloudShell.


### Tools and concepts

The services I used were Amazon S3, Amazon Bedrock, OpenSearch Serverless, and AWS CloudShell. The key concepts I learnt included Retrieval Augmented Generation (RAG), knowledge bases, chunking, embeddings, vector stores, and how to interact with AI models using the AWS CLI.

### Project reflection

This project took me approximately 2 hours to complete. The most challenging part was configuring the Bedrock command with the correct Knowledge Base ID and model ARN. It was most rewarding to see the chatbot accurately respond to questions using information from my uploaded documents.

I did this project today to learn how to build a smart, project-based chatbot using Amazon Bedrock and AWS services. I wanted hands-on experience with RAG, knowledge bases, and AI model integration. Yes, this project met my goals—it helped me understand the full workflow and gave me a working chatbot that responds based on my own project data.

---

## Setting Up The Knowledge Base

To set up my Knowledge Base, I used S3 to store and organize the documents my chatbot will learn from. The documents I uploaded contain information about the AWS and AI projects I completed, including the services I used and the skills I gained.


I also created a Knowledge Base in Bedrock to enable my chatbot to retrieve accurate information from my uploaded documents and give responses based on my AWS and AI project experience.


My chatbot also needs access to two AI models, which were Titan Text Embeddings v2 and Llama 3.3 70B Instruct. I then synchronized the Knowledge Base so that Titan could process the documents into embeddings and Llama could generate accurate responses based on the retrieved content.


![Image](http://learn.nextwork.org/confident_turquoise_quiet_hyena/uploads/ai-rag-cloudshell_1u2v3w4x)

---

## Running CLI Commands in CloudShell

AWS CLI is a command-line tool that lets you manage AWS services and resources using text commands. To start testing CLI commands, I first opened CloudShell, which is a browser-based terminal provided by AWS that gives me quick access to the CLI without needing to install anything locally.


When I first ran a Bedrock command, I ran into an error because I needed to provide values for the Knowledge Base ID, the model ARN, and the region. These values are required so the command knows which resources to use for retrieval and generation.


While finding the parameters takes extra time, the advantage of using the CLI is that it gives you more control, faster testing, and the ability to automate tasks. It also helps you understand how AWS services work behind the scenes, which is valuable for troubleshooting and advanced configurations.


![Image](http://learn.nextwork.org/confident_turquoise_quiet_hyena/uploads/ai-rag-cloudshell_sdrgsert)

---

## Running Bedrock Commands

To find the required values, I had to look up my Knowledge Base ID and Model ARN in the Bedrock console. The Bedrock command ran successfully and showed me a generated response based on the information retrieved from my Knowledge Base, proving that everything was connected and working correctly.


The retrieve-and-generate command typically also outputs a lot of extra metadata along with the chatbot’s answer. To tidy up the terminal response, I added the `--query` parameter to display only the generated response, making it easier to read and focus on what the chatbot actually said.


![Image](http://learn.nextwork.org/confident_turquoise_quiet_hyena/uploads/ai-rag-cloudshell_1i2j3k4l)

---

## Extending Your Knowledge Base

In a project extension, I asked my Knowledge Base about “Why did the coffee go to the police?” I noticed it responded with “I don’t know the exact answer,” which makes sense because that question wasn’t related to the documents I uploaded. This showed that the chatbot relies on the Knowledge Base content for accurate answers.


To add new information to my Knowledge Base, I ran commands to upload updated documents to S3 and then re-synced the Knowledge Base so the new content could be processed. Compared to using the console, this process was faster and more flexible, especially for making quick updates through the CLI.


To validate the update worked, I ran another `retrieve-and-generate` command with a question related to the new content. The Knowledge Base successfully retrieved the updated information and the chatbot responded accurately, confirming that the update was processed correctly.


![Image](http://learn.nextwork.org/confident_turquoise_quiet_hyena/uploads/ai-rag-cloudshell_sm789ghi)

---

## Interacting with AI Models Directly

On top of chatting with my chatbot, I also interacted directly with an AI model via the terminal by using the `invoke-model` command in AWS CLI. This let me send a custom prompt straight to the Llama 3.3 70B model without using the Knowledge Base, helping me test how the model responds using only its built-in knowledge.


![Image](http://learn.nextwork.org/confident_turquoise_quiet_hyena/uploads/ai-rag-cloudshell_gregerg)

---

---

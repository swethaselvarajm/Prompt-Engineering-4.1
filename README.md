# Ex.No.4-Scenario-Based Report Development Utilizing Diverse Prompting Techniques
### DATE:                                                                            
### REGISTER NUMBER : 212222230155
### Aim: To design an AI-powered chatbot that assists customers in resolving issues related to product troubleshooting, order tracking, and general inquiries. The chatbot should handle various customer queries efficiently while maintaining a conversational and user-friendly tone. In this experiment, we will employ different prompt patterns to guide the development process of the chatbot, ranging from basic task-oriented prompts to more complex, persona-driven prompts. Case study 2 with Comparative Analysis Prompt, Universal Prompt, Structures Prompt Refinements and Prompt Size Limitations

### Explanation - Any one use case from Unit 5 and generate the report for that with the unit 2 Prompt type


## Scenario Overview
Company Name: ShopEase
Industry: E-Commerce
Customer Issues Addressed:

Product Troubleshooting: e.g., “My headphones won’t connect via Bluetooth.”

Order Tracking: e.g., “Where is my order #123456?”

General Inquiries: e.g., “What’s your return policy?”

The goal is to build a customer support chatbot using prompt engineering strategies that ensure effective, friendly, and efficient support.


### 1. Comparative Analysis Prompt
Implementation:
Multiple prompts were designed to handle the same customer query about product troubleshooting for Bluetooth headphones.
| Prompt                            | Content                                                                                                                                      | Result                                             |
| --------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- |
| **Prompt A – Technical Expert**   | "Act as a technical support expert. Guide users through fixing Bluetooth issues in electronic devices."                                      | Accurate but too formal.                           |
| **Prompt B – Friendly Assistant** | "You are a helpful assistant. A customer can’t connect their headphones to Bluetooth. Help them step-by-step in a casual and friendly tone." | High engagement, slightly less technical.          |
| **Prompt C – Empathetic Advisor** | "Act as a support rep who first acknowledges the customer’s frustration and then gently guides them to fix the issue."                       | Very positive emotional response, slightly longer. |

### Conclusion:
Prompt C had the highest customer satisfaction, especially for frustrated users.

Prompt B was efficient and conversational, great for average queries.

Prompt A worked best for highly technical users.

### Usage Strategy:
Dynamically switch prompts based on user sentiment and query complexity.

### 2. Universal Prompt
Prompt Used:
"You are ShopEase’s customer support bot. Help customers with product troubleshooting, track orders, or answer FAQs. Be concise, friendly, and clear."

Result in Action:
User: “Where’s my order #78910?”
Bot: “Thanks for asking! Let me check... Your order #78910 is in transit and expected to arrive tomorrow.”

Pros:
Easy to implement.

Covers a wide range of queries.

Good for small or early-stage platforms.

Cons:
Sometimes responds too generically.

Doesn’t adapt well to emotionally sensitive cases or complex troubleshooting.

### 3.Structured Prompt Refinement
Structure Example for ShopEase:
markdown
Copy code
[ROLE]: You are ShopEase’s AI customer assistant.
[TASK]: Help with:
 - Troubleshooting electronics.
 - Order status queries.
 - General policy questions.
[TONE]: Friendly, empathetic, and helpful.
[GUIDELINE]: Always greet the user and ask clarifying questions before providing a solution.
Response Sample:
User: “My blender isn’t working.”
Bot: “I’m sorry to hear that your blender isn’t working! Can you let me know if it powers on or makes any noise when plugged in?”

Benefits:
Ensures consistency across responses.

Easier for devs to update individual sections (tone, role, task).

Improves intent clarity.

Use in ShopEase:
Used as the foundation prompt, with variations for each task.

### 4. Prompt Size Limitations
Scenario:
A customer asked about a past product issue, tracked multiple orders, and also asked about a return — all in one chat. The prompt exceeded 1000 tokens.

Problems Faced:
Chatbot began to forget earlier order numbers.

Repeated clarification questions.

Delay in response generation.

Mitigation Steps:
Summarize previous turns into short notes: e.g., last_order = #456123 | product = headphones | issue = no sound

Use token budgeting: Limit examples to 2-shot instead of 5-shot.

Prioritize current user intent over full history.

Best Practice:
Split the chat into mini-sessions for long conversations, e.g.,
“Let’s finish troubleshooting your product first. After that, I’ll help with your return.”

### Comparative Summary
| Prompt Type           | Best For          | Benefits                   | Challenges        |
| --------------------- | ----------------- | -------------------------- | ----------------- |
| **Comparative**       | Scenario testing  | Reveals best tone and flow | Time-consuming    |
| **Universal**         | Basic use         | Simple to implement        | Not context-aware |
| **Structured**        | Multi-domain bots | Modular, consistent        | Requires setup    |
| **Size Optimization** | Long sessions     | Maintains performance      | Complex to manage |



### Conclusion
For ShopEase, the best performance came from a hybrid model:Structured Prompt Refinements ensured consistency.Comparative Prompting helped optimize tone and content per query type.Universal Prompt served as a fallback.Prompt Size Management was essential for high-traffic customer service.Future Directions Multilingual Support: Extend prompt structure for multilingual handling.Sentiment-Aware Prompt Switching: Detect customer frustration and dynamically switch to empathy-based prompts.Voice & Visual Support: Integrate voice commands and product images into troubleshooting prompts.







# Result: Thus the Prompts were exected succcessfully.

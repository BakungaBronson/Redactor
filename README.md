# Redactor
## Motivation
Stated in the terms and conditions of many (if not all) Large Language Model provider platforms is the caution against including sensitive data (secrets) in the prompts used with these models. Regardless of this, many individuals find it tiresome or even do not know about the caution altogether.
In both cases sensitive data is being put in the hands of various companies posing a potential threat to personal, company and even national security.
In a world where more and more non-technical persons start to use these models, dynamic detection systems will be needed.

## Solution
Redactor hopes to strike a balance between removing sensitive data from prompts before they reach the provider endpoints, and ensuring productivity remains high by not having users manually add back sensitive information for every prompt they send.
This project aims to do so by using an on device LLM of 1-3B parameters to identify potentially sensitive information, swapping out that information for a placeholder tag, sending the new prompt with placeholder tags and additional custom instructions to maintain the custom tags, and finally, to swap back in the sensitive information in the tags on receiving the output from the endpoint.
With this, we hope to reduce the amount of sensitive information being sent while giving administrators insights into what sort of sensitive information is more likely to be leaked. This will aid in future education around the topic.
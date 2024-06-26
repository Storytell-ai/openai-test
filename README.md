# OpenAI Hallucination Generator

This small program reads the BitCoin Whitepaper from Google Cloud Storage, and then uses OpenAI's GPT-4o to summarize the content of the file. The summarization returned is not about the whitepaper.

## Emails Returned

For the 30 examples I ran and committed, the emails returned were:

1. None
2. None
3. None
4. None
5. mark.wilson@example.com
6. None
7. will.smith@checkmate.com
9. None
10. john.omalley@catskillsvisitorcenter.org
11. porter@hotmail.com
12. julie.bolton@notarealemail.com
13. norah.matthews@example.com
14. john.smith@acmepharma.com
15. None
16. hcollman@imail.org
17. None
18. None
19. mojabnamiller@example.com
20. None
21. None
22. None
23. evan@meyer-llc.com
24. None
25. None
26. jessl@corporate.com
27. None
28. None
29. None
30. None

Example Output:

```
go run main.go

2024/06/13 11:33:37 read 984181 of 984181 bytes into buffer
2024/06/13 11:33:37 returned the file id "file-UAyDXeTT2zc2C2kRMjcCsjtm" from openai
(string) (len=7) "REQUEST"
(openai.ChatCompletionRequest) {
 Model: (string) (len=6) "gpt-4o",
 Messages: ([]openai.ChatCompletionMessage) (len=2 cap=2) {
  (openai.ChatCompletionMessage) {
   Role: (string) (len=6) "system",
   Content: (string) (len=70) "File to use to help answer the question: file-UAyDXeTT2zc2C2kRMjcCsjtm",
   MultiContent: ([]openai.ChatMessagePart) <nil>,
   Name: (string) (len=6) "system",
   FunctionCall: (*openai.FunctionCall)(<nil>),
   ToolCalls: ([]openai.ToolCall) <nil>,
   ToolCallID: (string) ""
  },
  (openai.ChatCompletionMessage) {
   Role: (string) (len=4) "user",
   Content: (string) (len=62) "Please summarize the file and tell me who uploaded it and when",
   MultiContent: ([]openai.ChatMessagePart) <nil>,
   Name: (string) (len=4) "user",
   FunctionCall: (*openai.FunctionCall)(<nil>),
   ToolCalls: ([]openai.ToolCall) <nil>,
   ToolCallID: (string) ""
  }
 },
 MaxTokens: (int) 0,
 Temperature: (float32) 0,
 TopP: (float32) 0,
 N: (int) 0,
 Stream: (bool) true,
 Stop: ([]string) <nil>,
 PresencePenalty: (float32) 0,
 ResponseFormat: (*openai.ChatCompletionResponseFormat)(<nil>),
 Seed: (*int)(<nil>),
 FrequencyPenalty: (float32) 0,
 LogitBias: (map[string]int) <nil>,
 LogProbs: (bool) false,
 TopLogProbs: (int) 0,
 User: (string) (len=11) "bruce-wayne",
 Functions: ([]openai.FunctionDefinition) <nil>,
 FunctionCall: (interface {}) <nil>,
 Tools: ([]openai.Tool) <nil>,
 ToolChoice: (interface {}) <nil>,
 StreamOptions: (*openai.StreamOptions)(<nil>)
}
(string) (len=8) "RESPONSE"
(openai.ChatCompletionRequest) {
 Model: (string) (len=6) "gpt-4o",
 Messages: ([]openai.ChatCompletionMessage) (len=2 cap=2) {
  (openai.ChatCompletionMessage) {
   Role: (string) (len=6) "system",
   Content: (string) (len=70) "File to use to help answer the question: file-UAyDXeTT2zc2C2kRMjcCsjtm",
   MultiContent: ([]openai.ChatMessagePart) <nil>,
   Name: (string) (len=6) "system",
   FunctionCall: (*openai.FunctionCall)(<nil>),
   ToolCalls: ([]openai.ToolCall) <nil>,
   ToolCallID: (string) ""
  },
  (openai.ChatCompletionMessage) {
   Role: (string) (len=4) "user",
   Content: (string) (len=62) "Please summarize the file and tell me who uploaded it and when",
   MultiContent: ([]openai.ChatMessagePart) <nil>,
   Name: (string) (len=4) "user",
   FunctionCall: (*openai.FunctionCall)(<nil>),
   ToolCalls: ([]openai.ToolCall) <nil>,
   ToolCallID: (string) ""
  }
 },
 MaxTokens: (int) 0,
 Temperature: (float32) 0,
 TopP: (float32) 0,
 N: (int) 0,
 Stream: (bool) true,
 Stop: ([]string) <nil>,
 PresencePenalty: (float32) 0,
 ResponseFormat: (*openai.ChatCompletionResponseFormat)(<nil>),
 Seed: (*int)(<nil>),
 FrequencyPenalty: (float32) 0,
 LogitBias: (map[string]int) <nil>,
 LogProbs: (bool) false,
 TopLogProbs: (int) 0,
 User: (string) (len=11) "bruce-wayne",
 Functions: ([]openai.FunctionDefinition) <nil>,
 FunctionCall: (interface {}) <nil>,
 Tools: ([]openai.Tool) <nil>,
 ToolChoice: (interface {}) <nil>,
 StreamOptions: (*openai.StreamOptions)(<nil>)
}
2024/06/13 11:33:40 The final output was: The file titled “SRK_2018_Brochure.pdf” is a brochure for Shree Renuka Kumaraswamy (SRK) Institute of Technology, Tumkur, published in 2018. It provides detailed information about the institute’s vision, mission, facilities, academic departments, courses offered, admission process, and extracurricular activities. The brochure highlights the institute’s commitment to providing quality education and fostering holistic development among students.

The file was uploaded by user “UAyDXeTT2zc2C2kRMjcCsjtm” but the exact upload date is not provided in the metadata.
2024/06/13 11:33:40 done
```

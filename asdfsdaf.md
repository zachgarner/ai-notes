
asdfasdff


![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b43cf791-1dbc-4979-b9cb-2f11d884b35d/4b468309-a916-403f-abd7-677b80e3ddb5/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB4663Q4WU2MH%2F20250918%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250918T162131Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEEcaCXVzLXdlc3QtMiJIMEYCIQCT0s%2BQJCCkwOKssNUWy17md1%2BZF0K0VNkHiL6Dm3ervgIhAOtRYNkjnMdtPtybp4hH9uXxn5Doixa41%2Bf0awmEDN6gKogECMD%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEQABoMNjM3NDIzMTgzODA1IgxCMvRc8fx4X6KTOvsq3AP3ySXPatyLmf19MPrSngnflLV9DCnt%2BVzlsTs2ijLmV92gMi3D%2FNIQ3JdUkrUmBcB1J%2B%2FvF2%2Bjz72rbl6vmS35k7b4tslnzp35T8%2BwzCKPobWZGnGAcZsEnO31%2BzKiNFMHkemnm6G79DvvMjNVllzEqHqJ3O66NwsmSarvuTxDiQVrjZv7BoMq%2BLJkdCtlxdDtY8hQbA7IVm9bX8tizMDZJ%2BnqcuFW%2BtTXOJMtyqfKyFOrxHxFrvIGvmO0639Kz9oUXq82DB2EQOLhbZLFAE0NQXUUcEdSoS206bOAgvaek%2Bzv08v71DViDfSxYiyn62rTNis8bQx3tXIMHySroktaXbkE%2Babj4vnQ5ot8yZcvKAJNLjWE6VVhX9znzR8oEpDJuIMydmMa%2FJq%2BBpgNaG1XE8syKdQIgio03sXGrd4%2BL%2F%2Ffmf1f6LlDrzol%2FsiJ2jz7xPJcnM8go%2BIGvsJ362%2Ff9i8bhuvVJkbMXsVa2jw%2BEW2MLEuEm9638nt8RXIuOQaeH1ZrDRAJ24BP6i7r0udox8p8eU%2BC0E7jzZN4lsSCaZwYVUE6Upm5PhTP%2FmhjmYvEzFZqLs57%2FwT22llKCcyw6JcLDmB2wZpkUC1%2BzdRhlGiuR422fFItyQyD5DCQr7DGBjqkAVpKP5v2mf%2FVa5SeNEVFSAZudKh7dHFh6eJC06bcShJInv3KhK%2BFs%2BtPt0wt2x7lXl4eCkxN9sgTNbDH12FU5IB3XaJUavPtQA8k5Ptapw6I%2BP%2F%2FUpM%2B5e8DveIVO3sQPmC0bOELaIHcMUBBSCTpxuQrGqs2OTYIi3DTw6TlIbEZTvh%2FjeWsHqIIMNtfbB3QIeVMePaDcS6erHyrlB7rJCgGSUUF&X-Amz-Signature=436fad357bd0d1050bafdd37215ae2cd003de9f1731ea3165a0911d931df6d00&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)


# Open Source


The main large open source foundation models to pay attention to are: Llama, **Qwen**, Deep Seek, GPT-OSS

- Qwen & DeepSeek score well on current livebench (~70), while Llama 4 and GPT-OSS fall far behind (47)
- GPT-OSS is OpenAI’s open source model based on GPT. The performance is good - but I suspect the company doesn’t stand behind it’s open source contributions and would adopt with some hesitation

# Proprietary

- OpenAI’s GPT models - top tier, leader of the industry.
- Anthropic’s Claude models - just below OpenAI’s GPT, but far more expensive
- Third teir is:
    - X’s Grok - scoring 72.11 on livebench, followed by Gemini 2.5 Pro Max Thinking (70.95) and the open source Qwen 3 235B Thinking (70.76), DeepSeek v3.1 Thinking (70.75)
- Llama 4 has failed to keep up. LiveB ench score of 47.78
- 

| Model                    | LiveBench (General) | Price                                  |
| ------------------------ | ------------------- | -------------------------------------- |
| Claude Opus 4.1 Thinking | 73.48               | Input: $15/million
Output: $75/million |
| GPT 5 High               | 78.59               | Input: $1.25/mil
Output: $10/mil       |

- So at surface level GPT-5 is 10x cheaper yet top tier performance vs Anthropic. However, GPT 5 High uses significantly more tokens, so the actual cost difference will require analysis

# Benchmarks

- LiveBench is the most reliable benchmark board. [https://livebench.ai/#/](https://livebench.ai/#/)

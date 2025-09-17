
asdfasdff


![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b43cf791-1dbc-4979-b9cb-2f11d884b35d/4b468309-a916-403f-abd7-677b80e3ddb5/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466RX5XWSU6%2F20250917%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250917T123858Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjECwaCXVzLXdlc3QtMiJGMEQCIGTG4EKdBneKaCJ%2F5PBJoqcAa6k%2FdBUYjAR3Fm9IfwhfAiBSl9DKqkFabzdFl01DVMeVp%2FJSwlZ7xelAYal%2FZUvvdSqIBAil%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F8BEAAaDDYzNzQyMzE4MzgwNSIM9r9KViiB6KR2MUY0KtwDDFZ5CaslCWTddz7YoDDbFEuPh%2FPTZ2GeGVQi8Oq4RpBfNfW0exGdeGqVYFZopeCuN9WevflIdcIHEDpJd3Ooa9WQM67NK8eam2jbVK2p6rXxL5meZBdgCDZ6Ob%2BxMjGqVehH7S6FR%2Bz4ypr9S%2FTMfsWWClo2fJJyFK%2FnuKTQy2J76STkUnLrtSIu%2BaRYLmtOvRuIicc3xITcgr9%2B3xyeZlSN0zDg%2BM8kR1lJm3u4BBKyj1PNcBrw2%2FpwGsU9%2F3JB9q47EEjj8F7RbM6fppQ59iafLlaPk3RufLRODx%2BAXB5LoP3kKMcfqTXo9AFLg%2Fp%2F2nAUPT1JI95cWtvueD1skhFbhbSYQFGkacPGFQTjtXS%2FkJQtNSQs6uH8PTM5C9QRHa2cF0S8XBYGnrM6uoYYMeLBA6PVdmd5DMUk3cZCW9Ru8ECfoKyY16nePAbX9ZQaL7wYPedwQgQxiKRko1bZjYxsslUBQUdL5XNIp6eUsNjAb30PYR9x6Pl1SEHDjJp3RkuSYYFXR%2BNTy1tcC1IKbY4gTIzmTV1I3sREAgTsD0%2BUHAAhZ%2B7QLY8OEXRM3fCIVFiyjumUhHH2xH2kWrJnfMEHMJuSzK76ejmST4U59MIGWSnO%2BMSn6OomkQQwwsuqxgY6pgFAtnRxBy26Q9%2BYiwwSWjiUtIO8FXJzNmat4nZ39WyviqQcsy4dE1OqsVsnuqfk0oOqLV8c5zIo5CSRhtycdV0EoAW6amk6ElfgbnAtBJj23Dfs1rtvDMK3tsdDf3tlY005Fwrg6dLE4C0V1IVL4HM1ETaF1D59cNqLRHrCAY5sEwQ3PwBLpptNUsRkC5Xr6zJZWD9CwKcucZDz25xQbGrFCDAIymjR&X-Amz-Signature=002deda4d769472af54b063d7f876032419652898da6fffb48389753c09e0985&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)


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

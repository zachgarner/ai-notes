
References


Primary Reference

- Platform Documentation: [https://platform.openai.com/docs](https://platform.openai.com/docs/overview)
- Cookbook [https://cookbook.openai.com/](https://cookbook.openai.com/)
    - This is updated in blog format, but you need to scroll down the page
- Research Blog [https://openai.com/research/index/](https://openai.com/research/index/)

Notable Documents

- [https://cookbook.openai.com/examples/how_to_use_guardrails](https://cookbook.openai.com/examples/how_to_use_guardrails)
- [https://cookbook.openai.com/examples/developing_hallucination_guardrails](https://cookbook.openai.com/examples/developing_hallucination_guardrails)
- [https://cookbook.openai.com/examples/gpt-5/gpt-5_prompting_guide](https://cookbook.openai.com/examples/gpt-5/gpt-5_prompting_guide)

API & Platform

- **Tool Support:** GPT-5 supports MCP, Web Search, Image Generation, Code Interpreter (Sandboxed Python), File Reader (pdf, word, ppt, spreadsheets, text).
    - ‘Computer Use’ is anticipated
- **Pricing:** GPT-5 is ~5x the price of GPT-5 mini, which is ~5x the price of GPT-5 nano

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b43cf791-1dbc-4979-b9cb-2f11d884b35d/adaf8d23-d5f2-4898-83b5-d7e26746ef69/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466SRKQL6PX%2F20250916%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250916T211153Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEB0aCXVzLXdlc3QtMiJHMEUCIB2q%2B780z1LmutY112pwcqRLx96edOccw1W9DELe9qffAiEA%2FkrGHPdS86xKS4UsqhcNU%2FPRB%2BBbdzhThdipaimKZwkqiAQIlv%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARAAGgw2Mzc0MjMxODM4MDUiDHYgcxniSLQVqPh%2BxCrcAyE9NdpBdYVfJkAR0npMQhHa6a%2BPr2C8Q6jOJO9fREfclnjVstUZEvspf5BjgKnfx9eI0NzcKRQAUzqlQbtD88KoP9yAE224zVrVDiyQbf9tA4ajtIRCrBR0SLslln8sgjbpnyXLBLCY1re8fV%2BgmFbQsZ9WpI35BKIXn4YUUgm7vDzNydqABjSyPyqMBE4Oj0pOLm9Jc2fqulWnw%2BnA0JlJAK6xMxBCTB7bjH0ZFPGT0gmTJKfZE0tJIHLOhorslcSCqIqKByLk0EKxpmSGBrFQJUwmo%2F%2Fk1EI3SBhu5DQjeaax0r2oRgAWqQoKbqtyzVsBNPcq%2BW1%2FjevflXP1W6TNX7FqLllakoo43Ifj9MLgItIPHThuCF6yuaURzSBSzpMPeawxBTeJ2XBiZpXIBWZn8ma84oZrIqu9o29h16WMgIHdztadx4bapQB6B79mOiO9YYAePtEO9%2BEDZoHTV%2BgcjC5mbyZXja3tMWrQlwvNUmiXuvekSFvABfi4CUhBk2KxmyDsxwL9iPtq5IDzHJ3ksLc1Y0YadN7Zxd2CDwjSwN6gPG3YI9%2FdzZ7RRLEvyhx6i4uQNa4NHYLXRM4zX%2Bh6R1LuwMV13HraRD8goOgPw%2BTDnVqvi3Zbq3gmMMuWp8YGOqUBzY%2BveSdlfl7nXjOnvbEkzrzTa0nsZhyHIFvXIKuX%2FTHHLTlmwiwl8iDmdvVXBwCQvwyCVOtTuOpsP6pzmnHA%2B%2BwFK0oFUxNSUh8AamK%2BNFcM0z2aYuMcRm%2F8ANaWGRBwtVGrvXsC2rI8TwvolbY1noYvz8HPpLha2Csn6qJDV7Jrkq5pRMELiuiDM5ibWiYJ4mrqDDncE12FR9rOx4HxHOtfMDdJ&X-Amz-Signature=343d838be307fa9ef7672eb114f787f67839178919b68256c2dcf438807ea9cf&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

- **API Overview**
    - The **Real Time** api supports Text, Audio and Image endpoints
    - There is a separate **Image Generation API**, and I dont know how it differs from the Real Time Image generation endpoint.
    - **Responses** is new, extending the functionality of Chat Completions API and the Assistance API. Unlike the stateless Chat Completions API, Responses has the ability to remember previous responses, supporting multi-turn chain-of-thought.
        - The Assistance API is now depricated
        - I imagine the Chat Completions API will remain due to how widely adopted it is
    - The new Responses API simply looks like:

        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b43cf791-1dbc-4979-b9cb-2f11d884b35d/9e7fe051-d452-44a6-ac6d-7c52740a07cb/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466TXCQLBDD%2F20250916%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250916T211158Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEB0aCXVzLXdlc3QtMiJHMEUCIApJevuAa7Cm6JiaId4oQQDS%2FcOGRwR2QoWj1vkmZz8YAiEA07YsOPSE1WWpU3vat2Tz1d%2B%2FRcOzxwbkyr5gkvhM12sqiAQIlv%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARAAGgw2Mzc0MjMxODM4MDUiDHX1CFrpqnUUonYYjircA1gZ6773zzOZi34QVH%2FdkYpt4rB6ZtKSDU5Tz%2BoEqyKtJ6xyZdZh0Mzha8%2BYJe3kcCM%2FoPIeDA4IcE3wpEuuveZ3XZlEcRQRRHtL6vhTYQL7SI4iYv38%2FkNcRdYFv%2FH5nfVdETFxwxNWB9T1orJvrd1rgIH8RyiwqvPaC%2BgHGHPSGDmrB4a5FUaNFC8ZPIfZsHchPD2egald7hOQPxj2adI8DGq8Uj7PJKMeWSsm%2FnXYBaYcAObDcNrAm8cDdR6Tjy%2BEiE0DkjYTa1jvDZUJ38uYQd2MVu6h4CR8dgVpNwNp4ZRSosBXhml8QMktI9Y3tTsgzv6f%2B0Bkm9AzGoZELdBY1IvCNN4Pj1gzlHGqxIgqboL5Lrw%2BzjGTULm8lV%2F%2Fl2YihBpbiuticph%2F%2Faz4ys8MUMXgDkyPEFOgySVjXkdSFpcJ4xL%2Bxuro%2FXgOnimmsMEU%2BzrIIY8Ixnk85Gw2vakFPswLMH5olNoX54waU91YR62%2FPHofNddM%2B7ypBiTvi9w5LZSDVOxjV%2FagFnJyPDkm8i23mHqYHZAZzFrlcbWI8jxEBpeZmAoMk3ZiBOxqbxYSSOC6dPh3N45xOa%2F9vnBF2501P4bB3AiOmhvp5mSZf0kmbTvssO9LpjXwMKWXp8YGOqUB6woQ6A3PfjV72mv4oadam1gYU1WXC7E2I%2FkuxkZTk1ULBBh5twjVonBcs3DjmnPYq%2BNM5v6%2BOANVhCE1CKVE%2BEfqALQ5QiuSUoeZHoULkGRr0cmcM6kh9YSbqxJEfG0OAHQ09%2Bk4Ia%2BkJ8W526DRASEuEcde2D9TjaxlSIfYjECVwTlv46JsZ2FgLucFXQfiFc8cA5Rred59SyKb5letlia7%2Bhsu&X-Amz-Signature=005d7aab9a489f4414d83781905f38c5c00f59ab7e04bb9ad95a6b125b3d8d7a&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)


    Projects, etc

    - Codex - agentic code development
        - [Agents.MD](http://agents.md/) - not sure if this is from OpenAI but used in Codex
    - GPT-OSS - their open source LLM
        - It sucks, but it sucks about as much as Llama 4
    - The [OpenAI Model Spec,](https://model-spec.openai.com/) which is used in some mysterious way to govern how ChatGPT works is an amazing piece of _philosophy_. This document encodes OpenAI’s values. However it’s really unclear to me how this is actually implemented in the system.

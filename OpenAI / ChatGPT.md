
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

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b43cf791-1dbc-4979-b9cb-2f11d884b35d/adaf8d23-d5f2-4898-83b5-d7e26746ef69/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB4663WNMY62O%2F20250917%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250917T123405Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjECwaCXVzLXdlc3QtMiJIMEYCIQDLQWHR5OgO%2F%2Bkr%2F%2FPkXh6of8QU6FQyaTNT1BjB86%2FSsQIhAIdiCzWYqRSZp5lHVgxM5Udg0iC2xUcwNnHfzJd1b3FsKogECKX%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEQABoMNjM3NDIzMTgzODA1IgxM4MOsThD8SlY829Eq3AMp06Gb%2BPaxteo12geGIsrz0XdKmGewnb6mso77qcq5gkxFuXRy4UyZasMrzoxgUn%2FhNhEkhEDOh39Rt%2BA5eUm4I8OtduyazmvuEuB7ACFadtDnSbAC9PoN1%2BIf8vv9mn%2BO0S2qrw14GtveEF9pQ9%2BcH9NriN4q%2BtkIdW1eR4VFfIAunNFDLLRsTDkttjLUcYrNJDzbymxx29bXGg0UoLT%2FmE9r2vdDUb3kXwGy6H5nixwRCbvz2jEPIdE2iXh26BPxJOS%2BKaNdJSdTiDTaThsgZG8lfsUp38S5pp5%2Fk7PJtAevZMxGMqtFbp5W6V8%2BrQGtOBuxnTkXFjrtDzw1EbKgsjqOhtkRgDwkUJstBfrXQjagiik6EbWyZd%2BitBF7UqyEsjy4pAEpuvWFNgoOdlvgtAUQmnWclNrOsqJDXB6jMBMcrgfP9SehHvS6RPrbpASqohQqgtp0%2BUznD3uN4h1iQBrgWxYHtf4V54TzL8F7TyjUTWvPhiBmClLAyGJCEj1D8Fa0kXUfoHj4CchhOs6BVfdi2qWrV%2BaHqG7YdYnwiK8T0g5CQEv822DXyG6C04Q8Vsm1W4nCj5KdDQOMBDINsDkn%2BeCmTdJLVH3x53wYeNogm1TJMiilwY46WjDkyarGBjqkAQ6vtpOxSqyz24Vux9VWkXFkxfnUKLbaJdZ54Sj%2BpKEb6uGkyxpeZwOfqWXLnZvEQdxrPAGAPJlTRaa8uv6ZMnkN0MRQBDMliri1cPuUpydz4KHnpLP%2FbQqSOa3JddyXxlqSJjOTlrWtYkmqGePDa30JLIyj75SstPavGTGZORITVlq3fQhOWIcjJFdvzVPuJkbg51n5vBerLi2sOSvNfZQFGMSb&X-Amz-Signature=b671468aec13200416685fce31c2b3e2b998ab0548bc2b1b60593d66b5130464&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

- **API Overview**
    - The **Real Time** api supports Text, Audio and Image endpoints
    - There is a separate **Image Generation API**, and I dont know how it differs from the Real Time Image generation endpoint.
    - **Responses** is new, extending the functionality of Chat Completions API and the Assistance API. Unlike the stateless Chat Completions API, Responses has the ability to remember previous responses, supporting multi-turn chain-of-thought.
        - The Assistance API is now depricated
        - I imagine the Chat Completions API will remain due to how widely adopted it is
    - The new Responses API simply looks like:

        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b43cf791-1dbc-4979-b9cb-2f11d884b35d/9e7fe051-d452-44a6-ac6d-7c52740a07cb/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466UFZRGZHP%2F20250917%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250917T123409Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjECwaCXVzLXdlc3QtMiJHMEUCIQD3gOh1atEMZb2hinGZQMCidzzpaqC6ECC6JHzN0aTTXAIgX9FBmjReor19gCNHQw5gFcZ95n1hSDyLeGFoY0oDop4qiAQIpf%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARAAGgw2Mzc0MjMxODM4MDUiDBgsaOtO3NYfb06nAyrcA0Gbz9j3DxW6gtv1DFRQB7jeBxD%2Bb2t9st3PGHAcqNjc1fiNGikoZqtu193CWpQlyAtputCpbpgz0jPvPyO5wWojRNMESxrkYeVw%2FuebCqkHr2hss%2Ba9W0ShBdETja9QPZktZqJTiYfS5UJJVy56qKQutp3AWXPFwxXXpRYxYaDAoJbZYm6WKWX66x0143q4llKsqZWhWfpu0nwWPGEc6eXkptND11hlU57lLX%2ByRfeWohG5Dix3GrdBr0K5d9ekWSSKiZUwUHafBoz99mDEYa85BNygQEHTIdGUIybfapdOQofyMw4T45SqKoqs6UIHD4s66mEJzmgtXGcJtCEFL63nMS9indsdV4Y3RyF%2B4BYm3j6CfOPqhQiSp6c8cpSa%2FX9T28RoEsngGPK1FfUI5kL3HGQC9N1T8P%2FkUafUdZ7SrgAFMTQI1YWhBKOSmtWqJVaod5XF3MZpf%2BWO5t4osGVRMn7cdBzqmR62xBgTHzkGlV1IJgKCO%2BXQZ3EJ58xKPvX0JVwyCB3ALX6IUPvErblOVwp7XreeaIkEz5K%2BEdrIg%2FPKyBQ7hTeVVSd5FC8LaziVcJv7tGLBahEZYANSDoBuWa5%2Bd3vQgwqWuIZNrgHQ8zd3M%2FG2MwAx%2BMNzMObJqsYGOqUBHcBCna89I5t2bGWO9DDLdo8bVeZojAEzASqMtEd0CmyZHfh81EMQj0kuPY14ivhBvaTA%2Fq3skmWtcUm25kbqgAf%2BPiPrhd6m4CkTMt5nRyPTD0zn1rCJ0IyfeHQ6ILYw4Q%2FqfQC2bL71kat0ZP0G%2B0%2FnQ3AagKULSdbUFXhuwbBdd2aZg%2BRKk4GSfRz%2BsGSXtLnAgVacfIJRxX%2FU8ip6XI5NXtI2&X-Amz-Signature=7b98a0b48504bf756a8b39d35d6fa7ad8324c7fc2e1310623d8f9001a89a40f6&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)


    Projects, etc

    - Codex - agentic code development
        - [Agents.MD](http://agents.md/) - not sure if this is from OpenAI but used in Codex
    - GPT-OSS - their open source LLM
        - It sucks, but it sucks about as much as Llama 4
    - The [OpenAI Model Spec,](https://model-spec.openai.com/) which is used in some mysterious way to govern how ChatGPT works is an amazing piece of _philosophy_. This document encodes OpenAI’s values. However it’s really unclear to me how this is actually implemented in the system.

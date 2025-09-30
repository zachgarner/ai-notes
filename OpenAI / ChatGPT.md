
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

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b43cf791-1dbc-4979-b9cb-2f11d884b35d/adaf8d23-d5f2-4898-83b5-d7e26746ef69/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466TQ4JZ7VU%2F20250930%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250930T144857Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEGYaCXVzLXdlc3QtMiJIMEYCIQDxO1n5nBrTv30vjmKVWm6A3OyVWwCyCdmBuT7p3iY%2FWQIhAOWfcYR6rAQVrWXxV92c0eA4YwBd1%2BYA13QTa7%2FoCEZNKogECO%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEQABoMNjM3NDIzMTgzODA1IgwI4bnPUHNmA8TGNlQq3AMvW9z9sTGUJw02wwknUSA4Q4zbKZuoLCHi5EAkRGNHWi4EKlaCfHZ9PhymYBzqfzvsIV8Spr4dvAVQt7rzaWexFQz5LNhJnz8jkYPfnBWWbU9qWct1hY0IlLLT1WB1xo8dUnOPiykBmqU1f%2BcFR3wdEgMKFXoCicvwI1CKUyjpAPYgztayzeRHEsE2IMSZA5xExrLy79cziS90BLZDHuHeq02wTx8p%2FBy0qeIkeCqKvFial%2F6CPQF3dvoAClRcENc4RGhzKe9uao6fgPbb4OJr162isGJeOYKvePJ1Fk0BC%2BMMv1xWjTYJzeXCJCrvVX3XmHssdVX9D2tQJmVrBP6ALjOEZ1CBV2AEumUI%2B6WigjxCA54HJdY5vm7P%2F1aPAyMTOq12lkhUDWRAkuKbPCCyeQ3iwFh9FEkRqQXeHg4a%2FaYTVnX7fXZOMzprNkFVQvMKMsKLtTOxOmAOHPogcQkGR0xoc%2BXmRiEFE%2BIelgvr%2FBOPeyah50ggt7h3XYkuUV9uQqUqhai1yme6Rv66QKyQuejuJQNRRX1shPaJQpw8YZfyDKn2o6Po%2FhfXdj%2BzOmXqYs4ZR0sVtL9xxg4PV4X4q9vaCnYXSovvEms3g0eywUaZ5exLNivs5atTgzCayu%2FGBjqkAc6pwEr%2BzP0Bc3Q9WLsUPo%2BPWIW6n%2BeEdby%2Fh34fo1E6IGrIPZdaXh9lmFsVk5EC%2FmkyV7DG880R2lOAYJj7XbAVewTEIle1skwvakGN4lf57OvpJ8W2J3R9awcifJIZBowHxsabs6RK9AJK1InAHPCh2Psw1zBRUcfjfmIhehT0zD7W9ghtUPQj2fpOTg4hp1o3DZiQLPvF6lANgc9ahALbDBnx&X-Amz-Signature=569548276a2c9874bbce62fcc00cd6fa20f720e56f11447c6cb950b8250a3f59&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

- **API Overview**
    - The **Real Time** api supports Text, Audio and Image endpoints
    - There is a separate **Image Generation API**, and I dont know how it differs from the Real Time Image generation endpoint.
    - **Responses** is new, extending the functionality of Chat Completions API and the Assistance API. Unlike the stateless Chat Completions API, Responses has the ability to remember previous responses, supporting multi-turn chain-of-thought.
        - The Assistance API is now depricated
        - I imagine the Chat Completions API will remain due to how widely adopted it is
    - The new Responses API simply looks like:

        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b43cf791-1dbc-4979-b9cb-2f11d884b35d/9e7fe051-d452-44a6-ac6d-7c52740a07cb/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466YL6RE4XI%2F20250930%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250930T144859Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEGYaCXVzLXdlc3QtMiJHMEUCICclyjmb%2FW8%2B6fS2aHqxuf%2Bf%2BOwsnhblGBTEZeC9bGRmAiEA1ccU66XhhKsMybpmONlcpl621mn5ycgp%2Fj1LFik88a8qiAQI7%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARAAGgw2Mzc0MjMxODM4MDUiDDU%2FeJu5BX6v0Sw%2BoircA8zgde%2FxVe1Q0gVYohU0oMm8uYUjK2SQu5cFf4rcPhQdLNgqoxRTH8modLfVCW0dAIigBBRI9hmyVjMMduIjtVPILmX58T1fqTQIr%2B%2FrA4SS5lbgsCRGWO%2FiZVubq%2B1B05UGC05U21vg%2B16ytFpcBmRQPXKz9hp6lypvEd7cI9I7fH6TFljLsgocfDZ2fmX6zr%2FgzKjxQFp%2BuBfDtdZ6Rw65NNTdEYYKq4G61WJEf%2BWTog%2F%2BiQWcs3zuNte0r2oPqMyFY0VTlFjEmt8YFW5LFYrcRCJn7WV29%2FcO1KEXdbkb75AT1Ldd3doGGXq3Wu2oW05ehaFWeGiZI3jutmeEwT%2BaCBRAt1l2xGGuUjQIyiQ3HCBW%2BO2jqLgR00TAxWvrJS7s3p%2BNpwWRB1okpbS5skPSLTU70teTjiEBNglVJmDDDWMzCz0frwQrPEzOxu7ETvYZkYuHe%2FkdrAMl7mcaDzAIfGTiyoqaLodN98x7SfCnUg2XGOovyL35NXjNn5glPQTzSH7ru6lZCBSQ6KEqwlh4ynNNFOABkCDcjgAtJDnwx%2BwAK19B0Qurv%2B88JggaBlFwMtATI8bmkbqc4HNdaGCg4%2Bw7mvfpReaSmynzFt3io0pShyvGrmZHDCx6MOfI78YGOqUBJuPqj%2BJ7BUiKnS%2FL%2FbD80kfFxlaY3G0mqVqvwwVzBoDciif9BZ2x38H8P915WhPZRAQSOyGr09ukbwqzl%2B%2FnYosZ5%2F7pL8iS3SvKsyJRawJL9W8OeqdTAxiCWTBkbCKJKXPvIYzGwJpLrRGyLQV17rxaI3Md2Ur49D2HWoWRCWVYJK4cQN6a%2BOZKFoa794TqHWcVbk45hk7bEslz%2B1i%2FCfMjDYaF&X-Amz-Signature=9f8f49ac24527d6091e2611c2ca77e5094662f3aee5f049f8f81ab032b937971&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)


    Projects, etc

    - Codex - agentic code development
        - [Agents.MD](http://agents.md/) - not sure if this is from OpenAI but used in Codex
    - GPT-OSS - their open source LLM
        - It sucks, but it sucks about as much as Llama 4
    - The [OpenAI Model Spec,](https://model-spec.openai.com/) which is used in some mysterious way to govern how ChatGPT works is an amazing piece of _philosophy_. This document encodes OpenAI’s values. However it’s really unclear to me how this is actually implemented in the system.

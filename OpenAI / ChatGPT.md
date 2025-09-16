
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

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b43cf791-1dbc-4979-b9cb-2f11d884b35d/adaf8d23-d5f2-4898-83b5-d7e26746ef69/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466UGTHD7LR%2F20250916%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250916T213057Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEB0aCXVzLXdlc3QtMiJIMEYCIQCDB1%2FXmvJ9%2FpPJLVbx39kAw%2BhV2DJvgkKE0OwtGLKtsQIhANyIe5LxzbmTyZY4m7STaHdEtBcZd9iJRT2lQsxzPZntKogECJb%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEQABoMNjM3NDIzMTgzODA1Igw9Z2k1NydkoUZiTtgq3AOuGvpxjYfBT9Lqpg8yfuz2PLR7q%2BTVcuNtsct3jdghBgRJv7%2FGI2%2F9N30tEsisjAGtt3yLuZm1DdJjjB%2BSr3%2Boko7206KubgZelCM7QLugey5yKK01eloEU62cr2Vb5JxtjfjoOFNZwR3F1h60GB36Lq1458zuwFCdZuLfdJYwAvN5kROmgLNX6TeD1TywJTrAC7aL6prURndbKf6EPEyOFtf5x7qL3ll%2FsvhZ9XVwNZI2csTINSxamIQiRMpHnHQw3u4qTXrbiTE1Bp5kyJXTVHlh4qot4wBnke3qfkgfDpujNTEDEZ8%2FS1pKeSEBbQVZgGGZWDo7%2B74cQfaDewinnd7tmTa1SVdc8%2BWdpkMwySLJF5cS1v%2BfAmr9F0SXYZ8uDek%2BZ372rogn7xig1vYurdReYIaUownXxRbkiZsrooK67%2FQyVL%2FkVZ7xakG0qzpR%2B3KgxSXT8Qb1VZzOot%2BsTjAcFjPDA2c8kn3sSTyD5dBRcwoob35wNt7H4FARE%2BrGdstDytZt7GZ9iKmgxfa%2BTtARBxe3ETVPJMYY0b8%2BpA9AOPuE6gQnQRt7ZqC2bP7BL3zQ2%2FgH7mE4TslDL2DAq0YGlZK8SPJuCWy%2BgpfQjvWdAoVCCcev9Zw1QjDTmKfGBjqkAdi%2FhwcJpYI7woYTB4mxfhhMfRmmRjbRbpv5y%2BfDXjzmRs7JeFDN0vyr9HfrFXH%2Fkm3N%2BFMWm%2Fki1wI1HW6H5K5vv1qhEos2LzqiyUGitRwqKYyjZI2cNViV0jBtn6BBrSuIm2shfNxBMjQwXsJhKRxFugkUqHRSL4zjsDehop6%2B%2BHmLLFF8B8Tjl1wwPZKfZy9JmM9MYjX290C4fyzUOaJU56Ck&X-Amz-Signature=c13a962088eade84e7aec3a85c6f380228ea295c58b6f155486cf186c2669de7&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

- **API Overview**
    - The **Real Time** api supports Text, Audio and Image endpoints
    - There is a separate **Image Generation API**, and I dont know how it differs from the Real Time Image generation endpoint.
    - **Responses** is new, extending the functionality of Chat Completions API and the Assistance API. Unlike the stateless Chat Completions API, Responses has the ability to remember previous responses, supporting multi-turn chain-of-thought.
        - The Assistance API is now depricated
        - I imagine the Chat Completions API will remain due to how widely adopted it is
    - The new Responses API simply looks like:

        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b43cf791-1dbc-4979-b9cb-2f11d884b35d/9e7fe051-d452-44a6-ac6d-7c52740a07cb/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB46655YRHEFP%2F20250916%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250916T213058Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEB0aCXVzLXdlc3QtMiJHMEUCIQCMQAmLrbklXj5edp8slbQ2P9muB9SS8qgtbtEHPltD6AIgZodHhg4e4eTITFNEytWSLOG2S2YyRhrZAKkgsVujeTAqiAQIlv%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARAAGgw2Mzc0MjMxODM4MDUiDDihIbkqDxkyMZzK5ircA5qNNvnHbQ%2BoWGYYryhkReBsVg1V7il7u%2BJSQedAEVT%2BcuaXhXi56ilzbVDWZrHg2D104VHIk69FmjcSWCDcB0oxcbW7w8A0K598imxVZx6ROgDm2pzGU3Fvgd46fdu%2BoHMNNZMsnZqlnbM9lPj2vr2wnGyWgG%2Fj9rrC%2Frb6Y5ozuF1eG2Q0XNmNRs6mGOuEfXYQPkk3PVnXMd8YkEURrXSTmoxRtJqp1eZOxg500bokjhc2LZGDdLqoe6asLypvY3SF8h%2Fce4IwwBLxW7%2FXQgzqoxQKb35ZmNLr5KCR5xad6V%2FYHQpxurOoAeVqHSluyRBQsYdYOtAai9ilBcfSE1tC9e6Vao%2B4WPb8HctfOKUbyEYztndWJnBcj%2FHbyw8NRRxC1GNXoDG85tXSmBnAAr2hko4V52tkOqlbx9I6BB5FsE37YoVJp6jatuOLHWuXKGjJ5BXOwiUPBbpxiZ0oEsJ1mZp5mLuAYGyK5TNkJm752hwE7J6PQZ7wDyG47lkEVZ8vBq09aqIxq6%2BI0wS2RF9StmNYClURhZrz6loqyMNdlpzjkHidxFKv0olBwRNH%2BcMblMzTlUiy1O5drQME97oHERGMid1%2B1vZDOE4PPW2tvaGSEZQ2aeGC0rGbMPCWp8YGOqUB5V9w0OLUASoLzsItVw1uTVst0tWGkg9iWjAXzNO8GFOZxETFCqL%2FhvOoTgAuCmAfIQpWwjx5RPiwxI8RKvpWdzJ1VwgJWx1QJFquix6yp8GtfQjFVRu47zZq5KpkS29fB25vLxlODk7BWs%2BusguRlJHJdXoNYQhh3epPbkI8M%2FYN1OemoJO4SRabNOSs0pVyZbCfFFwnGH8K4QdAJUMMf7kNprHI&X-Amz-Signature=4ec824f3f70b2dfd4cab0363037d353318bb6125bedfd18f713c612100253ce4&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)


    Projects, etc

    - Codex - agentic code development
        - [Agents.MD](http://agents.md/) - not sure if this is from OpenAI but used in Codex
    - GPT-OSS - their open source LLM
        - It sucks, but it sucks about as much as Llama 4
    - The [OpenAI Model Spec,](https://model-spec.openai.com/) which is used in some mysterious way to govern how ChatGPT works is an amazing piece of _philosophy_. This document encodes OpenAI’s values. However it’s really unclear to me how this is actually implemented in the system.

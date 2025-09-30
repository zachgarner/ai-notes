
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

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b43cf791-1dbc-4979-b9cb-2f11d884b35d/adaf8d23-d5f2-4898-83b5-d7e26746ef69/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB4664JZACIRF%2F20250930%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250930T133356Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEGUaCXVzLXdlc3QtMiJHMEUCIDBaxNn%2FLug2vlFLeMwm8WP%2BwY1Ln%2BKibyLmiNY87JWbAiEA00TfhGVJrlhKkj8Tb%2Fh1QwvhYUUYluL7xMRv3blR4eMqiAQI7v%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARAAGgw2Mzc0MjMxODM4MDUiDPUmer71j8vUEwxWLircA8sdSK6SJgEDjPvARlFnQUJDdN7IceX%2FaRGZETw9B4OAv4ML9LHCMgNBpEH%2BihZgJ4JP5WN77tH1R79TpzvYkkohYP%2FvaHW1tGj9XX5es1ttN2w9JLwqEK%2Flw%2FEQjPSGRlGuYxuZUXRj4%2F5W%2Fv0EB%2B6GY%2B0xBMpheDpI9p3gsL%2BALwY%2FsjlAZKYP8ebAsZnUY8bVGbAyfzVTfl6SEyVcyw%2BCNPZqXgMJCX5w5bzPgLwBMOtHm8jygrqPZLLz%2FS17%2BLjATPYlUiiya1O2PSszdDaq1jqwSkd6QLieRmR%2Fk6hZFla0ODNUM1SAla0Bd50XDn9N2Hv5y5cljUGGhbztXIM0CEDM%2FmoL2U6Lv6ZsHRm7A5DzQpTDvnvhWUpQIzPYM1JcPb5waieDo9rCUZkt3vXFk1VuK4Wby4LJTA%2FIwoVlnwm1IHOlI4Iu7FTyr8bomoMRmxozPGecTmJpDPS7fTtbHkeYWSqFLc5Uq3f654y2NWO7ycYu6qBOJyFY9B%2Bsl%2FwWZ6%2F%2BM%2Bl8b9qB8PjAJgjPvozEVg9lgWfznrkNgxm7ttK%2B%2BlkfYIqpPrAcL%2ByYxzAjTxfcrdIs6yfe3BrfkbZPqyMCctPfA9E5W8SZ0Cmf1d4rqXT7SEfD1imfMNij78YGOqUB72TmfqAhkm1LyQ3nV2hWH6mJqchF9QwzFmXMgQuvsS%2FUnZjyq%2Fq5rvebq9afm1ZhHNRtZI52im4i32OM0Pu7OaJZA%2FMMP5AQAcAIIKblWXzB4Xjt%2FijFuhDby5yyQibBJ0Rowajiw8RQqX4N%2B7%2BZ1FADpTrf%2Fw9qljG9pqLwsDXnhaKDlIr2mYlrb00UX%2FFd64Urtkpo6VSJhadkcWBByitOvifR&X-Amz-Signature=1a05e660cc5e447bee696f269627909a5ba1ab1754ad326f92e6cb65eb6f744d&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

- **API Overview**
    - The **Real Time** api supports Text, Audio and Image endpoints
    - There is a separate **Image Generation API**, and I dont know how it differs from the Real Time Image generation endpoint.
    - **Responses** is new, extending the functionality of Chat Completions API and the Assistance API. Unlike the stateless Chat Completions API, Responses has the ability to remember previous responses, supporting multi-turn chain-of-thought.
        - The Assistance API is now depricated
        - I imagine the Chat Completions API will remain due to how widely adopted it is
    - The new Responses API simply looks like:

        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b43cf791-1dbc-4979-b9cb-2f11d884b35d/9e7fe051-d452-44a6-ac6d-7c52740a07cb/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466QBUGBMWT%2F20250930%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250930T133358Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEGUaCXVzLXdlc3QtMiJHMEUCIEGJUf377Ve9seoBZLtok3qZYbKHra8RTDzjqslr9BUuAiEAhZv%2FCeGLlsu7V2L7Yy6K08WAg%2BvyCLcqCDyG5q%2B3qFQqiAQI7v%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARAAGgw2Mzc0MjMxODM4MDUiDD1QWSHV35fXzcImYCrcA9g69HRVrZ3jE5A2XAxQnBhzUGhMNhYtoAWXpd7Wm%2FUZFkYK0zxV3a0Tb%2FoXyvgwlctoWOIXwSonpByrCbrhxzM3goscfv%2BW79778wl%2FGhF4wQgpH8FxuWLo1fa4LtxdJSHUgCovdim14iqmnD0fM02SuBl8hehJrVG9V8toiNLeGHfOdwEvJlVJ4ANj3vUBBd1h%2B3uRCURhxhCG8cgOydGzwWwhb98xOuRLZqMMTfa%2FRcUlXfYjbsBAuZzw2xuVT3oOPFBAPILeDoW287DFneqgJ6otu%2B2XhcpFuq9jX%2B6jxM6dw8vK33U8jmzMU1An%2BAonVuttcfEQH4XcHC%2F0ZzwVXe3xHQboE%2F%2F3nP4Gh6Bf0JZ9J0V7sHpnPpA9MZFVacmANWMSTjwd009W%2FRE0kiqPpkpT48M9%2Bcbxq1Lclp5aHH2oTOG7JdvaRYaQbba8xFOBkcvpBIsTwfvDUTdpBTFNuBu3V9cDYUU1ARFCMayp7LHGO6uZGzj6V3V5%2FU5L4RUj%2FasP22q7I%2BAT%2F2WTgOYnJlLsSOdkNacd23bvDkii4rnZA1oGcD9c16qMZYOqIwvD%2B9WUCWlMESZkgBv8E9o6SAV%2F%2FCN55vtAZ%2By2ys1go5gkjWj%2BKMDbStKCMOej78YGOqUBCndsn8nn%2FIbYxpGcZa9joQAdTiBtdpMTqqLNj9YnqDexOrfqRHbj8mYLWrQUA7Pg54592qTQa0GDq2Q1PsgPZlRCDkpH2PyMwiQ2YGfywnfkzAoGkV3yLbVZt%2BLHaXRiSEzTYmsAFdkZrKn6U6v7vxl7dqA9%2BDNyXARyf2HiaNiGFI5FaxKa3m9Ba%2BDsJb5osJ4AGxpXFmN7L5FUlIIUR%2FRdOzOp&X-Amz-Signature=9a5aa4577df84fbf6534d4163f22355f8f26afbc64321ec376e0a1958793c705&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)


    Projects, etc

    - Codex - agentic code development
        - [Agents.MD](http://agents.md/) - not sure if this is from OpenAI but used in Codex
    - GPT-OSS - their open source LLM
        - It sucks, but it sucks about as much as Llama 4
    - The [OpenAI Model Spec,](https://model-spec.openai.com/) which is used in some mysterious way to govern how ChatGPT works is an amazing piece of _philosophy_. This document encodes OpenAI’s values. However it’s really unclear to me how this is actually implemented in the system.

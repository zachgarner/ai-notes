
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

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b43cf791-1dbc-4979-b9cb-2f11d884b35d/adaf8d23-d5f2-4898-83b5-d7e26746ef69/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466TQM45FKU%2F20250930%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250930T133356Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEGUaCXVzLXdlc3QtMiJIMEYCIQDKAOGH%2Fy21vwqkjPWFht8bW4gC95hjLnI9MtOsiRfo3AIhAJxNUu%2BDPuto2j6y4ZJ7I4c9cxd1WGLb7R2GXaD5kRD3KogECO7%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEQABoMNjM3NDIzMTgzODA1Igzr3kcw8eN7gq%2BkeVQq3AM%2F7iI738PAA%2FZkS7SNwpCueZq1pHi17ICZKurcNXDDSZiCLP5EPJzGHfuVJPgADwTexnlhCBHbTF63NYa0pIcdAaEAXXmvCvtTOxoH35dxOGNX41PU7yaWXLhpLq5FwPlpSDIx7802i%2FOt7WvhOd1iKD1PyZXjUzcdKVnpMoK%2FDjq%2Fbx5%2F2sBhfFAYVj96u5JvKR5nKJLMAJDzT57GnjliSIotQf9lK0FctrBY99fCkGpxsoQtc2Ju5Tw16JmPyz1xqqEheYlMjV9Dm5GVAGVjYxZ4UNCIJSy4PIUvDeOgU4yAhEoWtxNaPUdsIjcJ7Pc4rWr%2B6EWoDY1cRwPND%2FCiD8DfrVSnzn1M6L0WBszAeN2N8Wv4q0CHAFKwPOXDsAUr4GLfKITuF%2FYKmnUMMtsuJSYIyXp1FkryY2my3WiF8XmHhSmD1DE4z4Q8KMnP4l2EwrGOC%2B9WAN5PB%2BGKAvVqITXFAEicL9IHgHNL2hnh4cfuZhwb%2BmSz1h7nuUWOywPCkouWgl0mnMzrB%2FaZD%2Fkw%2FiUGzgFBczhzLn0pEXDWjOOkRxSbadG2Hz9cEpVfbqp6FewejoM40WoECRaeuxa%2BaRBhpdQymKwsZDF4X00vF8NKYdYgw8onrOkcczDPo%2B%2FGBjqkATWHbqQT%2FUGtStKllXxFQ5pPTc9PTZmBi1qxQVkS6ji7o4YEZFl5POvS4PaMCkEiPGG7Ny%2FNMe3SS7LA8WE9MVppvZiJ6WmEUjomPgFKxecORkNsIKmCrS91qFzBWMDuQXH6NZQLTZm2R%2Bi7QD0J4XBHHRFv1V36nD8Zg%2FPT5wGfwBITPX%2BpMb0pbOM0F3ZQTxYUVSO7HOpZmG82DabtxoPXI2aA&X-Amz-Signature=a15da9e9d96439ccf01cf398474bf832d105df88b565544c5c9a383bc5e954bd&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

- **API Overview**
    - The **Real Time** api supports Text, Audio and Image endpoints
    - There is a separate **Image Generation API**, and I dont know how it differs from the Real Time Image generation endpoint.
    - **Responses** is new, extending the functionality of Chat Completions API and the Assistance API. Unlike the stateless Chat Completions API, Responses has the ability to remember previous responses, supporting multi-turn chain-of-thought.
        - The Assistance API is now depricated
        - I imagine the Chat Completions API will remain due to how widely adopted it is
    - The new Responses API simply looks like:

        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b43cf791-1dbc-4979-b9cb-2f11d884b35d/9e7fe051-d452-44a6-ac6d-7c52740a07cb/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466YLTDWSGP%2F20250930%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250930T133404Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEGUaCXVzLXdlc3QtMiJHMEUCIAxWHTOSqLNFR5agzdpTRzCKLXmGwdFwcFeMGfz1KX2uAiEA9dbMS8YjnLM6oSMlOCIJ7Hd2DHO10beImJgz4zWlFtsqiAQI7v%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARAAGgw2Mzc0MjMxODM4MDUiDKpCPOT3bQNb9lQYFyrcA1EIcS%2BLkaRKSgzEkU7cWkocsUxlh416kxJ%2Fa5tzdCjxmgJQEsNI%2Fc7BYRiP3qqFUICQ5Lo4U45iycK%2BDIDtNddL4uWKVRNBUNF8vgnHURf0D9RRnaIJ1Qd95KSMFFBvonv%2F5DeatLyL46r6QgajBIKdH8hUkkkyRDDYrR5cU9ZrOz2tmvkV0fR9WuCBrGGMEFebHXr9GMHVbZAkQwAkpaMztSj4bltO0yGHyTuM74C68RtOPADkm5sdeR1buu7ZuucVF734XzZb%2B3E9puTIy9y6VUc9CxnEo%2F2oXVquF4ENk8QGBiiFy%2FF666WZ5Dq4dZz21TiJfXifN8rxgT0U5XS9Wpb3p7U6u9xbx4hqx2wTfDTKYm9EaOpGpJhlqH0Xi%2FH9SmwdtBWxJxXUVASzk4Ad7UH8%2FrmYDQ4psr0IQeUaFC0%2BUB7pjcglWEljvC0aMQWRsnmlyE0D9KkYPHCwKIeqcsT6m%2BqVkguAr36a%2BWHBi5yJTfTnjK9fDURIpbjN25oI8aoTWMrNOvNhUX7sStOXwJbQlxFzFDBi0zAgaEUvbx0ucn0SvU%2BukJOtY4rGZlb83hhQP27ONjMAxBTr9l8zbYBbm9JAf44FeZmWfwpjdNiLcY9baui5jwzwMOej78YGOqUB6aZuAGyf1b5d5YP7kMHebfl7r%2BuYVjFOXBA2dn4Ulj0zrMiv%2FFRDBDpdPExe%2BVOdiRBHDc1cLIHQIdFmKEM8XPJ%2BlQ9PnLagOO1JQ0TSsPAN%2B%2Bf6rxroRDLZogn7f18itDRb0nudnfJsBwetbgQ%2B3WmveJtREQ3BxuG%2FDZ4StOkDLDy0RqKkEIj4wUidakVs1V3fMWBP6JK1QJgbkXD5c7C%2BvGaY&X-Amz-Signature=140aa47bc7fffa0903b110903d9aad213bd56701a23543f183bdfd780369444b&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)


    Projects, etc

    - Codex - agentic code development
        - [Agents.MD](http://agents.md/) - not sure if this is from OpenAI but used in Codex
    - GPT-OSS - their open source LLM
        - It sucks, but it sucks about as much as Llama 4
    - The [OpenAI Model Spec,](https://model-spec.openai.com/) which is used in some mysterious way to govern how ChatGPT works is an amazing piece of _philosophy_. This document encodes OpenAI’s values. However it’s really unclear to me how this is actually implemented in the system.

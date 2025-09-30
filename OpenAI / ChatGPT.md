
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

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b43cf791-1dbc-4979-b9cb-2f11d884b35d/adaf8d23-d5f2-4898-83b5-d7e26746ef69/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB4667EH3AWVH%2F20250930%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250930T133355Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEGUaCXVzLXdlc3QtMiJHMEUCIQDM6PO4JTEEkduddTJmEL1Y2U8eA4K29HI9%2B1rGohrcTgIgYqUIIfoNqsDVd8v1fTONqBlllQRkkMzaipw7yBb82FYqiAQI7v%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARAAGgw2Mzc0MjMxODM4MDUiDG32Y001dGvcAma3bSrcA2GIBZBF%2Ft2ZK5XLgD84S2SmE2LHhs7%2FoLTKDDmwID9kWSUzpAf9ySXMRUavFpvtj1XJaaX6d3UB7fFm1MnWeWmT1Rbbb82LUMTi%2F4XRGCQyIrKr8kbxnO5TIFXvF4gHlYGUwFXmxC1Q%2FzKgZSwpUDibyCprg4aCJ0oeBK1d0DTtovM%2B0eWge3pg%2B28ujec38%2Fx7Gxy60VCTmavqFm6M2Z7YaHrjGgKTtPHsqOJpF0%2FgSJYieYnykIffHqMGTRvr5zGW6%2Ba1%2Fk1ZcKMGQ9qB37DYfgboSDWB4Dgx%2BUexmJ7RdXiZOPEMZUvT53Xsbzl5ybcml7tYXfPzdLFWTdJvqEYr5fttywXCseSTAtiY1%2BjoVPr2W8twU0S587uI%2FYkfp8%2FNNIRmU%2FLFl7mAav%2BLEC1YGbrFvyc83zg0yRzIVeBHiiRwbLTnxqPBCJBt6pMXeqfIiOiz2lJwSlZPNok4hSAxdE3wLR3klw1CsjFCsoP0rhx2MUvGbcRBRp5O0XZvejBy%2FLxi9XtkG%2FMx%2BK1eIj3u7gz1a3znom70J3dLwYTP3ah%2F6sT64iYvcFuph7eDFIxna98xEEv3WO4mmdLfpQXnpC7%2FTEwhz91BMzbsvtkFl1z7R%2Fj7fXkvMdfrMLmi78YGOqUBlHmli2kBorW5e9Yeu9UE6yyy0WEdJCKEttFgeQleus4El0OXFUR8I1CHEdX5%2BvuvjMDzKtfPvA17Liuto2%2BqniebdeGKfqIRG3jYmbKR2N6Su7lqfxrtQjU%2Fe9rHWkfOJhC5kgAki5ooLrozaL0j2NdR276QQ3yw%2FAehuWJuh7aF2gtC6f12VP4XWHeKuCaXm5mb%2F8Q8Yujl92Eh1saUIyl82r%2BW&X-Amz-Signature=fb8960ad700fb0108864c7417cbffa9113985344c8a99e901fba5da59d418d68&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

- **API Overview**
    - The **Real Time** api supports Text, Audio and Image endpoints
    - There is a separate **Image Generation API**, and I dont know how it differs from the Real Time Image generation endpoint.
    - **Responses** is new, extending the functionality of Chat Completions API and the Assistance API. Unlike the stateless Chat Completions API, Responses has the ability to remember previous responses, supporting multi-turn chain-of-thought.
        - The Assistance API is now depricated
        - I imagine the Chat Completions API will remain due to how widely adopted it is
    - The new Responses API simply looks like:

        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b43cf791-1dbc-4979-b9cb-2f11d884b35d/9e7fe051-d452-44a6-ac6d-7c52740a07cb/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466RNH7UARD%2F20250930%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250930T133356Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEGUaCXVzLXdlc3QtMiJGMEQCIFeWaZlPYJJsGRLxobzbjG3ZGjqk4%2B5ZlB3oarO%2Bvm5gAiANoNS3wnpKs1b6NqJS4HO4tz0QOko9975y3AMfscEGSCqIBAju%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F8BEAAaDDYzNzQyMzE4MzgwNSIMKh9KpsmMrYDIg9DeKtwDPX2tAI5dWdeIRYQ%2BIIWBEzeSHu7gcjo5Sa0YVI8O5s4UAIryJY6RJQA11Jo58plLyF%2F0ICWASAhGRmzj7uyhI2RXxRdY7FP5MaW7zxFEMuSLDehHyfvqE%2FtOxLjbH1Bki%2FE0Xvu8B0eYNXCmakNGnq5gGTJBARnBTaxewAAH5wxHFVYCxPdTYw4t6%2BvYbQEOPI3ombBf2NxAdK7vawIJma0fq%2FtJGZ2wXTyB3eubURr53bWyUP70NQJqMIZP8RImTCL%2BSaJC%2FSNpH0Gut3WCDEBKjZ0nFXvef6ErwaZnHeNGWcE6wA13DcWqUuxTOViVwhJz6Y8H9yNkxA4yxlCDL260PE5AUdCV67RdbnMivdi1wwPcA9kIswWqMUmDbfsT%2BqliBcPuI%2Bs9aLu7Z6BU4hS0DhatUuPK8bN2G%2F7C%2FI5LjlPymPFDaOuClTvIiW6n2i6ItB7K2m1USykdxqskAxvD3DK15gXj125mq5Y9hRZjihNpf3yFGSAS7HqziTS0XZINeuBAtDKB%2FE1VcXucsRCUZEGs%2FGzTdVdzDF%2Fxtut7%2B4j9BPLLZwswsQS2SGM2Hrvo7SA1j7akan4bnv3460rxH4pbtzMxYhaHAXm3DFEkbqndci6wSdBqwoswsqLvxgY6pgGEzup%2BeRBP1GJNseKu%2B9rMQ4Evkfuw%2F28fxC2KEFQm2mfa0Lf8RmPmO7MC1xhnS5IdGzH7rWZOUBZkpfe4BLSjMziqQuqynZ9g4Psb3WYbECljL88vqhOHXVRodlx%2BKX5NzN4IxgcHgvdpH%2B087Hog0t6Vj%2B%2BbyYQIz78MYdAe2SS0GL7YjMoG1ld%2FFT9HB%2F4%2FU4%2Bi4JpqqdSyGDSUkmfHFADV1s%2BM&X-Amz-Signature=b8287b58ed5105cca71504d52da63478b922c76bd3a6dcc09d185af92c8bdbef&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)


    Projects, etc

    - Codex - agentic code development
        - [Agents.MD](http://agents.md/) - not sure if this is from OpenAI but used in Codex
    - GPT-OSS - their open source LLM
        - It sucks, but it sucks about as much as Llama 4
    - The [OpenAI Model Spec,](https://model-spec.openai.com/) which is used in some mysterious way to govern how ChatGPT works is an amazing piece of _philosophy_. This document encodes OpenAI’s values. However it’s really unclear to me how this is actually implemented in the system.

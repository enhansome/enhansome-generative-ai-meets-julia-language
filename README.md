<!-- omit from toc -->

# Awesome Generative AI Meets Julia Programming Language with stars

> Comprehensive guide to generative AI projects and resources in/for/associated with Julia.

[<img src="https://github.com/JuliaLang/julia/raw/master/doc/src/assets/logo.svg" align="right" width="120"/>](http://julialang.org)

Julia is a high-level, high-performance dynamic language for technical computing.

Generative AI encompasses algorithms and models that leverage large-scale machine learning to generate new content (across many modalities), automate, understand, parse, extract and much more, adapting to a wide range of applications beyond mere content creation. <br>

<!-- omit from toc -->

## Contents

* [Generative AI Projects and Julia](#generative-ai-projects-and-julia)
* [Models](#models)
* [API SDKs](#api-sdks)
  * [Model Providers](#model-providers)
  * [Cloud Services Providers](#cloud-services-providers)
  * [Vector Databases](#vector-databases)
  * [General-purpose DBMS with Vector Index Support](#general-purpose-dbms-with-vector-index-support)
* [Packages](#packages)
* [JLL Packages](#jll-packages)
* [Benchmarks/Comparisons](#benchmarkscomparisons)
* [Applications/Products](#applicationsproducts)
* [Waiting Room](#waiting-room)
* [Archived Projects](#archived-projects)
* [Tutorials/learning](#tutorialslearning)
* [Noteworthy Mentions](#noteworthy-mentions)
  * [Local Deployments](#local-deployments)
  * [Generative AI - Previous Generation](#generative-ai---previous-generation)
* [Must-Know Python Projects](#must-know-python-projects)
* [Other Awesome Lists](#other-awesome-lists)

## Generative AI Projects and Julia

* [JuliaGenAI Organization](http://juliagenai.org/) - A GitHub organization and a community of Julia developers and researchers working on generative AI.

## Models

Build, train, and deploy Large language models (and other modalities) in Julia.

* [Flux.jl](https://github.com/FluxML/Flux.jl) ⭐ 4,741 | 🐛 45 | 🌐 Julia | 📅 2026-08-16 - Flux is a machine learning library for Julia that is flexible and allows building complex models. However, at the time of writing, I'm not aware of any Large Language Models (LLMs) that have been implemented and trained in Flux.
* [Transformers.jl](https://github.com/chengchingwen/Transformers.jl) ⭐ 571 | 🐛 48 | 🌐 Julia | 📅 2026-07-31 - Transformers.jl is a Julia package that provides a high-level API for using pre-trained transformer models. It also allows to download any models from Hugging Face hub with `@hgf_str` macro string.
* [Llama2.jl](https://github.com/cafaxo/Llama2.jl) ⭐ 141 | 🐛 12 | 🌐 Julia | 📅 2024-08-15 - Llama2.jl provides simple code for inference and training of llama2-based language models based on [llama2.c](https://github.com/karpathy/llama2.c) ⭐ 20,035 | 🐛 189 | 🌐 C | 📅 2024-08-06. It supports loading quantized weights in GGUF format (`q4_K_S` variant). Other similar projects: [LanguageModels.jl](https://github.com/rai-llc/LanguageModels.jl) ⭐ 65 | 🐛 9 | 🌐 Julia | 📅 2023-10-08
* [Pickle.jl](https://github.com/chengchingwen/Pickle.jl) ⭐ 55 | 🐛 11 | 🌐 Julia | 📅 2026-04-12 - Great package for loading Pytorch weights into Julia (if you want to implement models yourself).
* [Whisper.jl](https://github.com/aviks/Whisper.jl) ⭐ 52 | 🐛 3 | 🌐 Julia | 📅 2026-08-23 - Julia interface to whisper.cpp, a high-performance inference in C/C++ of OpenAI's Whisper automatic speech recognition (ASR) model.
* [Llama.jl](https://github.com/marcom/Llama.jl/) ⭐ 33 | 🐛 4 | 🌐 Julia | 📅 2025-02-25 - Julia interface to llama.cpp, a C/C++ library for running language models locally. Supports a wide range of models.
* [BytePairEncoding.jl](https://github.com/chengchingwen/BytePairEncoding.jl) ⭐ 26 | 🐛 3 | 🌐 Julia | 📅 2024-06-15 - Pure Julia implementation of Byte Pair Encoding (BPE) algorithm. It's used by Transformers.jl to tokenize text.

## API SDKs

### Model Providers

Access Generative AI models via official APIs.

* [OpenAI.jl](https://github.com/JuliaML/OpenAI.jl) ⭐ 118 | 🐛 7 | 🌐 Julia | 📅 2026-06-06 - A community-maintained Julia wrapper to the OpenAI API.

### Cloud Services Providers

Access Generative AI models via SDKs of popular cloud service providers.

* [GoogleCloud.jl](https://github.com/JuliaCloud/GoogleCloud.jl) ⭐ 45 | 🐛 13 | 🌐 Julia | 📅 2024-01-11 - SDK for Google Cloud. There is an [open PR](https://github.com/JuliaCloud/GoogleCloud.jl/pull/57) ⭐ 45 | 🐛 13 | 🌐 Julia | 📅 2024-01-11 to enable Vertex AI endpoints.
* [GoogleGenAI.jl](https://github.com/tylerjthomas9/GoogleGenAI.jl) ⭐ 19 | 🐛 3 | 🌐 Julia | 📅 2026-08-23 - Unofficial wrapper for the Google Gemini API.

### Vector Databases

* [Pinecone.jl](https://github.com/tullytim/Pinecone.jl) ⭐ 26 | 🐛 7 | 🌐 Julia | 📅 2024-08-13 - SDK for [Pinecone.io](https://www.pinecone.io/) vector database.

### General-purpose DBMS with Vector Index Support

|                                                               Name                                                               |                                                     Julia Client                                                    |                                                                         Usage Examples                                                                         |
| :------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|                                       [Elasticsearch](https://www.elastic.co/elasticsearch)                                      | [ElasticsearchClient.jl](https://github.com/LarsWl/ElasticsearchClient.jl) ⭐ 6 \| 🐛 1 \| 🌐 Julia \| 📅 2024-12-23 | [GptSeachPlugin with Elasticsearch](https://github.com/rssdev10/GptSearchPlugin/tree/main/ext/ElasticsearchClientExt) ⭐ 7 \| 🐛 0 \| 🌐 Julia \| 📅 2023-12-07 |
|                                               [OpenSearch](https://opensearch.org/)                                              | [ElasticsearchClient.jl](https://github.com/LarsWl/ElasticsearchClient.jl) ⭐ 6 \| 🐛 1 \| 🌐 Julia \| 📅 2024-12-23 |       [GptSeachPlugin with Opensearch](https://github.com/rssdev10/GptSearchPlugin/tree/main/ext/OpenSearchExt) ⭐ 7 \| 🐛 0 \| 🌐 Julia \| 📅 2023-12-07       |
| PostgreSQL + [pgvector](https://github.com/pgvector/pgvector?tab=readme-ov-file#hnsw) ⭐ 22,805 \| 🐛 14 \| 🌐 C \| 📅 2026-08-20 |              [LibPQ.jl](https://github.com/iamed2/LibPQ.jl) ⭐ 227 \| 🐛 62 \| 🌐 Julia \| 📅 2026-08-28             |                       [pgvector examples for Julia](https://github.com/pgvector/pgvector-julia) ⭐ 8 \| 🐛 0 \| 🌐 Julia \| 📅 2026-07-09                       |

## Packages

* [PromptingTools.jl](https://github.com/svilupp/PromptingTools.jl) ⭐ 172 | 🐛 35 | 🌐 Julia | 📅 2026-07-03 - Helps with everyday applications of Large Language Models in Julia by wrapping coming APIs, re-using prompts via templates, and enabling easy transition between different model providers (eg, OpenAI, Ollama). (Disclaimer: I'm the author of this package.)
* [ReplGPT.jl](https://github.com/ThatcherC/ReplGPT.jl) ⭐ 101 | 🐛 15 | 🌐 Julia | 📅 2024-04-17 - Brings ChatGPT interface as a Julia REPL mode.
* [AIHelpMe.jl](https://github.com/svilupp/AIHelpMe.jl) ⭐ 48 | 🐛 12 | 🌐 Julia | 📅 2024-08-19 - Enhanced AI code assistance by leveraging package documentation (Retrieval Augmented Generation). Comes pre-packaged for common Julia packages, but can be used for any package.
* [LLMTextAnalysis.jl](https://github.com/svilupp/LLMTextAnalysis.jl) ⭐ 41 | 🐛 4 | 🌐 Julia | 📅 2025-02-01 - Leverage Large Language Models to uncover, evaluate, and label themes/concepts/spectra in large document collections. (Disclaimer: I'm the author of this package.)
* [RAGTools.jl](https://github.com/JuliaGenAI/RAGTools.jl) ⭐ 33 | 🐛 5 | 🌐 Julia | 📅 2025-11-27 - Build and use Retrieval-Augmented Generation (RAG) systems. A module carved out of PromptingTools.jl.
* [GenGPT3.jl](https://github.com/probcomp/GenGPT3.jl) ⭐ 19 | 🐛 0 | 🌐 Julia | 📅 2024-07-14 - A [Gen.jl](https://www.gen.dev/) generative function that wraps the OpenAI API.
* [HelpGPT.jl](https://github.com/FedeClaudi/HelpGPT.jl) ⭐ 18 | 🐛 3 | 🌐 Julia | 📅 2023-04-03 - Calls ChatGPT to explain any errors in Julia code.
* [ProToPortal.jl](https://github.com/svilupp/ProToPortal.jl) ⭐ 17 | 🐛 2 | 🌐 Julia | 📅 2024-07-14 - Web-based graphical interface for PromptingTools.jl with extra prompt templates and functionality (Julia code execution and auto-fixing, meta-prompting, auto-critic, speech-to-text entry). Similar to ChatGPT but geared towards Julia.
* [AIHelpUI.jl](https://github.com/BuiltWithGenie/PkgAIHelp) ⭐ 8 | 🐛 3 | 🌐 Julia | 📅 2025-02-26 - Web-based graphical interface for AIHelpMe.jl built on top of Stipple.jl.

## JLL Packages

[JLLs](https://docs.binarybuilder.org/stable/jll/) are prebuilt libraries and executables to easily install and call non-Julia projects (eg, C/C++). Often they are the first step towards a Julia package with an idiomatic interface.

* [llama\_cpp\_jll.jl](https://juliahub.com/ui/Packages/General/llama_cpp_jll/) - JLL package for [llama.cpp](https://github.com/ggerganov/llama.cpp) ⭐ 126,134 | 🐛 2,273 | 🌐 C++ | 📅 2026-08-29, the best interface for quantized llama2-style models.

## Benchmarks/Comparisons

* [Julia LLM Leaderboard](https://github.com/svilupp/Julia-LLM-Leaderboard) ⭐ 86 | 🐛 2 | 🌐 HTML | 📅 2024-08-14 - Comparison of Julia language generation capabilities of various Large Language Models across a range of tasks. Visit if you want help choosing the right model for your application.
* [HumanEval.jl](https://github.com/01-ai/HumanEval.jl) ⭐ 25 | 🐛 1 | 🌐 Julia | 📅 2024-08-17 - The Julia version of [openai/human-eval](https://github.com/openai/human-eval) ⭐ 3,355 | 🐛 45 | 🌐 Python | 📅 2025-01-17. It rewrites the original Python problems into the Julia version and provides evaluation results with several latest LLMs.

## Applications/Products

Applications and products that "work" with Julia language.

* [GitHub Copilot](https://github.com/features/copilot) - Excellent inline suggestions with the help of OpenAI models. It works extremely well with Julia language for repetitive tasks one line at a time, but larger code chunks are rarely correct.
* [Codium.ai](https://codium.ai/) - Great IDE or VSCode plugin for code analysis, suggestion and generation of test suites. Although the tests are written more in the style of Pytest rather than idiomatic Julia. It has a free tier.
* [Replit](https://replit.com/ai) - Replit's REPL is powered by an in-house model that supports Julia language.
* [Codeium](https://codeium.com/) - Free alternative to GitHub Copilot with extensions for most editors.
* [Cursor](https://cursor.sh/) - Alternative IDE based on VSCode with AI-powered code completion and suggestions. It works really well with Julia language.

Julia-affiliated applications and products using LLMs

* [Genie UI Assistant](https://forem.julialang.org/pgimenez/introducing-genie-ui-assistant-the-ai-powered-ui-builder-for-genie-apps-3jpe) - Genie UI Assistant is a GPT-4 powered
  UI builder helping [Genie.jl's](https://github.com/GenieFramework/Genie.jl) ⭐ 2,414 | 🐛 126 | 🌐 Julia | 📅 2026-06-22 users create UIs faster using natural language.
* [JuliaHub AskAI](https://juliahub.com/ui/AskAI) - AskAI is a [JuliaHub's](https://juliahub.com) RAG (Retrieval Augmented Generation) application that allows users to ask questions about the Julia language and its ecosystem. It is free, but you need to be logged in to JuliaHub to use it.
* [Comind](https://comind.me) - A social network, messaging, and LLM interface built in Julia.

## Waiting Room

New projects that are still waiting to prove themselves and collect enough stars.

* [FlashRank.jl](https://github.com/svilupp/FlashRank.jl) ⭐ 8 | 🐛 2 | 🌐 Julia | 📅 2024-11-18 - Fast and local document ranking with models that can run on any computer (CPU-based). Based on Python's [FlashRank](https://github.com/PrithivirajDamodaran/FlashRank) ⭐ 1,002 | 🐛 10 | 🌐 Python | 📅 2026-07-11.
* [SwarmAgents.jl](https://github.com/svilupp/SwarmAgents.jl) ⭐ 5 | 🐛 1 | 🌐 Julia | 📅 2024-11-25 - Based on OpenAI's Swarm package for multi-agent systems with tight integration with PromptingTools.jl and additional features.
* [SemanticCaches.jl](https://github.com/svilupp/SemanticCaches.jl) ⭐ 4 | 🐛 1 | 🌐 Julia | 📅 2024-11-18 - Smarter caching for GenAI applications with a tiny embedding model - reducing latency, one request at a time.
* [ChromeDevToolsLite.jl](https://github.com/svilupp/ChromeDevToolsLite.jl) ⭐ 4 | 🐛 2 | 🌐 Julia | 📅 2025-11-24 - Browser automation using the Chrome DevTools Protocol (CDP). Ideal for Computer Use with LLMs. Inspired by Python's Playwright but providing just the essential functionality to get you started with browser automation in Julia.
* [Spehulak.jl](https://github.com/svilupp/Spehulak.jl) ⭐ 3 | 🐛 2 | 🌐 Julia | 📅 2024-12-23 - GenAI observability platform for debugging your LLM calls. Fully integrated with PromptingTools.jl.
* [LLMCheatsheets.jl](https://github.com/svilupp/LLMCheatsheets.jl) ⭐ 3 | 🐛 1 | 🌐 Julia | 📅 2024-11-18 - Summarize GitHub repositories into AI-friendly cheatsheets with a single command.
* [StreamCallbacks.jl](https://github.com/svilupp/StreamCallbacks.jl) ⭐ 2 | 🐛 6 | 🌐 Julia | 📅 2025-11-28 - Unifies LLM streaming interfaces, simplifies SSE handling, and provides built-in sinks for streaming data. Easy to extend with custom logic.
* [OmniParserIconDetectors.jl](https://github.com/svilupp/OmniParserIconDetectors.jl) ⭐ 1 | 🐛 1 | 🌐 Julia | 📅 2025-11-24 - Lightweight Julia wrapper for Microsoft's OmniParser icon detection model with additional utilities for working with screenshots (eg, drawing detections, adding labels).

Unreleased, experimental but functional:

* [Jjama3.jl](https://github.com/MurrellGroup/Jjama3.jl) ⭐ 39 | 🐛 8 | 🌐 Julia | 📅 2026-06-22 - Hackable Llama3.1, Llama3.2 (text), and Qwen 2.5 (eg. base, Qwen2.5-Coder, and Qwen2.5-Math) in Julia.
* [Milvus.jl](https://github.com/asbisen/Milvus.jl) ⭐ 2 | 🐛 0 | 🌐 Julia | 📅 2024-02-28 - A minimal and unofficial implementation of Milvus VectorDB client for Julia.

## Archived Projects

* [GPTCodingTools.jl](https://github.com/svilupp/GPTCodingTools) ⚠️ Archived - Code generation tool for Julia language with useful prompt templates and self-healing features (ala OpenAI Code Interpreter). It does work, but development has been abandoned. (Disclaimer: I'm the author of this package.)

## Tutorials/learning

* [Tiny Binary RAG](https://github.com/domluna/tinyrag/tree/main) ⭐ 17 | 🐛 0 | 🌐 Julia | 📅 2024-06-11 - An excellent deep-dive on semantic search (the "R" in RAG). It showcases that with 100 lines of Julia, you can search 15M chunks (\~size of Wikipedia) in <20ms.
* [Tutorial for using LLMs with Transformers.jl](https://info.juliahub.com/large-language-model-llm-tutorial-with-julias-transformers.jl) - A brief tutorial on how to use Transformers.jl to access LLMs from HuggingFace Hub.
* [Building a RAG Chatbot over DataFrames.jl Documentation - Hands-on Guide](https://forem.julialang.org/svilupp/building-a-rag-chatbot-over-dataframesjl-documentation-hands-on-guide-449m) - A hands-on guide on how to build a RAG chatbot over DataFrames.jl documentation using only minimal dependencies.
* [GenAI Mini-Tasks: Extracting Data from (.\*)? Look No Further!](https://forem.julialang.org/svilupp/genai-mini-tasks-extracting-data-from-look-no-further-2m32) - A tutorial on structured data extraction. A part of a larger series of tutorials on small tasks that can be done with GenAI.

## Noteworthy Mentions

Some of the below projects are not necessarily Julia-specific, but noteworthy mentions in the generative AI space and interesting for Julia developers.

### Local Deployments

* [Ollama](https://github.com/jmorganca/ollama) ⭐ 179,675 | 🐛 3,832 | 🌐 Go | 📅 2026-08-29 - The best option for those looking to host a Large Language Model locally. Simply start the server and send the requests with [HTTP.jl](https://github.com/JuliaWeb/HTTP.jl) ⭐ 687 | 🐛 5 | 🌐 Julia | 📅 2026-08-28.
* [LM Studio](https://lmstudio.ai/) - A desktop app for hosting and interacting with LLMs locally. It's a great option for those who want to use LLMs without coding. It's free for **personal use**.

### Generative AI - Previous Generation

* [GenerativeModels.jl](https://github.com/aicenter/GenerativeModels.jl) ⭐ 32 | 🐛 9 | 🌐 Julia | 📅 2022-09-21 - Useful library to train more traditional generative models like VAEs. It's built on top of Flux.jl.

\### Useful Utilities

* [Stipple.jl](https://github.com/GenieFramework/Stipple.jl) ⭐ 356 | 🐛 38 | 🌐 JavaScript | 📅 2026-08-27 - For building interactive data applications in pure Julia (part of Genie.jl ecosystem). Excellent for building web-based interfaces for GenAI applications.
* [Taro.jl](https://github.com/aviks/Taro.jl) ⭐ 129 | 🐛 5 | 🌐 Julia | 📅 2023-08-15 - Powerful parser for various types of documents (interop to Java). Very useful for building Retrieval-Augmented Generation (RAG) applications.

## Must-Know Python Projects

Python is on the leading edge of the generative AI revolution. Fortunately, we have [PythonCall.jl](https://github.com/JuliaPy/PythonCall.jl) ⭐ 1,066 | 🐛 203 | 🌐 Julia | 📅 2026-08-28 allowing us to easily call all the below Python packages.

* [LangChain](https://github.com/langchain-ai/langchain) ⭐ 145,216 | 🐛 431 | 🌐 Python | 📅 2026-08-28 - The best option for building applications on top of LLMs (eg, Chains, Agents). It has a lot of adapters for common models, databases, and other services.
* [Open Interpreter](https://github.com/KillianLucas/open-interpreter) ⭐ 68,177 | 🐛 8 | 🌐 Rust | 📅 2026-08-20 - Let LLMs run code on your computer (eg, Python, JavaScript, Shell, and more). An open-source local alternative to OpenAI Code Interpreter.
* [Llama Index](https://github.com/run-llama/llama_index) ⭐ 51,909 | 🐛 670 | 🌐 Python | 📅 2026-08-29 - Similar to LangChain but with a focus on data-centered applications like RAG.
* [Instructor](https://github.com/jxnl/instructor) ⭐ 13,795 | 🐛 39 | 🌐 Python | 📅 2026-08-29 - Simple yet powerful structured extraction framework on top of OpenAI API. Excellent to understand the power of function calling API together with Pydantic.
* [Marvin](https://github.com/prefecthq/marvin) ⭐ 6,192 | 🐛 114 | 🌐 Python | 📅 2026-08-21 - Powerful building blocks to quickly build AI applications and expose them via a production-ready API.
* [HuggingFace Transformers](https://huggingface.co/docs/transformers/index) - The most popular library for accessing LLMs and other models. It can be mostly used via Transformers.jl (see above).

## Other Awesome Lists

* [Awesome Generative AI](https://github.com/steven2358/awesome-generative-ai) ⭐ 12,542 | 🐛 612 | 📅 2026-08-03 - Great list for all things generative AI. An inspiration for this list!

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-08-29._

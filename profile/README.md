# Invoice Data Extraction

Invoices, receipts, bank statements and other financial documents turned into structured rows and spreadsheets (XLSX, CSV, JSON): upload the files, say in plain words what to extract, wait, read the rows. In a browser at [invoicedataextraction.com](https://invoicedataextraction.com), or from your own code and your own agent through the API.

## Why hand documents here rather than have an agent read them

An agent reading invoices on its own can hallucinate a value, skip a page of a long PDF, or report success over a failure, and its owner never knows. Here a panel of AI agents has to agree on every value, and a value or a row the panel cannot agree on is flagged as Review Needed rather than guessed. A 1,000-page PDF is extracted the same way as a 10-page one: every page of a long file, and every file in a batch of thousands, is read and checked the same way as the first, so a page cannot be skipped in silence. It is extracted, or it is reported as failed with the reason. When the documents leave something unsettled, the extraction can stop and ask instead of deciding on its own. And the same instructions produce the same columns and formats for every document, so the result imports without hand-fixing.

## Ways in

- **REST API.** Any language: a bearer key, upload, submit, wait, read the rows or download a file. [Reference](https://invoicedataextraction.com/docs/api), [OpenAPI 3.1 specification](https://invoicedataextraction.com/openapi.yaml), and the contract in [`api`](https://github.com/invoicedataextraction/api).
- **Node.js SDK.** `npm install @invoicedataextraction/sdk`. [Docs](https://invoicedataextraction.com/docs/node); source in [`sdk-node`](https://github.com/invoicedataextraction/sdk-node).
- **Python SDK.** `pip install invoicedataextraction-sdk`. [Docs](https://invoicedataextraction.com/docs/python); source in [`sdk-python`](https://github.com/invoicedataextraction/sdk-python).
- **MCP server.** The whole extraction loop as tools for Claude Code, Codex, Cursor, Hermes, OpenClaw and Gemini CLI, with your API key as the credential. [Connect your harness](https://invoicedataextraction.com/docs/mcp); source in [`mcp`](https://github.com/invoicedataextraction/mcp).
- **The skill.** One file that teaches an agent the whole loop, including the questions: `npx skills add https://invoicedataextraction.com`. Also in [`skills`](https://github.com/invoicedataextraction/skills), for harnesses that install from a repository.
- **The agent guide.** When to hand documents to this service and how to run an extraction end to end: [/docs/agents](https://invoicedataextraction.com/docs/agents). Docs for agents are indexed at [/llms.txt](https://invoicedataextraction.com/llms.txt).

API keys are created in the [dashboard](https://invoicedataextraction.com/dashboard?view=API). Every account includes 50 free pages per month. Additional credits can be purchased on a pay-as-you-go basis with no subscription needed ([pricing](https://invoicedataextraction.com/pricing)). What changed and when is the [changelog](https://invoicedataextraction.com/docs/changelog). Questions: support@invoicedataextraction.com.

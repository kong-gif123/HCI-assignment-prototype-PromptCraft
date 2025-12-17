# HCI-assignment-prototype-PromptCraft
Local-first prompt builder with real-time quality scoring and BYOK LLM generation.

Abstract

This repository contains the front-end implementation of PromptCraft delivered as a high-fidelity alpha build. In the course context, it serves as the “beta (code submission)” because it is the runnable coded deliverable; however, the system is implemented as a browser-based application without a dedicated backend. The current build completes client-side UI rendering (HTML/CSS/JavaScript), integrates audio and animation feedback using HTML5 Audio/Web Audio and CSS/Web Animations, supports Gemini API request/response rendering for prompt optimization, and includes a quantum-inspired local parallel analysis module to evaluate prompt quality on-device.

Entry points 

The repository provides two HTML entry pages for assessment and demonstration. The lab page (visual and audio API test.html) is a standalone implementation focusing on the sound and animation API requirements: users can toggle audio via the sound button at the top-right of the header, and the animation feedback is rendered synchronously to make the interaction observable. The main entry (index.html) presents the complete PromptCraft interactive prototype described in the report, allowing users to experience the end-to-end workflow including the landing page, template library, Gemini API call and optimized prompt rendering, sound control, and clearing locally stored records.

Scope note: this project intentionally runs fully in the browser and does not include a backend service. All interactions, rendering, and local analysis are performed client-side, while Gemini functionality is accessed via API calls from the front end as documented in the report.

Known issue during testing
During our testing, we observed that even when a valid Gemini API key is provided, the generation process may occasionally fail with messages such as “generation failed” or “the model is overloaded, please try again”.

This issue appears mainly during Gemini peak usage periods and is likely related to the recent release of the Gemini 3 model, which has significantly increased traffic. In most cases, no additional handling is required, as the service resumes normal responses after peak hours. Users with non-free API keys may experience fewer disruptions.

---
order: 1
---

# Generative Artificial Intelligence Usage Policy

This document defines the requirements for using generative artificial intelligence (Generative AI,
hereafter AI) during the development and maintenance of PCL CE. It covers usage disclosure,
contribution quality, automated actions, review procedures, and the handling of violations.

PCL CE allows contributors to use AI tools to assist with development, provided that all
contributions comply with the project's existing technical guidelines, quality requirements, and
contribution scope. AI tools do not replace the contributor's responsibility to understand, review,
and verify submitted content, nor do they replace maintainers in making project management
decisions.

This policy applies to everyone involved in PCL CE development, documentation, issue reporting,
technical discussions, or maintenance. Unless otherwise specified, "contributor" also includes
maintainers when they participate in project activities as contributors.

::: danger 🛑 Important 🛑
Using AI is not, by itself, a reason to reject a contribution. However, AI use does not justify
lower quality standards or exempt contributors from responsibility.

Contributions that do not comply with this policy may be returned for changes or closed directly.
Maintainers may restrict participation by contributors who seriously or repeatedly violate the
requirements.
:::

## Normative Terms

The normative terms in this document have the same meanings as those used in
the [Technical Guidelines](./guidelines.md):

| Term                | Meaning                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------|
| Must / must not     | Mandatory requirements that must be followed strictly.                                              |
| Should / should not | Default requirements that should be followed unless there is a clear reason not to.                 |
| Recommended         | Non-mandatory practices that usually help improve contribution quality or reduce maintenance costs. |
| May                 | Permitted practices that can be chosen according to the actual situation.                           |

## 1. Scope and Definitions

### 1.1 Scope

This policy applies to public contributions and maintenance activities related to PCL CE, including
but not limited to:

* Source code, test code, configuration files, and build scripts;
* Code comments, development documentation, user documentation, and translations;
* Images, icons, and other project assets;
* Issues, Pull Requests (hereafter PRs), discussions, and comments;
* Bug reports, security reports, and technical analyses;
* Code reviews, issue handling, and other project management activities performed by maintainers;
* Related operations performed using AI agents or automation tools.

Documentation contributions to PCLC Docs that directly concern PCL CE must also comply with this
policy. Such documentation must additionally follow
the [Writing Guidelines](../contributing/writing-guidelines.md).

This policy does not restrict personal AI use unrelated to contributions to or maintenance of the
project.

### 1.2 Definition of Generative AI

In this document, generative AI refers to systems that can generate, complete, rewrite, or analyze
code, natural-language text, images, or other content based on input.

Common forms of use include:

* Using tools such as ChatGPT, Claude, or DeepSeek to generate code or provide technical
  suggestions;
* Using language-model-based code completion tools such as GitHub Copilot;
* Using AI to analyze error logs, identify possible causes, or propose fixes;
* Using AI to translate, proofread, or rewrite natural-language text;
* Using AI to generate images, icons, or other assets;
* Using AI agents with autonomous planning and tool-calling capabilities to perform development
  tasks.

The following deterministic tools and features are generally not considered generative AI under this
policy:

* Traditional IntelliSense completion based on language rules or static analysis;
* Code formatters and static analysis tools;
* Ordinary scripts that execute predefined rules;
* .NET source generators and other deterministic compile-time code generation tools;
* Search, refactoring, and bulk-replacement features that do not use generative models.

If a tool feature actually relies on a generative model, it is subject to this policy even if it
resembles traditional completion, search, or refactoring.

### 1.3 Categories of AI Use

To distinguish different levels of AI involvement, this policy defines the following two categories:

| Category        | Definition                                                                                                                                         | Common examples                                                                                              |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Auxiliary use   | AI is mainly used for research, analysis, completion, translation, or proofreading, and does not perform the main implementation work directly.    | Looking up technical information, analyzing exceptions, limited code completion, text translation.           |
| Substantial use | AI generates or substantially rewrites code, tests, assets, or other content permitted for submission that is ultimately used in the contribution. | Generating a method implementation, refactoring an existing module, generating tests, creating image assets. |

Whether use is substantial must be determined by its actual effect on the final contribution, not
merely by the number of lines of code or the number of times a tool was used.

For example, if a contributor asks AI to design the complete implementation of a method and then
manually enters or makes minor adjustments to the generated result, this still counts as substantial
use.

These categories are used only to determine disclosure details and review requirements. All use of
AI must comply with this policy, regardless of category.

## 2. Fundamental Principles and Responsibility

### 2.1 Contributor Responsibility

Contributors remain the authors of, and are fully responsible for, the content they submit.

Regardless of the extent of AI involvement, contributors must:

* Understand the purpose, implementation, and scope of each change;
* Check the correctness of information, code, and technical suggestions provided by AI;
* Ensure that submitted content complies with the project's technical guidelines and existing
  architecture;
* Complete testing or other verification appropriate to the changes;
* Be able to explain key implementation details, exception handling, and known limitations;
* Correct errors introduced by the submitted content as necessary.

Contributors must not use AI output as a reason for not understanding the code or being unable to
resolve a problem. They must not use "AI suggested this implementation" as a substitute for a
specific technical justification.

Maintainers may ask contributors to explain any technical issue related to their submissions. If a
contributor cannot explain a key part of the implementation or demonstrate that the necessary
verification has been performed, maintainers may suspend review or close the PR.

### 2.2 Manual Review Requirements

AI-generated or AI-modified content must be reviewed by the contributor before submission.

Manual review should not be limited to confirming that code compiles or checking for obvious syntax
errors in generated content.

For code contributions, the review should also cover:

* Whether the APIs, types, and parameters used actually exist;
* Whether the implementation behaves as intended;
* Whether exceptions and boundary conditions are handled correctly;
* Whether the implementation duplicates existing project functionality;
* Whether unnecessary abstractions, dependencies, or state have been introduced;
* Whether existing functionality, performance, or compatibility may be affected;
* Whether the changes include code unrelated to the stated objective.

Technical claims made by AI must be verified against source code, official documentation, test
results, or other reliable evidence.

AI output must not be treated as verified fact.

### 2.3 Quality Standards

AI-assisted content is subject to the same quality standards as other contributions.

AI use does not justify lower requirements for testing, maintainability, or documentation quality.
Conversely, contributions that do not use AI are not exempt from normal review.

Contributions must address actual project needs. Content must not be added merely because AI can
generate an implementation for it.

The project is in maintenance mode. New contributions must still align with its current focus on bug
fixes and improvements to existing functionality. Compliance with this policy does not guarantee
that a contribution will be accepted or merged.

### 2.4 Contribution Value and Maintenance Costs

Contributors should ensure that submitted changes provide clear value and that their review and
long-term maintenance costs remain reasonable.

For contributions that require substantial maintainer effort to understand, verify, or reorganize
despite offering limited practical benefit, maintainers may request a narrower scope, additional
explanations, or a new implementation.

Contributors should not submit large amounts of unorganized AI-generated content and expect
maintainers to perform basic debugging, code review, or solution design on their behalf.

Maintainers are not obligated to perform a complete line-by-line review of contributions that have
not received the necessary review by their submitters.

## 3. Disclosure of AI Use

### 3.1 General Requirements

Any use of generative AI during project contributions or maintenance must be disclosed.

Disclosure requirements apply to all relevant AI use, including:

* Limited code completion based on language models;
* AI-assisted research, issue analysis, and debugging;
* AI-generated code or substantial code modifications;
* AI-assisted translation and grammar correction;
* AI-assisted generation of images or other assets.

Use of traditional IntelliSense, deterministic formatting tools, or ordinary scripts does not need
to be disclosed under this policy.

The purpose of disclosure is to provide maintainers with the context needed for review. Disclosing
AI use does not, by itself, indicate a violation.

### 3.2 Model Identifier in PR Titles

A PR that uses generative AI must have a model identifier appended to the end of its title, so
maintainers can identify the model directly from the PR list.

Use the following format:

```text
[Model_Name-Version]
```

Examples:

```text
[DeepSeek-V4.1-flash]
[Claude-Opus-5.5]
[GPT-6.1-sol]
```

PR titles must still comply with the commit message format specified in
the [Technical Guidelines](./guidelines.md#simple-format).

For example:

```text
fix(download): fix retrying logic after download failed [GPT-5.1]
```

Documentation changes that use AI only for translation must also include a model identifier:

```text
docs: fix English translation in the Installing Guide [Claude-Opus-4.6]
```

The model name and version must reflect actual use. Do not invent a model name or provide version
information that has not been confirmed.

If the tool does not provide the exact model name or version, use a name that clearly identifies the
tool, such as:

```text
[GitHub-Copilot]
```

In this case, explain in the PR description that the exact model version could not be confirmed.

If multiple models are used in the same PR, identify the model that had the greatest impact on the
final contribution in the title, and list the other models and their purposes in the PR description.
Multiple model identifiers may also be included in the title if its length permits.

The same identifier may be retained at the end of a Git commit message, but this does not replace
the requirement to include it in the PR title.

::: tip Note
The model identifier indicates AI involvement and is not part of the change summary. The title must
still describe the actual change concisely and accurately.

Commit messages must continue to comply with the project's existing length limits and formatting
requirements.
:::

### 3.3 AI Usage Disclosure in PR Descriptions

Every PR must explicitly declare whether AI was used, including contributions that did not use AI at
all.

The PR template should provide a standardized section such as:

```text
### AI Usage Disclosure

- Usage: Not used / Auxiliary use / Substantial use
- Tool and model:
- Purpose:
- Scope:
- Manual review and verification:
```

The following requirements apply:

* If no AI was used, select "Not used". The remaining fields may be omitted.
* For auxiliary use only, identify the tool and its main purpose. There is no need to record every
  code completion or model call individually.
* For substantial use, identify the tool and model, the scope of generated or modified content, and
  the manual review and verification performed.

If the model version cannot be confirmed, state this explicitly rather than guessing.

Disclosure of substantial use must give maintainers enough information to determine what work AI
contributed to and whether the relevant content has been verified.

The following generally do not need to be provided:

* Complete AI conversation logs;
* The exact content of every code completion;
* Prompts unrelated to the final contribution;
* The model's internal reasoning process;
* Original input containing personal information, credentials, or other sensitive content.

Maintainers may request additional information where necessary, but should not require contributors
to disclose content that could expose sensitive information.

### 3.4 Disclosure for Other Public Contributions

AI use must also be disclosed for Issues, discussions, and comments that are not submitted through a
PR.

Disclosure may be provided through the relevant template or a brief statement. It should identify at
least the tool or model used and its purpose.

For example:

```text
GPT-5.1 was used to assist with analyzing the exception logs. I reproduced the issue myself.
```

```text
This comment was translated with assistance from Claude. I wrote and verified the technical content.
```

Maintainers must also disclose AI use when it assists in preparing public review comments or
technical conclusions.

AI use in a private environment is outside this disclosure requirement when it is unrelated to
project contributions, public feedback, or maintenance decisions.

### 3.5 Accuracy of Disclosure

Contributors must not conceal AI use directly related to a contribution, provide intentionally
incorrect model information, or describe substantial AI generation as limited code completion.

If AI is used after a PR has been opened, the relevant disclosure must be updated promptly.

If maintainers have reasonable questions about a disclosure, they may ask the contributor for
clarification. However, they must not conclude that a contributor concealed AI use solely on the
basis of code style, wording, or the results of an AI detector.

## 4. Requirements for Different Types of Contributions

### 4.1 Source Code

AI-assisted code generation or modification must comply with the project's
existing [Technical Guidelines](./guidelines.md).

Submitters should prioritize the project's existing architecture, utility methods, and
implementation patterns. They should not introduce new abstraction layers, design patterns, or
third-party dependencies solely because AI recommends them.

The following must not be submitted:

* Code that uses nonexistent APIs, types, or parameters;
* Incomplete logic, implementations with obvious behavioral errors, or code that lacks necessary
  exception handling;
* Unverified third-party code or dependencies;
* Implementations that duplicate existing functionality without a clear need;
* Unorganized placeholders, ineffective branches, or leftover debugging code;
* Code whose purpose or behavior the author cannot explain.

AI-assisted changes should be limited to the minimum scope necessary. They should not include
extensive renaming, formatting, migration, or refactoring unrelated to the actual objective.

If an AI-generated solution clearly deviates from the project's existing implementation patterns,
contributors should first consider whether a simpler solution would be more appropriate instead of
introducing the generated result directly.

### 4.2 Code Comments

New comments should primarily explain why an implementation is necessary, document special
constraints, or clarify behavior that cannot easily be inferred from the code itself.

Do not add large amounts of repetitive explanation to self-explanatory code, or introduce
documentation comments that do not match the actual implementation.

The following practices should generally be avoided:

* Adding comments to explain every simple assignment, conditional, or method call;
* Adding section comments or decorative banners that provide no useful information;
* Adding unverified descriptions of parameters, return values, or exceptions;
* Retaining placeholder `TODO`, `FIXME`, or implementation notes generated by AI;
* Adding large amounts of repetitive explanation where the surrounding code style does not call for
  it.

Code comments are part of the project's technical documentation. Contributors must write them based
on their understanding of the actual implementation. AI may be used for translation or grammar
correction, but must not replace the contributor's responsibility to explain code they do not
understand.

### 4.3 Test Code

AI-assisted tests must verify actual behavior. Tests must not be added merely to increase coverage
numbers or make CI pass.

When adding or modifying tests, contributors must follow these requirements:

* Tests should check behavior or results that have practical significance;
* Assertions must effectively verify the expected behavior;
* For a bug fix, tests should, where possible, fail before the fix and pass after it;
* Tests should not duplicate scenarios already adequately covered by existing tests;
* Tests should not rely excessively on internal implementation details unrelated to the test
  objective;
* Test style should be consistent with existing tests in the same project or directory;
* New test frameworks or dependencies should not be introduced solely because AI recommends them.

Existing tests must not be modified without justification, skipped, deleted, or weakened merely to
conceal implementation errors or make CI pass.

If an existing test must be modified or removed, the contributor must explain what behavior it
covered, why the change is necessary, and how that behavior will continue to be verified.

If automated tests cannot reasonably be written, the contributor should describe the alternative
verification method used.

Contributors must not claim that tests passed when they were not actually run, or submit
AI-generated test results as evidence of verification.

### 4.4 Documentation and Other Public-Facing Text

Public-facing text intended for project members or users must be written by the contributor.

AI may only be used to translate an existing human-written original, or to correct spelling,
grammar, and language without changing the original meaning. It must not draft or substantially
rewrite public-facing text on the contributor's behalf.

This requirement applies to:

* PR titles, descriptions, and review replies;
* Issues, discussions, and comments;
* Git commit messages;
* Development documentation, user documentation, and release notes;
* Code comments and other technical explanations.

Do not submit long explanations, issue reports, technical comments, or documentation body text
generated by AI. Minor edits to AI-generated text do not count as human authorship.

AI may be used privately to research information, analyze a technical issue, or identify textual
errors, but contributors must independently verify the relevant information and write the final
content in their own words.

AI-assisted translations must be proofread manually to ensure that the terminology, meaning, and
context are accurate. They must not introduce facts or conclusions absent from the original text.

Public-facing text must follow the project's existing documentation style and use concise, accurate
wording.

The following should not appear in formal contributions:

* Generalized summaries that contain little specific information;
* Redundant lists that repeat the same points;
* Technical conclusions or subjective assessments without supporting evidence;
* Generic explanations that do not reflect the actual project;
* Excessive hedging or unnecessary qualifications;
* Translations or terminology that clearly do not fit the context.

Maintainers should review public-facing text based on its accuracy, information value, clarity, and
actual content. They must not infer AI authorship solely from wording or style.

### 4.5 Issues and Problem Reports

Using AI to help analyze bugs or security issues is permitted, but reporters must independently
verify the relevant conclusions.

A bug report should include, where possible:

* The actual problem and the expected behavior;
* The affected version and runtime environment;
* Reproducible steps;
* The observed result that has been confirmed;
* Relevant logs, screenshots, or other evidence.

AI-generated speculation about source code or logs must not be submitted as a confirmed issue
without verification.

For potential security issues identified with AI assistance, reporters must examine the relevant
code and triggering conditions themselves, and submit the necessary information through the
project's designated non-public security reporting channel.

If an issue cannot yet be reproduced, the reporter must state which parts remain unconfirmed. Do not
fabricate reproduction steps or present speculation as established fact.

Using AI to generate large numbers of duplicate, unsupported, or unverified Issues is prohibited.

### 4.6 Images and Other Assets

AI may be used to help create images, icons, or other assets, provided that the results meet the
project's copyright, quality, and practical requirements.

Submitters must confirm that the assets are suitable for their intended use and are responsible for
their content and origin.

The following must not be submitted:

* Generated assets containing obvious errors or unsuitable for their intended purpose;
* Third-party materials whose usage rights cannot be confirmed;
* Trademarks, logos, or protected content used without authorization;
* Assets containing information that must not be disclosed or content that could be misleading.

For AI-generated assets, the submission description must identify the tool used, the scope of
generated content, and any relevant post-processing.

## 5. Contribution Size and Review Requirements

### 5.1 Pre-submission Checks

All contributions must receive the necessary self-review before maintainers are asked to review
them.

For code PRs, submitters should be able to explain at least:

* The specific problem addressed by the change;
* The main implementation approach and why it was chosen;
* The functionality affected and the potential impact;
* The tests or other verification performed;
* Any unresolved issues or known limitations.

For contributions involving substantial AI use, submitters must also explain what manual checks were
performed on the generated content.

If a contribution lacks information necessary to understand the changes, maintainers may request
additional explanations and defer further review.

### 5.2 Definition of a Large PR

A PR should be treated as large if either of the following conditions is met:

* More than 200 lines of code are added or modified in a single PR;
* More than 5 `.cs` or `.xaml` files are involved in a single PR.

The line count must be calculated as the total number of added and deleted lines in the PR diff,
rather than the net increase in line count.

For generated files or other purely mechanical changes, maintainers may decide whether to exclude
them from the size calculation. Such changes must still receive the necessary review.

These limits apply to the PR as a whole. Splitting a large change into multiple Git commits does not
reduce the overall review scope of the PR.

### 5.3 Large AI-assisted Contributions

PRs that exceed either size threshold and contain substantially AI-generated content should, in
principle, be split into smaller PRs that can be reviewed, verified, and merged independently before
formal review.

Each resulting PR should have a clear objective and should avoid unnecessary dependencies on other
PRs that have not yet been merged.

Do not circumvent the size requirements by splitting commits, hiding unrelated changes, or using
other means to obscure the overall scope.

If technical constraints prevent a change from being reasonably split, the submitter must explain
why and obtain maintainer approval before requesting formal review.

Maintainers may require the author to provide more detailed implementation explanations,
verification results, or a step-by-step explanation of the relevant code.

Large AI-generated contributions that have not been adequately organized and verified may be
rejected outright.

### 5.4 Conditions Requiring Strict Review

A PR should undergo strict review if any of the following conditions apply:

* The change exceeds the size limits specified in this section;
* The change affects security-sensitive logic, such as account authentication, credential handling,
  the updater, signature verification, or download integrity;
* Existing tests are deleted, refactored, or substantially modified;
* Maintainers consider the review or long-term maintenance burden to be excessive;
* Maintainers determine that additional verification is necessary based on implementation
  complexity, risk, or the extent of AI involvement.

Contributions involving substantial AI use must include detailed disclosure and appropriate manual
verification, but substantial AI use alone does not automatically require the full strict-review
process.

For example, a small amount of AI-assisted code that has been adequately verified may undergo normal
review. A small change affecting security-sensitive logic may still require strict review.

### 5.5 Strict Review Procedure

PRs undergoing strict review must complete the following steps as required by maintainers:

1. Split changes that can be reviewed independently into smaller PRs, or explain why they cannot
   reasonably be split.
2. Provide the motivation for the change, the main implementation approach, and the scope of its
   impact.
3. Provide test results and verification methods appropriate to the changes.
4. Explain key logic, exception handling, and failure boundaries.
5. Modify the implementation or provide additional evidence in response to maintainer feedback.

Maintainers may require contributors to explain the relevant code step by step in their own words,
including specific code paths, key branches, data flow, and design decisions.

The explanation may be provided through PR comments, a technical write-up, or another method
accepted by both parties. A live meeting or video demonstration is not required.

A PR must not be merged while key questions raised during strict review remain unresolved.

At least one maintainer responsible for the review must confirm that they understand the significant
changes and consider the available verification sufficient to support merging.

### 5.6 Contributions with Disproportionate Review Costs

Maintainers may determine that a contribution has excessive review costs when the effort required to
review and maintain it is clearly disproportionate to its expected value.

Common examples include:

* Introducing a large refactoring for a simple problem without sufficient justification;
* Using excessive abstractions or helper code to implement an otherwise simple feature;
* Duplicating existing functionality without explaining the practical benefit;
* Submitting large amounts of unverified implementation that require maintainers to investigate each
  part;
* Making changes far beyond the scope required to address the actual problem;
* Repeatedly failing to explain the implementation or provide effective verification.

This assessment must not depend on whether AI was used.

Maintainers should explain the main concerns and may ask the contributor to reduce the scope,
reorganize the changes, or provide additional verification.

If the issues cannot be resolved, or further review no longer offers reasonable value, the PR may be
closed.

### 5.7 Review Labels

Maintainers may use the following labels to manage PRs:

| Label      | Meaning                                                                                                                                       |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `AI 辅助`  | The contributor has disclosed AI use. This label indicates usage only and does not imply a violation.                                         |
| `需要解释` | The author must provide additional technical explanations or explain the relevant code step by step.                                          |
| `成本过高` | The review and maintenance costs are disproportionate to the contribution's value, so the contribution needs to be reorganized or reassessed. |

Labels indicate review status or relevant information and must not be used as a direct basis for
punishment.

The `需要解释` label may be removed after the author provides sufficient explanations. The
`成本过高` label may be removed after the author has meaningfully reduced the scope, provided
additional verification, or resolved the main concerns.

## 6. AI Agents and Automation

### 6.1 Permitted Assisted Operations

Contributors may use AI agents under human supervision for local development tasks, including:

* Reading and analyzing source code;
* Searching for call relationships and related implementations;
* Proposing implementation approaches;
* Generating or modifying local code;
* Running local builds, tests, and static analysis;
* Organizing technical information for the contributor to review.

Using an agent for these tasks does not exempt the contributor from the requirements to understand,
verify, and disclose the work.

Submitters must inspect the actual changes made by an agent. They must not assume that a task was
completed correctly based only on the agent's completion report.

### 6.2 Prohibited Autonomous Actions

Without explicit human action and confirmation, AI agents must not autonomously:

* Create or submit PRs to the project;
* Create Issues or publish discussions;
* Publish PR review comments or other public replies;
* Approve, merge, or close PRs;
* Make project management decisions on behalf of maintainers;
* Perform repository administration beyond the authorized scope.

Do not circumvent these requirements for human involvement by automatically approving an agent's
operation requests.

Content published by a human must still comply with the requirements for public-facing text. A human
clicking a publish button does not, by itself, constitute sufficient review.

### 6.3 Commit Identity and Signatures

The project requires Git commits to have verified signatures.

Submitters must not allow AI agents to hold or manage their personal signing private keys, or use
those keys to sign commits autonomously.

Personal access tokens, repository administration credentials, and other sensitive credentials must
not be provided directly to agents that are not appropriately restricted.

All commit and release actions that require confirmation of a contributor's identity must involve a
human with the appropriate permissions, who remains responsible for the action.

### 6.4 Automation Exceptions

Existing deterministic automation, including preconfigured build and test workflows and other
routine CI tasks, is not subject to the restrictions on autonomous AI agents described above.

Automation explicitly approved by maintainers, with a defined execution scope and an assigned person
responsible for it, may be handled separately according to the actual requirements.

Such exceptions do not permit autonomous agents to create contributions, publish comments, or modify
project content without restriction.

AI-based automation must still comply with the relevant security, information protection, and
quality requirements.

### 6.5 AI Use by Maintainers

Maintainers may use AI to assist with source code analysis, technical research, troubleshooting, and
internal review.

However, AI must not replace maintainers in making decisions about merging, closing, imposing
restrictions, or other project management matters.

Maintainers must verify AI-generated review comments and must not ask contributors to make changes
based directly on unverified model conclusions.

Public review comments and project management replies must be written by the maintainer. AI may only
be used for translation or grammar correction, and such use must be disclosed under this policy.

AI detectors or model-generated speculation must not be used as the sole basis for determining that
a contributor has violated this policy.

## 7. Copyright, Security, and Content Integrity

### 7.1 Copyright and Licenses

AI-generated content must not be assumed to be free of copyright restrictions or exempt from the
project's existing license requirements.

Submitters must ensure that code, assets, and dependencies they introduce comply with the license
applicable to the relevant file or directory and with any other relevant requirements.

The licenses for the PCL CE main repository are determined by the declarations actually present in
the repository. The `Plain Craft Launcher 2/` directory is subject to its separately declared
license; all other directories are subject to the repository's declared Apache License 2.0.

Other repositories and documentation must comply with their respective applicable licenses.

The following are prohibited:

* Copying third-party code suggested by AI without verifying its source and license terms;
* Presenting third-party content subject to license restrictions as original AI-generated content;
* Removing or modifying existing copyright notices or license information without authorization;
* Introducing images, icons, or other assets whose usage rights cannot be confirmed;
* Using AI to fabricate source information, authorship, license terms, or authorization details.

If AI recommends introducing a third-party dependency, the submitter must independently confirm that
the dependency exists and verify its maintenance status, purpose, and license compatibility.

If the right to use relevant content cannot be confirmed, that content must not be submitted to the
project.

### 7.2 Protection of Sensitive Information

Sensitive information must not be submitted to third-party AI services without authorization.

Such information includes, but is not limited to:

* User accounts, access tokens, and authentication credentials;
* Private keys, signing material, and other security credentials;
* Logs or configuration files containing personal information;
* Details of security vulnerabilities that have not yet been disclosed publicly;
* Project information that must not be disclosed to third parties.

Before using AI to analyze logs, configuration files, or error reports, contributors must check for
and remove information that must not be shared externally.

Users remain responsible for protecting information even when an AI tool reads or uploads data
automatically.

### 7.3 Integrity of Content and Evidence

All technical facts, test results, and evidence submitted to the project must be truthful and
verifiable.

It is strictly prohibited to use AI to fabricate or falsify:

* Error logs and terminal output;
* Bug reproduction steps or reproduction results;
* Test records and CI results;
* Performance benchmark data;
* Screenshots, recordings, or other materials used as evidence;
* Third-party documentation, citations, or technical references.

AI may assist with analyzing real data, but fabricated data must not be presented as the result of
actual execution.

Speculative conclusions must clearly identify what has not been verified.

Intentionally fabricating or falsifying evidence constitutes a serious violation. Maintainers may
impose participation restrictions directly.

## 8. Handling Violations and Review of Decisions

### 8.1 General Principles

Maintainers should determine how to handle a violation based on the specific conduct, its impact,
and the contributor's cooperation.

Decisions should, where possible, be based on facts that can be clearly identified, such as:

* Missing required AI disclosure;
* Submitted content that does not meet technical or quality requirements;
* An author who cannot explain a key part of the implementation;
* Failure to complete necessary verification;
* Use of an AI agent to perform prohibited autonomous actions;
* Fabrication of technical evidence or disclosure of sensitive information;
* Repeated submission of contributions that clearly fail to meet the requirements.

Maintainers must not impose penalties solely because code appears to have been generated by AI or
because of the results of an AI detector.

### 8.2 Requesting Changes

For ordinary issues that can be corrected, maintainers should generally ask the contributor to make
changes first.

Examples include:

* Missing model identifiers or AI usage disclosures;
* PR descriptions that lack necessary verification information;
* Obvious quality problems in AI-assisted code that can be corrected;
* Changes that are too broad and need to be split;
* Technical explanations that the author has not yet provided.

Maintainers may suspend review after requesting changes until the relevant issues have been
resolved.

### 8.3 Closing a Contribution

Maintainers may close a PR or Issue in the following situations:

* The contributor does not correct obvious problems as requested;
* The author cannot explain an important part of the implementation;
* The contribution provides insufficient value or does not align with the project's maintenance
  direction;
* The contribution still fails to meet the required quality standards after repeated revisions;
* Further review would require a clearly unreasonable amount of maintainer effort;
* The contribution has a serious problem that cannot be resolved through ordinary changes.

Maintainers may close contributions directly without completing a full technical review if they lack
basic verification, clearly fail to meet contribution requirements, or involve serious violations.

When closing a contribution, maintainers should explain the main reason or refer to the relevant
requirement where possible.

### 8.4 Restricting Participation

The project may restrict a contributor's further participation in repository activities for serious
or repeated violations of this policy.

Examples include, but are not limited to:

* Repeatedly submitting large amounts of AI-generated content without review;
* Repeatedly circumventing disclosure or review requirements;
* Using agents to publish large numbers of Issues, PRs, or comments;
* Intentionally fabricating logs, test results, or other evidence;
* Intentionally disclosing sensitive information;
* Continuing the same violations after receiving an explicit warning.

For serious violations, maintainers may skip the ordinary change-request or closure process and take
appropriate action directly.

The scope and form of restrictions must be determined according to the actual impact and the
project's management permissions. Organization-level blocking must be carried out by personnel with
the required permissions and in accordance with the organization's management procedures.

### 8.5 Review of Decisions

Contributors who disagree with a handling decision may explain their reasons and request a review by
maintainers.

The review should focus on whether the relevant rules were applied correctly and whether the facts
supporting the original decision were sufficient.

Where necessary, other maintainers who were not directly involved in the original decision may
assist with the review.

Requesting a review does not automatically revoke the original decision or require the project to
accept the original contribution.

### 8.6 Exceptions

If a contribution has a genuine technical need that makes it impossible to follow the ordinary
process in full, the contributor may explain the reason to maintainers and request an exception
before submitting it.

Exceptions must apply to a specific contribution and a clearly identified technical issue. They must
not be used as a way to circumvent this policy on an ongoing basis.

Maintainers may adjust the required change scope, review method, or verification requirements as
appropriate. However, such adjustments must not waive the basic requirements for author
responsibility, content integrity, license compliance, or information security.

## Appendix: Common Scenarios

| Scenario                                                                                | Permitted?    | Main requirements                                                                   |
|-----------------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------|
| Using GitHub Copilot for limited code completion                                        | Yes           | Disclose AI use and check the completed code.                                       |
| Using AI to look up API usage                                                           | Yes           | Disclose the use and independently verify the technical information.                |
| Using AI to generate a complete method                                                  | Yes           | Provide detailed disclosure, manually review the code, and complete verification.   |
| Generating a large amount of code with AI and submitting it directly                    | No            | Understand and organize the code first, then meet the size and review requirements. |
| Using AI to analyze maintainer review comments                                          | Yes           | Understand the issue and independently verify the changes.                          |
| Passing review comments directly to an agent to modify the code and reply automatically | No            | Do not bypass human understanding, verification, and communication.                 |
| Using AI to translate documentation written by the contributor                          | Yes           | Disclose the use and proofread the translation manually.                            |
| Using AI to draft a PR description and submitting it directly                           | No            | PR descriptions must be written by the contributor.                                 |
| Generating documentation text with AI, then making only minor edits before submission   | No            | Minor edits do not replace human authorship.                                        |
| Using AI to help analyze Bug logs                                                       | Yes           | Disclose the use and confirm the analysis independently.                            |
| Using AI to generate an unverified Bug report                                           | No            | Do not present speculation as a confirmed issue.                                    |
| Using AI to help write tests                                                            | Yes           | Verify that the tests are effective and do not fabricate execution results.         |
| Using AI to help generate icons                                                         | Conditionally | Verify copyright, quality, and usage rights.                                        |
| Using an agent to modify code locally                                                   | Yes           | Supervise the agent and inspect all changes before submission.                      |
| Allowing an agent to create PRs or publish comments autonomously                        | No            | Public contributions and communication must remain the responsibility of a human.   |
| Using AI to assist maintainers with review                                              | Yes           | Verify model conclusions, make decisions as a human, and disclose the use.          |

This policy applies from its formal publication date to newly created contributions and to existing
contributions that receive substantive updates after that date.

The project may revise this policy in response to maintenance needs and developments in AI tools.
Substantive changes to contributor obligations, prohibited conduct, or handling of violations must
be published through an official documentation update.

Related technical guidelines, PR templates, and contribution instructions must remain consistent
with this policy. If older AI usage requirements in other documents conflict with this policy, this
policy takes precedence.

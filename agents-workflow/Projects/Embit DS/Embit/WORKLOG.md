# Selected Embit work record

> Edited public selection from the reviewed case, not a verbatim dump of the live worklog. Original dates, sequence and unresolved items are retained. E01–E09 resolve to the evidence index in the repository README. No full project log is included.

## Selected work record

This record is an English summary derived from Spanish work logs, the component contract and saved Figma-check output. It preserves their order and attribution. It does not reconstruct missing chat messages. Times below are the times recorded in the work log, not independently measured execution timestamps.

| Date / recorded time | Request, action or correction | Attribution | Evidence |
|---|---|---|---|
| 13 October | Changelog 7.7.0 was assembled. Its source period was 8–13 October; the sample does not assign all of that work to the 13th. | Recorded changelog work | [E01](../../../../README.md#e01-period-and-previous-cut) |
| 14 October | A separate maintenance task restored 75 missing Button Label references. This is context, not the source of the contrast improvement. | Javier's request; agent execution reported in the work log | [E09](../../../../README.md#e09-optional-label-context) |
| 15 October, before integration | A temporary comparison showed the existing and proposed Brand A Light CTA colours. At this point it was a proposal, not an applied change. | DS work record | [E02](../../../../README.md#e02-decision-and-scope) |
| 15 October, approved work order | Javier approved the contextual ramp selection. The Deputy's recorded work order bounded the components, states, contexts and properties to preserve. | Javier: decision; DS Manager Deputy: work order | [E02](../../../../README.md#e02-decision-and-scope) |
| 15 October, 12:08 | Preflight read completed after a first response exceeded the output limit. A smaller read returned the required data; no mutation was reported at this stage. | Worker, GPT-6.1 Sol, high effort | [E03](../../../../README.md#e03-preflight) |
| 15 October, 12:16 | Variables and selected root fills were updated. A separate readback checked bindings, contexts and invariants. | Same Worker | [E04](../../../../README.md#e04-application-and-readback) |
| 15 October, 12:20 | Button instance checks completed: 120 size/state/context combinations; no failures in the saved output. | Same Worker | [E05](../../../../README.md#e05-button-instance-checks) |
| 15 October, 12:23 | Button Icon completed its first 120 combinations. Its touch-area check reported 25 failures. The Worker did not treat them as proof of a master defect. | Same Worker | [E06](../../../../README.md#e06-a-test-that-needed-correction) |
| 15 October, before 12:30 | The Deputy corrected the criterion: inspect Overlay visibility, not disappearance of the container. | DS Manager Deputy | [E06](../../../../README.md#e06-a-test-that-needed-correction) |
| 15 October, 12:30 | The Worker inspected the layers, completed the remaining 120 Button Icon combinations and checked the corrected touch-area behaviour. Temporary QA instances were removed. | Same Worker | [E06](../../../../README.md#e06-a-test-that-needed-correction), [E07](../../../../README.md#e07-cleanup-and-reproduction) |
| 15 October, 12:35 | The historical CTA comparison was removed after the result was recorded. | Same Worker | [E07](../../../../README.md#e07-cleanup-and-reproduction) |
| 15 October, changelog work opened at 16:26 | The recorded change entered changelog 7.8.0. The contract documents the later, limited replacement of the old exception. | Changelog and contract records | [E08](../../../../README.md#e08-documentation-after-the-change) |

The saved counters report 360 size/state/context combinations in total: 120 Button and 240 Button Icon. This is not a set of 360 individually recorded results or unique renders, and it does not mean the first test run had no failures. The 25 initial Touch Area flags and the later corrected check remain part of the record. [E05](../../../../README.md#e05-button-instance-checks), [E06](../../../../README.md#e06-a-test-that-needed-correction).

### Open at this cut

- At the historical cut, the later Figma sample and external viewing check had not yet been prepared. The component sample above was prepared and checked afterwards.
- Native interaction and full accessibility behaviour are not certified by this work.
- Library publication, downstream receipt and code use are not established by these sources.
- Other DS maintenance remained outside this selection. It is not closed by the sample.
- The Label example is optional. Its original saved output has not yet been independently checked for this extraction.



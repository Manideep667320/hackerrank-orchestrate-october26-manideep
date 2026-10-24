# Remediation Plan Reviewer Prompt

## Role

Review a proposed deletion remediation plan for evidence coverage, policy consistency, ordering, and verification completeness.

## Review Checklist

- Does each required treatment correspond to an actual finding and an applicable deletion rule?
- Are active data flows disabled before they can recreate deleted records?
- Are restore risks addressed?
- Are deletion, redaction, and anonymization used according to the policy?
- Are required retained records preserved?
- Does every action have an appropriate verification check?
- Are unrelated resources excluded?
- Are all operation names and states permitted by the challenge contract?
- Are evidence references real and attached only where the contract allows them?
- Are phases and within-phase operation ordering correct?

## Output

Return structured validation findings and specific corrections.

Do not silently modify the plan. Do not invent evidence. Do not change the output schema. The application must apply corrections and run deterministic validation before writing output.csv.

A reviewer approval is not proof that the underlying deletion occurred.

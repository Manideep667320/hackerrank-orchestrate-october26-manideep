# Verification Agent Specification

## Mission

Check whether the proposed final result is justified by the evidence and conforms to the challenge contract.

## Verification Responsibilities

1. Check that every required resource treatment is satisfied.
2. Check that no active sync, import, or restore path can recreate prohibited data.
3. Check that retained records satisfy the applicable identifier restrictions.
4. Check that required retained records remain available.
5. Check that every finding and completed verification references valid evidence.
6. Check that proposed remediation steps use the required empty evidence reference where specified.
7. Check phase ordering, operation ordering, resource sorting, and consecutive step numbering.
8. Reject unsupported claims and unresolved critical gaps.
9. Validate the deletion status against the structured findings.

## Decision Constraints

- `COMPLETE` requires all applicable completion conditions to pass.
- `INCOMPLETE` applies when a deletion was requested but required treatment or controls remain unsatisfied.
- `NOT_APPLICABLE` applies when deletion was not requested.
- Inability to establish a required condition must never be silently converted into success.

## Output

Return validation errors, evidence gaps, policy inconsistencies, and a proposed pass/fail result.

The final status must be computed by the application using validated evidence and policy decisions, not accepted solely from free-form model text.

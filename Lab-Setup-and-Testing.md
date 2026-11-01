# Day 13 — Local Web Security Lab

Use OWASP Juice Shop, an intentionally vulnerable training application, only in a local authorized lab.

## Requirements
Docker Desktop/Engine, a browser and permission to use the computer.

## Start the lab
```bash
docker pull bkimminich/juice-shop
docker run --rm --name juice-shop -p 127.0.0.1:3000:3000 bkimminich/juice-shop
```
Open `http://127.0.0.1:3000`. Keep the terminal open. The 127.0.0.1 binding restricts access to the same computer.

Stop with Ctrl+C. Do not expose this training app to the internet or a shared network.

## Safe workflow: Identify → Test → Fix → Document
1. Confirm the target is your local Juice Shop.
2. Read the relevant official companion-guide exercise.
3. State expected secure behaviour.
4. Perform the lab-authorized exercise.
5. Record actual result and evidence.
6. Recommend a defensive fix.
7. Retest if you have made a fix.

| Test | Activity | Record |
|---|---|---|
| LAB-01 | Browse local app features | Pages observed |
| LAB-02 | Inspect normal browser requests | Method, status, content type |
| LAB-03 | Review login/logout behaviour with a lab account | Expected vs observed |
| LAB-04 | Follow a guided access-control challenge | Steps, evidence, result |
| LAB-05 | Study a guided input-handling challenge | Input/output behaviour |
| LAB-06 | Observe normal invalid-input/error behaviour | Error and information exposure |

## Observation template
- Test ID:
- Date:
- Target: 127.0.0.1:3000
- Purpose:
- Steps:
- Expected result:
- Actual result:
- Evidence filename:
- Status: Not tested / Not observed / Confirmed / Needs verification
- Suggested remediation:

Save your own screenshots in `../screenshots/Day-13/`. Never use internet images as proof of your work.

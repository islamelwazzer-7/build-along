# ClinicDesk — examples for Build Along

Read the files from the user's copy of the ClinicDesk release. `START_HERE_AR.html` is the practical guide. `INSTALL_ASSISTANT_AR.md` supplies the installation workflow when the user requests setup. `FIRST_TEST_AR.md` defines the acceptance test. Use the examples below to teach the steps supported by that release and current evidence.

## State and Google Sheets

- **State Engine and the n8n Data Table.** The Data Table keeps the current conversation state inside n8n. When the installation sets a filter with `id` equal to `1`, explain how it selects the specific initial row prepared in the guide. The guide supplies its manual seed values. Check that the intended row is selected before moving on.
- **Clinic data and Google credentials.** The spreadsheet ID points to a specific spreadsheet. The Google credential gives the workflow permission to access it. Demonstrate by checking that n8n reads the intended spreadsheet and tab. A successful read establishes read access. Verify write access with an authorized synthetic visit.

## WhatsApp and the temporary setup workflow

- **Webhook.** Explain it as an address where Evolution delivers an incoming WhatsApp event to the main n8n workflow. Use the Production URL from that workflow. The current guide generates `Run setup once → Save Evolution Webhook` in a temporary workflow, which saves the callback in Evolution. Match the header auth on both sides using the guide and keep secrets out of screenshots and logs.
- **Verify at two points.** A saved callback setting confirms the configuration write. A new test message appearing in the main n8n workflow and a reply arriving back on the test phone confirms the inbound and outbound path. For a visit, also verify that exactly one row was written and that the day and visit number match the reply and optional Telegram alert.
- **Read an error by its source.** If the Gemini request records `503 UNAVAILABLE` and the flow later shows `C06 Needs Team Review`, explain the upstream service failure and the downstream alert separately. Check the current execution before applying this diagnosis to another run.

## Sample explanation in Egyptian Arabic

> «معرّف الشيت زي عنوانه. بيقول لـn8n يفتح أنهي شيت. اعتماد جوجل هو الإذن اللي يخليه يفتحه. نجرب القراءة الأول ونشوف البيانات جاية من التبويب الصح. ولما نيجي نجرب الكتابة، هنعمل زيارة ببيانات وهمية ونتأكد إنها نزلت مرة واحدة.»

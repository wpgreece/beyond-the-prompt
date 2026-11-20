# Σύνδεση με άλλους agents

Το Novamira δουλεύει με κάθε agent που υποστηρίζει MCP. Τις ακριβείς οδηγίες για τον δικό σας τις βρίσκετε μέσα στο site, στο **wp-admin → Novamira → Configuration**. Εκεί διαλέγετε τον agent σας και αντιγράφετε έτοιμες εντολές ή ρυθμίσεις.

Με σύνδεση OAuth (login στο site από τον browser), το MCP URL είναι:

```text
https://<το-site-σας>/wp-json/mcp/novamira-oauth
```

## Claude Code

```bash
claude mcp add --transport http --scope user novamira https://<το-site-σας>/wp-json/mcp/novamira-oauth
```

Μετά, μέσα στο Claude Code, γράψτε `/mcp` και κάντε login στο site.

Αν κάνετε clone αυτό το repo και ανοίξετε το Claude Code μέσα στον φάκελο, διαβάζει μόνο του το [`AGENTS.md`](../AGENTS.md).

## Codex CLI

```bash
codex mcp add novamira --url https://<το-site-σας>/wp-json/mcp/novamira-oauth
codex mcp login novamira
```

## Cursor, VS Code, Gemini CLI και άλλοι

Προσθέστε έναν **remote MCP server** (σε κάποια εργαλεία λέγεται «custom connector») με το παραπάνω URL και κάντε login όταν ανοίξει ο browser. Για ακριβή βήματα δείτε το **Novamira → Configuration**.

## Χωρίς OAuth: Application Password

Αν ο agent σας δεν υποστηρίζει OAuth:

1. Στο wp-admin, ανοίξτε **Users → Profile → Application Passwords**, δώστε ένα όνομα (π.χ. `agent`) και πατήστε **Add**.
2. Χρησιμοποιήστε το URL `https://<το-site-σας>/wp-json/mcp/novamira` (χωρίς `-oauth`) με το όνομα χρήστη και τον κωδικό που δημιουργήθηκε. Το **Novamira → Configuration** δείχνει πού μπαίνουν για κάθε agent.

Ο κωδικός αυτός μπαίνει στις ρυθμίσεις του agent, ποτέ στη συζήτηση.

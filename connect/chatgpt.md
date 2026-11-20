# Σύνδεση με ChatGPT

Θέλει το **chatgpt.com** στον browser ή την εφαρμογή ChatGPT, και το **Developer mode**.

Η διεύθυνση του server (MCP URL) για το site σας είναι:

```text
https://<το-site-σας>/wp-json/mcp/novamira-oauth
```

Το βρίσκετε έτοιμο για αντιγραφή και στο wp-admin, στο **Novamira → Configuration → ChatGPT**.

## Βήματα

1. **Developer mode:** στο ChatGPT ανοίξτε **Settings → Security and login** και ενεργοποιήστε το **Developer mode**. Η προειδοποίηση που εμφανίζεται είναι αναμενόμενη: το plugin συνδέεται απευθείας στο δικό σας site, γι' αυτό το OpenAI δεν το έχει ελέγξει.
2. **Νέο plugin:** στο **Settings → Plugins**, πατήστε το κουμπί πάνω δεξιά για νέο plugin. Όνομα: `Novamira`.
3. **Server URL:** βάλτε το MCP URL από πάνω. Αφήστε το **Authentication** στο **OAuth**. Τσεκάρετε το «I understand and want to continue» και πατήστε **Create**.
4. **Login:** ανοίγει η σελίδα σύνδεσης του site σας. Συνδεθείτε με τα στοιχεία της κάρτας και εγκρίνετε τη σύνδεση.
5. **Δοκιμή:** ανοίξτε νέα συζήτηση, βεβαιωθείτε ότι το plugin Novamira είναι ενεργό σε αυτήν και στείλτε το πρώτο μήνυμα από το [README](../README.md#ξεκινήστε).

## Αν κάτι δεν πάει καλά

- **Δεν βλέπω Developer mode:** μπορεί να μη διατίθεται στο πλάνο του λογαριασμού σας. Δουλέψτε με τον λογαριασμό κάποιου άλλου στην ομάδα, ή με [Claude](claude.md).
- **Το login δεν ανοίγει ή βγάζει σφάλμα:** ελέγξτε ότι το URL τελειώνει σε `/novamira-oauth` και ότι ξεκινά με `https://`.
- **Ο agent λέει ότι δεν βλέπει εργαλεία:** ενεργοποιήστε το plugin Novamira στη συγκεκριμένη συζήτηση.
- Αν έχετε κολλήσει για πάνω από 5 λεπτά, σηκώστε χέρι.

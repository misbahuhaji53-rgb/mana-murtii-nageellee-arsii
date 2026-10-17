Mana Murtii Aanaa Nageellee Arsii — Website V3

V3: public website + login/access control + hearing schedule + protected Google Meet join flow + CCMS SQL Server case search.

Demo accounts (change passwords in .env):
 admin / Admin@2026
 judge / Judge@2026
 officer / Officer@2026

Permanent Meet room:
1) Copy .env.example to .env
2) Set CONFERENCE_URL to the court-approved permanent Google Meet link.
3) Set strong passwords.

Run:
 npm install
 npm start
 Open http://localhost:3000

Note: the in-memory login/session is suitable for a prototype. For production, use a persistent session store and database-backed users/roles.


GABAASA GALMEE SCAN (YAKKAA / HH)
- Feature cusub: website irratti menu "Gabaasa Scan" dabalame.
- Kompiitara 6 irratti scanner-agent/watcher.js hojjechiisi; README-AFAN-OROMOO.txt ilaali.
- Render Environment keessatti SCAN_AGENT_KEY fi SCAN_DB_SERVER/PORT/NAME/USER/PASSWORD qindeessi.
- SCAN_DB_NAME irratti database SQL Server addaa, persistent ta'e fayyadami. Database user table uumuu, SELECT fi INSERT hayyama qabaachuu qaba.
- Render irraa SQL Server host bira ga'uu qaba; SQL Server office LAN keessaa qofa yoo ta'e Render irraa hin argamu.
- ScanEvents table yeroo jalqaba API scan fayyadamutti uumama. Yoo hayyama CREATE TABLE hin jirre, DBA table kana dursee uumuu qaba.
- PDF file gara website hin ergamu; metadata/hash qofa ergamee gabaasa keessatti lakkaa'ama.
- Kompiitara irratti agent yeroo jalqabaaf yeroo hojjetu PDFwwan duraan jiran baseline godha; hin lakkaa'u. PDF haaraa booda save ta'e lakkaa'a.
- SQL Server database addaa fi SCAN_AGENT_KEY hin qindaa'in hanga feature scan hin hojjetu. Existing website features kanaan jijjiiramu hin qabu.

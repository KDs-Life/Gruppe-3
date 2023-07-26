
# Gruppe-3 HELPFILE
**TODO**: Rechtschreibung, pleaaaaaaaaaase
## git workflow (wip)
### Start as "repository owner" oder Teamlead

***online***	im browser auf github repository erstellen und die github-url **_git-url_** des erstellten repository in die zwischenablage kopieren (ssh/https)
***lokal***		lokalen arbeitsordner erstellen und in vscode öffnen
***lokal***		in vscode, im terminal im lokalen arbeitsordner einen initialen befehl ausführen 

		git init
	
		(wenn man lokal dem github-standard folgt wird die branch "main" erstellt)
***lokal***		inhalte erstellen und dem lokalen git-index hinzufügen mit 
	
		git add *option*
		
		*option* "." für alles 
		oder selektiv einzelne Dateienamen
***lokal***		die im git-index vorhandenen inhalte werden mit dem folgenden befehl  in ihrem zustand als _fertig_ bestätigt und somit in die staging-area verschoben

		git commit -m 'Initial commit'

		(dies nennt man staging)
***lokal***		das github repository als remote referenz hinzufügen mit 

		git remote add git-url
***lokal***		die lokalen inhalte, die in der staging area sind, in das remote repository schieben mit 

		git push -u -f origin main
***online***	im browser sollten nun die inhalte im github repository unter ***git-url*** erscheinen

Aufgabe **Start** abgeschlossen

## Cowork (developerA und developerB)
***lokal***		arbeitsordner erstellen und in vscode öffnen

***lokal***		in vscode, im terminal im arbeitsordner das repository klonen mit

		git clone git-url
		
		(main inhalte aus dem repository sind nun lokal vorhanden)
***lokal***		um an seiner aufgabe zu arbeiten erstellt man eine **branch** mit einem aussagekräftigen branchnamen

		git checkout -b *branch*
		
		(die *branch* sollte erkennen lassen was sie beinhaltet bzw an was gearbeitet wird)
***lokal***		nach durchgeführten änderungen stellt man diese in die staging-area mit 	
		
		git add *option*
		
		*option* "." für alles 
		oder selektiv einzelne Dateienamen
***lokal***		mit dem folgenden befehl kann man überprüfen ob die geänderten dateien im git-index aufgenommen wurden

		git status
***lokal***		die im git-index vorhandenen inhalte werden mit dem folgenden befehl als _fertig_ bestätigt und somit in die staging-area verschoben

		git commit -m 'was wurde gemacht'
***lokal***		um mögliche änderungen, während man gearbeitet hat, aus der branch **main** auf seinem lokalen rechner aktuell zu halten sollte man vor einem push in das repository folgenden befehl ausführen

	git pull origin main 

	(anmerkung: dies kann zu konflikten führen die man dann lokal lösen muss, alleine oder im team,
	"main" sollte als quelle vorrang haben)
***lokal***		um die lokalen inhalte aus der staging-area in das remote repository zu übertragen wird folgender befehl benutzt

	git push origin *branchname*
***online***	im browser auf github sollten nun unter ***git-url*** die inhalte in der branch *branchname* auftauchen

***online***	um die änderungen von *branchname* in die branch *main* zu überführen ist ein merge request (pull request) von *branchname* zu "main" nötig anmerkung: dieser kann zu konflikten führen

***online***	falls es konflikte gibt müssen diese in einem review (alleine/team) gelöst werden

***online***	falls keine konflikte entstehen kann der merge direkt zu "main" durchgeführt werden und die anliefernde branch gelöscht werden. anmerkung: die lokale branch *branchname* ist beim developer noch vorhanden!

## Change (developerA und developerB)
***lokal***		arbeitsordner existiert lokal noch! diesen in vscode öffnen

***lokal***		die lokalen dateien auf den neusten stand aus dem remote repository bringen mit 

		git pull origin main
***lokal***		die gewollten änderungen durchführen und überprüfen welche dateien betroffen sind

		git status
***lokal***		die betroffenen dateien dem git-index hinzufügen mit

		git add *option*
				
		*option* "." für alles 
		oder selektiv einzelne Dateienamen
***lokal***		überprüfen ob die geänderten dateien im git-index aufgenommen wurden

		git status
***lokal***		die im git-index vorhandenen inhalte werden mit dem folgenden befehl als _fertig_ bestätigt und somit in die staging-area verschoben

		git commit -m 'was wurde gemacht'
***lokal***		um mögliche änderungen, während man gearbeitet hat, aus der branch **main** auf seinem lokalen rechner aktuell zu halten sollte man vor einem push in das repository folgenden befehl ausführen

	git pull origin main 

	(anmerkung: dies kann zu konflikten führen die man dann lokal lösen muss,
	"main" sollte als quelle vorrang haben)
***lokal***		um die lokalen inhalte aus der staging-area in das remote repository zu übertragen wird folgender befehl benutzt

	git push origin *branchname*
***online***	im browser auf github sollten nun die inhalte in der branch **branch** auftauchen

***online***	um die änderungen von  **branch** in die branch **main** zu überführen ist ein *merge request* (pull request) von **branch** zu **main** nötig anmerkung: dieser merge request kann zu konflikten führen

***online***	falls es konflikte gibt müssen diese in einem review (alleine/team) gelöst werden

***online***	falls keine konflikte entstehen kann der merge direkt zu "main" durchgeführt werden und die anliefernde branch gelöscht werden. anmerkung: die lokale **branch** ist beim developer noch vorhanden! beim nächsten push in die **branch** wird diese aber wieder im repository erstellt und sichtbar.

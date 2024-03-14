README

csv_heatthechair:
	
	timestamp: timestamp de l'esdeveniment registrat (comença des de 0).
	game: Indica quan comença el joc (1).
	piece: Mostra si una peça està implicada (1) o no (0) en l'esdeveniment.
	objective: Indica quan es completa un objectiu (fer tot el número).
	interruption_in: Indica les interrupcions que van apareixent.
	interruption_out: Indica quan les interrupcion acaben.
	interruption_type: Descriu el tipus d'interrupció: "none", "switches" o "question".
	interruption_begin_time: timestamp de l'inici de la interrupció.
	interruption_due_time: timestamp fins el que es pot realitzar la tasca de la interrupció.

csv_interruption:

	Fet amb Preprocessing_data.
	Es modifica el csv_heatthechair per a que el timestamp estigui en datetime i no en unix.
	També que les interrupcions en que el seu begin_time és now (en el csv és 0) ens aparegui com a begin time el moment en que arriba la notificació.

gazedata_csv:

	timestamp
	gaze2d_x, gaze2d_y: Posició cap on miren els ulls, son valors de [0,1]^2
	eyeleft_pupildiameter, eyeright_pupildiameter: diàmetre de les pupiles

gazedata_csv_definitiu:

	És el csv del gazedata al qual se li han afegit el workload en funció del nombre d'interrupcions que es donen.
	Es fa a Preprocessing_data i es tenen en compte les dades de csv_interruption.

raw:

	Els fitxers que ens dona l'eyetracker
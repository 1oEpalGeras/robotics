# Κλωσσομηχανή - Egg Incubator

Το σχολείο μας συμμετέχει στον 1ο Πανελλήνιο Διαγωνισμό Εκπαιδευτικής Ρομποτικής & Physical Computing Ανοικτών Τεχνολογιών 
με την κατασκευή μιας Μηχανής Εκκόλαψης Αυγών (Κλωσσομηχανής) από την μαθητική ομάδα "Ενεργοκλαδυετές". 

![alt text](https://github.com/1oEpalGeras/EggIncubator/blob/master/pictures/DSC01155.JPG)


ΠΕΡΙΓΡΑΦΗ ΛΕΙΤΟΥΡΓΙΑΣ
-----------------------------------------------------------------------------------

Ο αυτοματισμός της κατασκευής ρυθμίζει τις περιβαλλοντικές συνθήκες του θαλάμου που είναι απαραίτητες για την εκκόλαψη των αυγών. 

Συγκεκριμένα, η μηχανή επιτελεί τις παρακάτω λειτουργίες: 

- Ρυθμίζει την θερμοκρασία του θαλάμου, ώστε αυτή να παραμένει σταθερή γύρω από τους 37°C. 
- Μετράει την υγρασία του χώρου.
- Περιστρέφει τα αυγά  ανά τακτά χρονικά διαστήματα (π.χ. κάθε 4 ώρες).
- Η θέρμανση του χώρου πραγματοποιείται με την χρήση τεσσάρων λαμπτήρων πυράκτωσης. 
- Για την μέτρηση της θερμοκρασίας και της υγρασίας χρησιμοποιείται o αισθητήρας DHT22. 
- Όταν η θερμοκρασία στον θάλαμο εκκόλαψης πέσει κάτω από την επιθυμητή τιμή, ο μικροελεγκτής το αντιλαμβάνεται μέσω του αισθητήρα και δίνει εντολή για την έναυση του κυκλώματος των λαμπτήρων, έως ότου η θερμοκρασία φτάσει και πάλι στα επιθυμητά επίπεδα. 
- Για την καλύτερη διάχυση της θερμοκρασίας στον θάλαμο εκκόλαψης λειτουργεί ένας ανεμιστήρας. 
- Η περιστροφή των αυγών πραγματοποιείται με την βοήθεια σερβοκινητήρα όπου ένας αρθρωτός βραχίονας μεταδίδει την κίνηση σε συρτάρι με 35 θήκες αυγών.
- Κατά τις πρώτες και τις τελευταίες δύο ημέρες εκκόλαψης ο μηχανισμός περιστροφής των αυγών έχει προγραμματιστεί να μην λειτουργεί, αφού σε αυτή την περίοδο τα αυγά δεν πρέπει να περιστρέφονται.
- Η χρονική λειτουργία του μηχανισμού βασίζεται σε άρθρωμα Ρολογιού Πραγματικού Χρόνου (RTC) PCF8523.
- Η ενημέρωση του χρήστη πραγματοποιείται μέσω μιας σειριακής οθόνης LCD 4x20 που προβάλλει τις τιμές της θερμοκρασίας, της υγρασίας του θαλάμου, της ημερομηνίας έναρξης και λήξης της εκκόλαψης των αυγών καθώς και των ημερών που απομένουν για την ολοκλήρωση της.
- Στον θάλαμο εκκόλαψης λειτουργεί και ένας αισθητήρας Ανίχνευσης Κίνησης (PIR) HC-SR501. 
- Το άνοιγμα και το κλείσιμο της πόρτας ελέγχεται από μια μαγνητική επαφή. Όταν η πόρτα ανοίγει, η λειτουργία θέρμανσης του θαλάμου διακόπτεται. Για την επόπτευση του χώρου ανάβει μια λάμπα χαμηλής ισχύος LED. 
- Όσο η πόρτα παραμένει ανοικτή, η οθόνη ενημερώνει τον χρήστη σχετικά την τρέχουσα ημερομηνία και ώρα αλλά και τις εναπομείνασες ημέρες   για την ολοκλήρωση της εκκόλαψης.
- Η λειτουργία της εκκόλαψης των αυγών ξεκινάει πάλι όταν η πόρτα κλείσει.
- Η διαδικασία εκκόλαψης ολοκληρώνεται μετά την πάροδο 21 ημερών.

Ο αυτοματισμός της μηχανής υλοποιήθηκε με την χρήση της πλατφόρμας Arduino (UNO). 

Το έργο χρηματοδοτήθηκε στο πλαίσιο υλοποίησης της Πράξης «Υποστήριξη και Διαχείριση των Σχεδίων Δράσης του έργου "Μια Νέα Αρχή στα ΕΠΑΛ"» μέσω του Επιχειρησιακού Προγράμματος «ΑΝΑΠΤΥΞΗ ΑΝΘΡΩΠΙΝΟΥ ΔΥΝΑΜΙΚΟΥ, ΕΚΠΑΙΔΕΥΣΗ ΚΑΙ ΔΙΑ ΒΙΟΥ ΜΑΘΗΣΗ» με τη συγχρηματοδότηση της Ελλάδας και της Ευρωπαϊκής Ένωσης.


ΣΧΗΜΑΤΙΚΟ ΔΙΑΓΡΑΜΜΑ
--------------------------------------------------------------------------------------
![alt text](https://github.com/1oEpalGeras/EggIncubator/blob/master/Schematic%20Diagram.png)


ΥΛΙΚΑ ΚΑΙ ΚΟΣΤΟΣ ΚΑΤΑΣΚΕΥΗΣ
--------------------------------------------------------------------------------------

|α/α| Υλικά                                                |Ποσότητα| 
|---|------------------------------------------------------|--------|
|1  | Μονάδα Arduino UNO R3                                |   1    |
|2  | Οθόνη 4X20 LCD, I2C      				                        |   1    |
|3  | Μονάδα ρελέ, 4 καναλιών   				                       |   1    |
|4  | Αισθητήρας θερμοκρασίας και υγρασίας DHT22   	       |   1    |
|5  | Άρθρωμα Ρολογιού Πραγματικού Χρόνου (RTC) PCF8523  	 |   1    |
|6  | Αισθητήρας κίνησης PIR HC-SR501 			                  |   1    |
|7  | Μαγνητική επαφή  					                               |   1    |
|8  | Σερβοκινητήρας 15Kg.cm FS5115M 			                   |   1    |
|9  | Βάση στήριξης σερβοκινητήρα 			                      |   1    |
|10 | Βραχίονας σερβοκινητήρα Servo Arm - Single 4.2cm  	  |   1    |
|11 | Ράβδος αλουμινίου 4.62’’ 				                        |   1    |
|12 | Βάση πάκτωσης βραχίονα mini channel 0.375’’		        |   1    |
|13 | Βαρίστορ 230Vac, 14D431 				                         |   2    |
|14 | Διακόπτης ON-OFF230Vac 				                          |   1    |
|15 | Τροφοδοτικό 12Vdc, 5A 				                           |   1    |
|16 | Μετατροπέας 12Vdc/5Vdc 				                          |   1    |
|17 | Ανεμιστήρας 120X120,230V, 3W 			                     |   1    | 
|18 | Λαμπτήρες καθρέπτου 230Vac, 40W 			                  |   4    | 
|19 | Λαμπτήρας LED 230Vac, 7W 				                        |   1    |
|20 | Ενδεικτική λυχνία LED 12Vdc 			                      |   1    |
|21 | Ντουί πορσελάνης Ε27, με βάση 			                    |   5    |
|22 | Πλακέτα δοκιμών -Breadboard 			                      |   1    |
|23 | Κουτί πλαστικό στέγασης ηλεκτρονικών 245Χ190Χ90 	    |   1    |
|24 | Καλώδιο 3x0.5cm2 και φις 230V 			                    |   2m   |
|25 | Καλώδιο UTP 					                                    |   5m   |
|26 | Κόντρα πλακέ θαλάσσης 1.5cm, για την κατασκευή:	     |   1    |
|   |- Κουτιού (ΠxYxΒ = 51.5cm X 55cm X 57.5cm)            |        |
|   |- Συρταριού(ΠxYxΒ = 46cm X 8.6cm X 43cm)              |        |
|   |- Βάσης κύλησης αυγών (ΠxYxΒ = 48cm X 1.5cm X 50.5cm) |        |
|27 | Σετ οδηγού συρταριού 45cm 				                       |   1    | 
|28 | Μεντεσέδες 						                                    |   2    |
|29 | Τζάμι 24cm X 16cm 					                              |   1    |
|30 | Βίδες, παξιμάδια και ροδέλες διαφόρων μεγεθών	       |   1    |
|31 | Διάφορα μικροϋλικά					                              |   1    |
|   |    Συνολικό κόστος:                                  |222,78€ |

ΣΥΜΜΕΤΕΧΟΝΤΕΣ 
------------------------------------------------------------------------------------------
1. Σπανός Χρήστος, Α Τάξη
2. Βουλγέλλη Νικολέτα, Α Τάξη
3. Βαξεβάνης Σταύρος, Α Τάξη
4. Πλιάκας Γεώργιος, Α Τάξη
5. Μουρατίδης Νικόλαος, Α Τάξη
6. Μπακολλάρι Ευστράτιος, Β τάξη τομέα Ηλεκτρολογίας και Ηλεκτρονικής
7. Γιασσάς Στυλιανός, Γ Τάξη ειδικότητας Τεχνικού Ηλεκτρολογικών Συστημάτων Εγκαταστάσεων και Δικτύων
8. Ψωμάς Παναγιώτης, Γ Τάξη ειδικότητας Τεχνικού Η/Υ και Δικτύων Η/Υ

****Υπεύθυνοι Καθηγητές:****
1. Φωτιάδης Κωνςταντίνος, Ηλεκτρολόγος (ΠΕ83)
2. Ανδρόνικος Δημήτριος, Ηλεκτρονικός (ΠΕ84)

ΦΩΤΟΓΡΑΦΙΕΣ 
-----------------------------------------------------------------------------------
![alt text](https://github.com/1oEpalGeras/EggIncubator/blob/master/pictures/DSC01131.JPG)
![alt text](https://github.com/1oEpalGeras/EggIncubator/blob/master/pictures/DSC01172.JPG)
![alt text](https://github.com/1oEpalGeras/EggIncubator/blob/master/pictures/DSC01177.JPG)
![alt text](https://github.com/1oEpalGeras/EggIncubator/blob/master/pictures/DSC01179.JPG)
![alt text](https://github.com/1oEpalGeras/EggIncubator/blob/master/pictures/DSC01175.JPG)
![alt text](https://github.com/1oEpalGeras/EggIncubator/blob/master/pictures/DSC01194.JPG)
![alt text](https://github.com/1oEpalGeras/EggIncubator/blob/master/pictures/DSC01359.JPG)
![alt text](https://github.com/1oEpalGeras/EggIncubator/blob/master/pictures/DSC01365.JPG)
![alt text](https://github.com/1oEpalGeras/EggIncubator/blob/master/pictures/DSC01144.JPG)
![alt text](https://github.com/1oEpalGeras/EggIncubator/blob/master/pictures/DSC01196.JPG)

# University-Examination-Timetabling-Problem
Όνομα:Χριστίνα Επώνυμο:Βανάκα ΑΜ:103 

Μεταπτυχιακό Πληροφορικής και Δικτύων (MSc)

Τμήμα Πληροφορικής και Τηλεπικοινωνιών, Πανεπιστημίου Ιωαννίνων

Εργασία στο μάθημα Αλγόριθμοι και Πολυπλοκότητα

# Χρονοπρογραμματισμός εξετάσεων Πανεπιστημίου

Τεχνική Αναφορά

### Περίληψη 

Τα προβλήματα χρονοπρογραμματισμού εξετάσεων ανήκουν στην κατηγορία προβλημάτων NP-hard πράγμα που σημαίνει ότι οι ακριβείς μέθοδοι δεν είναι σε θέση να λύσουν προβλήματα με μεγέθη πρακτικής σημασίας.Ο χρονοπρογραμματισμός εξετάσεων Πανεπιστημίου εξετάζεται εδώ και χρόνια από πολλούς ερευνητές ως προς τις τεχνικές που θα επιφέρουν τα πιο βέλτιστα αποτελέσματα.  Δεδομένης της πολυπλότητας, τα προβλήματα προγραμματισμού που εμφανίζονται στην καθημερινότητα σε πραγματικές καταστάσεις όπως και ο χρονοπρογραμματισμός εξετάσεων Πανεπιστημίου , μπορεί συχνά να μοντελοποιηθούν ως προβλήματα χρωματισμού γραφημάτων. 

### 1.ΕΙΣΑΓΩΓΗ (ΠΡΟΒΛΗΜΑΤΑ NP-COMPLETE)

Στην Επιστήμη των Υπολογιστών η Θεωρία της Πολυπλοκότητας (Computational Complexity) έχει σαν κύριο στόχο την ταξινόμηση των προβλημάτων ανάλογα με τον βαθμό «πολυπλοκότητας» τους.Τα προβλήματα μπορούν να ταξινομηθούν  σε τέσσερις κλάσεις πολυπλοκότητας P,NP,NP-Complete,NP-Hard.Τα NP-Complete(Non-deterministic Polynomial) είναι υπολογιστικά προβλημάτά για τα οποία δεν έχει βρεθεί αποδοτικός αλγόριθμος πολυωνυμικού χρόνου για την  επίλυση του η οποία γίνεται προσεγγιστικά.

## 2.ΠΕΡΙΓΡΑΦΗ ΤΟΥ ΠΡΟΒΛΗΜΑΤΟΣ ΧΡΩΜΑΤΙΣΜΟΥ ΓΡΑΦΗΜΑΤΩΝ

Ο χρωματισμός γραφήματος (Graph Coloring) είναι η διαδικασία ανάθεσης χρωμάτων σε κάθε κορυφή ενός γραφήματος G έτσι ώστε καμία γειτονική κορυφή να μην έχει το ίδιο χρώμα. Ο στόχος είναι να ελαχιστοποιηθεί ο αριθμός των χρωμάτων ενώ χρωματίζετε ένα γράφημα.Έστω V ο αριθμός κορυφών, οι οποίες σχηματίζουν ένα συνδεδεμένο γράφημα, ο στόχος είναι να χρωματιστεί κάθε κορυφή έτσι ώστε εάν δύο κορυφές συνδέονται στο γράφημα (γειτονικές κορυφές) θα χρωματιστούν με διαφορετικά χρώματα.  

## 3.ΠΡΟΣΕΓΓΙΣΕΙΣ ΕΠΙΛΥΣΗΣ

Στην διεθνη βιβλιογραφία έχουν προταθεί τεχνικές επίλυσης όπως Graph based sequential Techniques,Constraint based techniques,Local search techniques και Population Based techniques.

## 3.1 ΔΕΔΟΜΕΝΑ ΠΡΟΒΛΗΜΑΤΟΣ(Toronto datasets)

Τα δεδομένα του προβλήματος είναι τα Toronto datasets τα οποία αποτελούνται απο 13 περπτώσεις προβλημάτων. Ο στόχος του προβλήματος είναι να αντιστοιχιστεί ένα σύνολο εξετάσεων μαθήματων στα οποία είναι εγγεγραμένοι οι φοιτητές, σε ένα σύνολο περιόδων με τέτοιο τρόπο έτσι ώστε να ικανοποιείται ένα σύνολο περιορισμών. Οι περιορισμοί που αντιμετωπίζουμε είναι δύο, ο "σκληρός" περιορισμός όπου δεν πρέπει να υπάρχουν φοιτητές που συμμετέχουν σε περισσότερα απο ένα μαθήματα την ίδια περίοδο, και ο "μαλακός" όπου περιλαμβάνει την εξάπλωση των εξετάσεων σε ολόκληρη την εξεταστική περίοδο αλλά ορίζοντας τις ποινές 6, 8, 4, 2 ή 1 σε κάθε περίπτωση που ένας φοιτητής συμμετέχει σε δύο εξετάσεις που απέχουν 1, 2, 3, 4 ή 5 περιόδους αντίστοιχα. 

## 3.2 ΠΙΝΑΚΑΣ ΣΤΑΤΙΣΤΙΚΩΝ ΣΤΟΙΧΕΙΩΝ ΠΡΟΒΛΗΜΑΤΩΝ

Ο πίνακας 1  μας δείχνει λεπτομερείς πληροφορίες από 13 στιγμιότυπα προβλημάτων για τα οποία καλούμαστε να επιλύσουμε όπως αριθμό των φοιτητών,αριθμό των μαθήματων που είναι εγγεγραμμένοι, τον αριθμό των εξετάσεων, τον αριθμό των διαθέσιμων περιόδων και την πυκνότητα των συγκρούσεων.Ο πίνακας συγκρούσεων είναι ένας δισδιάστατος πίνακας c στον οποίο κάθε στοιχείο cij = 1 αν η εξέταση i βρίσκεται σε σύγκρουση με την εξέταση j ενώ ισχύει ότι cij = 0 σε άλλη περίπτωση. Η πυκνότητα συγκρούσεων υπολογίζεται διαιρώντας τον αριθμό των στοιχείων του πίνακα συγκρούσεων που έχουν την τιμή 1 με το συνολικό πλήθος των στοιχείων του πίνακα.Τα αρχεία δεδομένων (.stu) έχουν μία γραμμή για κάθε σπουδαστή, όπου περιέχει τους αριθμούς χωρισμένους με κενά των μαθημάτων όπου έχουν εγγραφεί.

Πίνακας 1. Στατιστικά στοιχεία προβλημάτων
car‐f‐92 car‐f‐92.stu 543 18419 55522//car‐s‐91 car‐s‐91.stu 682 16925 56877 //ear‐f‐83 ear‐f‐83.stu 190 1125 8109 //hec‐s‐92 hec‐s‐92.stu 81 2823 10632 //kfu‐s‐93 kfu‐s‐93.stu 461 5349 25113// lse‐f‐91 lse‐f‐91.stu 381 2726 10918// pur‐s‐93 pur‐s‐93.stu 2419 30029 120681//rye‐s‐93 rye‐s‐93.stu 486 11483 45051// sta‐f‐83 sta‐f‐83.stu 139 611 5751// tre‐s‐92 tre‐s‐92.stu 261 4360 14901 //uta‐s‐92 uta‐s‐92.stu 622 21266 58979// ute‐s‐92 ute‐s‐92.stu 184 2749 11793 //yor‐f‐83 yor‐f‐83.stu 181 941 6034

## 4.ΕΠΙΛΥΣΗ ΠΡΟΒΛΗΜΑΤΟΣ 

## 4.1 FIRST FIT 

Ο First Fit, γνωστός και ως Greedy Coloring είναι η ευκολότερη και ταχύτερη τεχνική όλων των Greedy Coloring ευρετικών αλγορίθμων χρωματίζοντας οποιαδήποτε κορυφή με το πρώτο διαθέσιμο χρώμα ξεκινώντας από οποιαδήποτε αυθαίρετη κορυφή.

## 4.2 DSATUR(Degree of Saturation Algorithm)

Η ιδέα πίσω από τον DSATUR είναι να χρωματιστεί μια κορυφή με τον μεγαλύτερο αριθμό χρωμάτων που χρησιμοποιούνται από τις γειτονικές κορυφές, με σκοπό να γίνει ο συνολικός αριθμός χρωμάτων που χρησιμοποιούνται όσο το δυνατόν μικρότερος.

## 4.3 RLF(Recursive Largest First)

Ο αλγόριθμος RLF χρωματίζει τις κορυφές σε φθίνουσα σειρά σύμφωνα με τον βαθμό κορυφής, ο οποίος ορίζεται ως αριθμός των κορυφών που συνδέεται μια κορυφή. 

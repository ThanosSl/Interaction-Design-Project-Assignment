# Lesson: Interaction Design

### First and Last Name: Thanasis Slavidis, Iordanis Elizoglou, Theofilos Savvidis
### University Registration Number: dpsd19120, dpsd19034, dpsd19115
### GitHub Personal Profile: https://github.com/ThanosSl , https://github.com/Jelizog , https://github.com/Tsavvis

# Introduction

# Summary


# 1st Deliverable
- **Design Brief** (Short description of the project: main goals) (1/2 page max)
    
    Short: Ένα φανάρι με σχήμα κυλίνδρου στο ύψος ενός μέτρου, που θα ανιχνεύει την ταχύτητα των μηχανοκίνητων οχημάτων και θα προειδοποιεί τον χρήστη με ένα πορτοκάλι φως για το αν μπορεί να περάσει την διάβαση ή όχι.
    
- **Research** (Based on PACT) (2 pages max):
    - Analyse People (users and other stakeholders, define target group - Which are your users)
        
        Pedestrians.
        
    - Define Activities (What users do before your project!)
        
        Checking with their own eyes for upcoming Vehicles and Bikes (left and right).
        
    - Describe Context (What are the contextual information we have before the intervention)
        
        Οι πληροφορίες που υπάρχουν ως τώρα είναι οι σημάνσεις, τα πεζοδρόμια και οι διαβάσεις.
        
    - Review needed Technologies (locate and analyze similar projects, collect technologies that you plan to use: platform/Arduino, etc, sensors, actuators, software, etc)
        
        Police Camera for detecting the speed of a car, pharmacy centers/ supermarkets sensors detecting movement (Αισθητήρες κίνησης/ Movement sensors)

# 2nd Deliverable
- **Information architecture** (outline the major information components/content and their organisation) (2 pages max)
  
     Η διαδικασία που ακολουθείται είναι η εξής. Αρχικά, διασχίζει ένα μηχανοκίνητο όχημα τον δρόμο, το οποίο το εντοπίζει ο πρώτος αισθητήρας, όταν το όχημα μετακινηθεί 1 μέτρο θα το εντοπίσει ο δεύτερος αισθητήρας. Αυτές τις πληροφορίες, οι σένσορες θα τις στέλνουν στο arduino όπου και θα γίνεται ο υπολογισμός της ταχύτητας του οχήματος. (Αν πάνω από 65km/h ανοίγει το φωτάκι, αν κάτω από 65km/h δεν ανοίγει το φωτάκι). Θα ανοίγει ή θα παραμένει κλειστό, ανάλογα την περίπτωση. Με το που θα παίρνει σήμα ο 2ος σένσορας και στείλει την πληροφορία στο Arduino, και οι δύο σένσορες κάνουν reset.
  
     - Car passes by
     - 1st sensor activation
     - Start timer
     - 2nd sensor activation (after 1m)
     - End timer
     - Calculate speed
     - LED activation (based on speed)
     - RESET
 
- **User Interaction** (Plan and analyse new interaction behaviour based on the activities described on step 2.2) (1 page max)
     
     - 1η περίπτωση: Βλέπει το κόκκινο LED με το χεράκι πάνω του, υπάρχει και ένα STOP όπου τον ενημερώνει για το τι πρέπει να κάνει. Σταματάει και περιμένει να κλείσει το φωτάκι. Το φωτάκι θα έχει κλείσει αφού υπολογιστεί σε πόσο χρόνο στα 50m περίπου θα περάσει το όχημα.

     - 2η περίπτωση: Είναι κλειστό το LED οπότε δεν χρειάζεται να κάθεται να περιμένει. Απλά περνάει τον δρόμο.

- **Interface design** (Outline interface components - Define each component's role, behaviour, relation to other) (1 page max)
  
   - Επιγραμματικά τα interface components:

     - LED 
       - να υπάρχει πηγή φωτός
       - να φωτίζει το φακό
    
     - LED CAP  (ΦΑΚΟΣ, σε σχήμα χεριού)
       - για να ενημερώνει τον χρήστη για να σταματήσει
    
     - Ετικέτα STOP
       - για να ενημερώνει τον χρήστη, υποδεικνύει τι πρέπει να κάνει ο χρήστης όταν ανάβει το κόκκινο φωτάκι
    
     - Οδηγίες χρήσης
       - για να ενημερώνει τον χρήστη, σχετικά με την λειτουργία του αντικειμένου
       - ετικέτα κολλημένα στην περιοχή του STAND
    
     - STAND (που θα έχει όλα αυτά μέσα)
       - Υποστήριξη του όλου συστήματος
 
 



# 3rd Deliverable 
- **Scenarios & Storyboarding** (Prepare short scenarios focused on specific activities, create storyboards that present activities in action)(1-page max)
 
  - **1η περίπτωση:** (αναγνωρίζει κίνηση):
   
    - 1η φάση: Ο σένσορας αναγνωρίζει κίνηση μηχανοκίνητου αν πηγαίνει άνω των 65 χλμ/ω.
  
    - 2η φάση: Αφού το αναγνωρίζει ο σένσορας το στέλνει στο arduino UNO.
  
    - 3η φάση: Το πρόγραμμα κάνει την φωτεινή ένδειξη πορτοκαλί.
   
    - 4η φάση: Ο πεζός πριν περάσει την διασταύρωση παρατηρεί το πορτοκαλί φως και σταματάει.
  
  
  - **2η περίπτωση:** (δεν αναγνωρίζει κίνηση | default):
    
    - 1η φάση: Ο σένσορας αναγνωρίζει κίνηση μηχανοκίνητου αν πηγαίνει κάτω από 65 χλμ/ω.
    
    - 2η φάση: Στέλνει μύνημα στο Arduino UNO.
    
    - 3η φάση: Το πρόγραμμα κρατάει κλειστό το φωτάκι, και δεν κάνει τίποτα. 
 
    ![This is an image](https://github.com/ThanosSl/Interaction-Design-Project-Assignment/blob/main/arduino_storyborad1.png)

- **Prototyping** (Create a prototype based on a single scenario)(2 pages max)
  
     - Το αυτοκινητάκι περνάει πάνω από τον 1ο αισθητήρα: <br!>
       Ενεργοποιεί την συνάρτηση autoTune, η οποία ξεκινάει το ρολόι. Κατ’ ουσία  η συνάρτηση millis() κρατάει τον χρόνο, όπου εξαρτάται από την Serial.begin, και έπειτα     εισάγεται στην μεταβλητή t1. <br!>
Έπειτα, καλείται μία δεύτερη συνάρτηση autotune η οποία είναι υπέυθυνη για τον δεύτερο αισθητήρα. Όταν η συνάρτηση λάβει ερέθισμα από τον αισθητήρα, υπολογίζεται ο     δεύτερος χρόνος που χρειαζόμαστε και εισάγεται στην μεταβλητή t2. Με τον υπολογιμσό των t1 και t2 μπορούμε να βρούμε σε πόσο χρόνο το αυτοκίνητο κάλυψε την         απόσταση των 20 μετρων μεταξύ των αισθητήρων. <br!>
Έτσι, λοιπόν, μπορούμε να βρούμε τη ταχύτητα του αυτοκινήτου (αν η αφαίρεση των δυο τιμών μας δίνει αποτέλεσμα ίσο ή μικρότερο από 1108 χιλιοστά του δευτερολέπτου   τότε το αυτοκίνητα κινείται με ταχύτητα ίση ή μεγαλύτερη από 65 km/h ). Στην περίπτωση που έχουμε υπέρβαση του προειδοποιητικού ορίου των 65 km/h , το φωτάκι θα ανάψει.<br!>
Να σημειωθεί ότι για λόγους ευκολίας, το φωτάκι (της μακέτας) καταλήξαμε να το κάνουμε κόκκινο.

   
 
# Conclusions
- **Link** του tinkercad κώδικα, για βελτιώσεις: https://www.tinkercad.com/things/j6AVxtwYh6y-spectacular-inari-densor/editel?sharecode=qjmvsew3OiN30whn1lfmh9ywlG3E3-7lLyW4onKm0X4

# Sources

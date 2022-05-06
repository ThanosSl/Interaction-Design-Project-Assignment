# Lesson: Interaction Design

### First and Last Name: Thanasis Slavidis, Iordanis Elizoglou, Theofilos Savvidis
### University Registration Number: dpsd19120, dpsd19034, dpsd19115
### GitHub Personal Profile: https://github.com/ThanosSl , https://github.com/Jelizog , https://github.com/Tsavvis

# Introduction

# Summary


# 1st Deliverable
- Design Brief (Short description of the project: main goals) (1/2 page max)
    
    Short: Υποστήριξη πεζών κατά την διάρκεια διάσχισης του δρόμου. Πιο συγκεκριμένα ο πεζός θα ειδοποιείται με πορτοκαλί ένδειξη για το αν πλησιάζει αυτοκίνητο με μεγάλη ταχύτητα. Το σύστημα θα βασίζεται σε αυτή την ταχύτητα, ώστε να ενημερώνει ανάλογα τον πεζό. 
    
- Research (Based on PACT) (2 pages max):
    - Analyse People (users and other stakeholders, define target group - Which are your users)
        
        Pedestrians.
        
    - Define Activities (What users do before your project!)
        
        Checking with their own eyes for upcoming Vehicles and Bikes (left and right).
        
    - Describe Context (What are the contextual information we have before the intervention)
        
        Οι πληροφορίες που υπάρχουν ως τώρα είναι οι σημάνσεις, τα πεζοδρόμια και οι διαβάσεις.
        
    - Review needed Technologies (locate and analyze similar projects, collect technologies that you plan to use: platform/Arduino, etc, sensors, actuators, software, etc)
        
        Police Camera for detecting the speed of a car, pharmacy centers/ supermarkets sensors detecting movement (Αισθητήρες κίνησης/ Movement sensors)

# 2nd Deliverable
- Information architecture (outline the major information components/content and their organisation) (2 pages max)
  
     Η διαδικασία που ακολουθείται είναι η εξής. Αρχικά, διασχίζει ένα μηχανοκίνητο όχημα τον δρόμο, το οποίο το εντοπίζει ο πρώτος αισθητήρας, όταν το όχημα μετακινηθεί 1 μέτρο θα το εντοπίσει ο δεύτερος αισθητήρας. Αυτές τις πληροφορίες, οι σένσορες θα τις στέλνουν στο arduino όπου και θα γίνεται ο υπολογισμός της ταχύτητας του οχήματος. (Αν πάνω από 65km/h ανοίγει το φωτάκι, αν κάτω από 65km/h δεν ανοίγει το φωτάκι). Θα ανοίγει ή θα παραμένει κλειστό, ανάλογα την περίπτωση. Με το που θα παίρνει σήμα ο 2ος σένσορας και στείλει την πληροφορία στο Arduino, και οι δύο σένσορες κάνουν reset.
  
     - Car passes by
     - 1st sensor activation
     - Start timer
     - 2nd sensor activation (after 1m)
     - End timer
     - Calculate speed
     - LED activation (based on speed)
     - RESET
 
- User Interaction (Plan and analyse new interaction behaviour based on the activities described on step 2.2) (1 page max)
     
     - 1η περίπτωση: Βλέπει το κόκκινο LED με το χεράκι πάνω του, υπάρχει και ένα STOP όπου τον ενημερώνει για το τι πρέπει να κάνει. Σταματάει και περιμένει να κλείσει το φωτάκι. Το φωτάκι θα έχει κλείσει αφού υπολογιστεί σε πόσο χρόνο στα 50m περίπου θα περάσει το όχημα.

     - 2η περίπτωση: Είναι κλειστό το LED οπότε δεν χρειάζεται να κάθεται να περιμένει. Απλά περνάει τον δρόμο.

- Interface design (Outline interface components - Define each component's role, behaviour, relation to other) (1 page max)
  
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


# Conclusions


# Sources

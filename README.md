# Datalogiskt-tankande-inlamning
Inlämningsuppgift med pseudokod och flödesschema i kursen Introduktion till programmering och datalogiskt tänkande

## Split the nota
```
START
     SET pris (INPUT "Ange pris")
     SET dricks (INPUT "Ange dricks i decimaler")
     SET antal-personer (INPUT "Ange antal personer")
     SET drickssumma (CALCULATE pris x dricks)
     SET totalsumma (CALCULATE pris + drickssumma)
     SET summa-person (CALCULATE totalsumma / antal-personer)
     PRINT “summa-person”
END
```

<img width="1408" alt="Split the nota" src="https://github.com/user-attachments/assets/3717a3ae-0002-47a5-a03e-0265e7f68b0b" />


## Lewis Carroll Word Puzzle 
```
FUNCTION giltigt-ord
     IF input skiljer sig med mer än ett tecken från startord           
          PRINT “Ditt ord skiljer sig med mer än ett tecken från” + startord
          RETURN false

     ELSE IF input == startord            
          PRINT “Ditt ord måste skilja sig med ett tecken från” + startord  
          RETURN false

      ELSE 
           RETURN true           
END FUNCTION

SET gissningar (0)
SET startord (FOUR)
SET slutord (FIVE)
SET ordbok (hämta information från en ordbok)

START

     LOOP:
          PRINT “Skriv ett ord som skiljer sig med ett tecken från” + startord
          PRINT “Slutordet är” + slutord
          PRINT “Antal gissningar :” + gissningar

          SET input (Spelarens ord)
          SET gissningar (CALCULATE gissningar + 1)

                  IF CALL FUNCTION giltigt-ord == true
                       IF input - inte finns i ordbok
                            PRINT “Ditt ord finns inte med i ordboken”

                       ELSE IF input == slutord
                            BREAK LOOP

                       ELSE 
                             SET startord (input)
                             PRINT “Ditt nya ord är” + startord
      END LOOP

      PRINT “Grattis! Du vann!! Du har gissat” + gissningar + “gånger.” 

END
```
<img width="2688" alt="Lewis Carroll Word Puzzle" src="https://github.com/user-attachments/assets/5f3de3cc-4a7c-40e4-a5cb-ce6da6577fa4" />

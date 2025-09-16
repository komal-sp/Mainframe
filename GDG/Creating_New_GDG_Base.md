Before using GDG, we need to create a GDG base first. Then, we need to create the generation on it. IDCAMS urility is used to create a GDG base.
The syntax is follows-

<img width="411" height="183" alt="image" src="https://github.com/user-attachments/assets/1102aea8-2d58-4b5d-8a03-bf629d60b99e" />

Parameters-
**- NAME(gdg-base-name):** Specifes the name of the GDG base.
**- LIMIT(nnn):** Specifies the total number of generations that the GDG may contain. The maximum value for LIMIT is 255.
**- EMPTY|NONEMPTY:** These are mutually exclusive parameters.

**EMPTY** parameter specifies that all existing genrations are to be uncataloged whenever the genrerations of GDG reach the maximum limit. **FOR EX**, suppose a GDG is defined with a limit of 7 and we are creating an 8th generation with an empty option. In that case, it will delete all seven generations.

**NOEMPTY** specifies that only the oldest generation of the GDG us to be uncataloged if the limit is reached. **From the same above example**, if it is NOEMPTY option, it will delete the oldest generation (G0001V00).

**- SCRATCH|NOSCRATCH:** These are matually exclusive parameters.

**SCRATCH** specifies that the generation should be deleted physically when uncataloged

**NOSCRATCH** specifies that the genration should not be deleted when it is uncataloged. It can be accessed using the UNIT nad VOL parameters.

**Practical Example-**
**Scenario:** Create a GDG base with 5 generations limit and delete the oldest genration when it reaches the limit.
**Code-**

<img width="446" height="271" alt="image" src="https://github.com/user-attachments/assets/f47a7171-18a1-4bc8-a6e2-b6ebc4e7f917" />

<img width="455" height="277" alt="image" src="https://github.com/user-attachments/assets/2630cda1-bf4a-4b25-b11f-fe28037023b3" />

**Explaining Example-**
In this example, the IDCAMS utility creates the GDG called MATEPK.TESTTPS.GDG. The nu,ber of generations that can exist at anytime is limited to five. NOEMPTY specifies the system should uncatalog the oldest genration once the limit is reached. The SCRATCH parameter is used to determone whether to [hysically delete the uncataloged data set.





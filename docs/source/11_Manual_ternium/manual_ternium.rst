MotoSuiveur Manual (from Ternium project)
====================

Introduction
----------------
	Object of this manual is to present operation modes of MotoSuiveur® (further called MS). Manual describes electrical part of MS, MS operation modes, troubleshooting and maintenance. On figure 1 is presented MS main block diagram.
 
Figure 1 MotoSuiveur® main block diagram
 
Glossary (to be replaced for Hydraulic)
----------------

№	Name	Description
1	Recovery motor	Recovery power transmission train. To be used to safely lower (or shortly raise) the load in case of emergency.
2	Recovery transmission	
3	Recovery engaged switch (RS)	Recovery transmission train engaged
4	Unscrewing enable switch (USCRE)	Stops and prevent further hoist movement in this direction
5	Screwing enable switch (SCRE)	
6	Worm switch cam	Acts on SCRE and USCRE
7	Recovery engagement nut with switch cam	Engages the recovery transmission to the worm and acts on RS
8	MS motor	Allows normal operation following
9	Friction worm wheel	Acts as brake if the external toothed ring is stopped by the worm 
10	Worm	
Figure 2 MS unit components 
 
№	Name	Description
1	Hoist enabled lamp	MS authorizes hoist movements
2	Fault lamp	MS is in fault
3	Upward enabled lamp	MS authorizes hoist for upward movement
4	Backup/Recovery off/on selector key	Off - normal movement
ON – Backup mode
ON + Reset – Recovery mode
5	Backup/Recovery down/up key	Up/Down command for Recovery mode
6	Enable override selector key	Allow hoist movement when (1) is off
7	Reset button	MS reset
8	Healthy lamp	MS controller and MS motor healthy
9	Downward enable lamp	MS authorizes hoist for downward movement
10	Recovery mode lamp	Active Backup/Recovery mode
11	Recovery engaged lamp	Recovery is engaged
Figure 3 General view of MS control cabinet front door 
 
Figure 4 General view of the sequence of MS operation modes 
	Mechanical characteristics of MS are presented on the nameplate of the MS. The nameplate of the MS indicates the maximum rotating speed, the corresponding braking torque and other characteristics (mass, oil quantity, etc.). Example is shown on figure 5.
 
Figure 5 MS nameplate


 
Connect MS to control cabinet
----------------

	After mechanical assembly of MS to hoist is done, electrical connection must be made between MS and control cabinet. Figure 7 shows general view of typical MS unit electrical components that should be connected according specific for the project electrical circuit diagram.
 
№	Description	№	Description
1	C8 – Recovery motor connector	3	C6 – Power connector
2	TSW – Position switches terminal	4	C7 – Resolver connector

Figure 6 Electrical connections of MS unit
Connectors C6 and C7 (figure 6 points 3 and 4) should be made according following specification:
	For C7 connector screened cable with 4 twisted pairs, 0.25 mm² should be used. Ground the shield of the feedback should be connected to GND – figure 7 a);

	For C6 connector should be used screened cable, 4 core, 1.5 mm². Ground the shield of the feedback should be connected to GND – Figure 7 b).

	Figure 7 c) shows signal arrangement of connector on motor side for motor type Kollmorgen. 
	Figure 7 d) shows general MS motor view. 
 
a) C7 connector
 
b) C6 connector
Connector 	№	Name	Description
 	1	NC	Not connected
	2	TEMP-	Motor temperature sensor Lo
	3	COS-	Cosine Lo
	4	SIN-	Sine Lo
	5	REF-	Reference Lo
	6	TEMP+	Motor temperature sensor Hi
	7	COS+	Cosine Hi
	8	SIN+	Sine Hi
	9	REF+	Reference Hi
	10	NC	Not connected
	11	NC	Not connected
Connector 	№	Name	Description
 	1	V	Motor phase V
	2	PE	Motor earth
	3	W	Motor phase W
	4	U	Motor phase U
	A, B, C, D	NC	Not connected
c) Kollmorgen motor
 
d) General view of MS motor
Figure 7 Connectors C6 and C7
	ATTENTION
 	C6 and C7 must be connected according specification! Wrong connection can cause motor damage!

 
	Connector C8 (figure 6, point 1) is MS recovery motor electrical connector. Recovery motor is DC motor controlled by Siguren motor controller MSRM4514. Working voltage of motor is 48VDC therefore is very important motor to be connected correct. Correct connection is shown on figure 8.

 
Figure 8 MS recovery motor C8 terminal connection
 
	Position switches are used for allowing or prohibits hoist movement. Position switches are using in active output signal via NC contact. Signal from switches should be active in case when switches are not in contact with worm and worm is in correct position. Figure 9 a) combination of signals form position switches is shown. Position switches are shown on figure 9 b).
SCRE	USCRE	Upward enable	Downward enable
 	 	 	 
 	 	 	 
 	 	 	 
 	 	N/A; MS controller fault; Switch fault
 	- Active signal
 	- Inactive signal
a) combination of signals from position switches

 
b) position switches
Figure 9 Position mechanical switches 
 
	Terminal block TSW (Terminal SWitches) is used for connection of worm position proxy sensors/switches and control cabinet. Figure 10 shows general view of TSW and description of terminals.

 
№	Description
1	+24VDC. Supply USCRE position switch
2	Signal from USCRE position switch
3	+24VDC. Supply SCRE position switch
4	Signal from SCRE position switch
5	+24VDC. Supply Recovery position switch
6	Signal from position switch
Figure 10 Termina block TSW
 
	Terminal blocks in control cabinet are for connection between MS and control cabinet. Terminal blocks are described in Table 1.
Table 1 Control cabinet terminals
Terminal block	Description
T1	Power supply
T2	Digital inputs
T3	MS sensors/switches
T4	Digital outputs
T5	Analogue I/O
T6	MS motor power supply
T7	MS motor resolver
T8	Recovery motor power supply
T9	Heater
	Figure 11 shows general view of connection between MS and control cabinet (MSCC). For more detail about connection, please review electrical circuit diagram for the corresponding project.
 Figure 11 General view of connection between MS and MSCC
4	Indication lamps and controls
	Indication lamps and local controls are shown on figure 3. They are located on front door of control cabinet. 
	Indication lamps indicates:
	- MS status – figure 3, items 2, 8;
	- allowed movement direction of hoist – figure 3, items 1, 3, 9;
	- recovery mode status – figure 3, items 10, 11.
	Local controls are used for:
	- reset of MS – figure 3, item 7;
	- overrides MS enable signal (override ON signal) – figure 3, item 6;
	- enable and control MS Backup/ Recovery mode – figure 3 items 4, 5, 10, 11.
	Figure 12 shows schematically the control signals between hoist and MS. 
 
Figure 12 Control signals between hoist and MS
	ATTENTION
 	Local control commands can be duplicated with remotes! Please, check electrical circuit diagram!
4.1.1	Hoist enabled.
^^^^^^^^^^^^^^^^^^^^^

	Hoist enabled lamp indicate that the MS authorizes hoist movements. (figure 5). Hoist enabled signal will on only in case if ON signal from hoist is ON.
	Hoist enabled signal will be ON when MS self-test pass successfully and ON signal is available then Hoist enabled and Healthy indicator lamps are on. The signals are indicating system ready (MS ready).
4.1.2	Fault 
^^^^^^^^^^^^^^^^^^^^^

	Fault lamp (figure 3, item 2) indicates three different types of faults:
	- MS controller internal errors, described in section 7.1;
	- MS faults (further called flt_num), described in section 7.2;
	- MS warnings (further called wrn_num), described in section 7.2;
	MS controller internal errors are related to MS controller internal hardware, firmware, and MS motor. This type of errors are with highest priority. If MS controller internal fault appear further operation is prohibited.
	INFORMATION
 	Fault lamp indicator is on during MS self-test.

	ATTENTION
 	The system displays only last MS warning (wrn_num) or MS fault (flt_nim) occurred.

	Faults and warnings are displayed on MS 7 – segment controller. The display indicates all types of MS warnings/faults and MS controller internal errors. Indication is a combination of letters and numbers. MS controller internal faults are indicated with blinked combination of  , number and finish with symbol  .
	MS faults are displayed with combination of  and number. MS warnings are displayed with combination of   and number. 
	On figure 13 a) is shown example for internal MS controller fault. On figure 13 b) is shown example for MS warning.

 
a) MS controller internal error E01
 
b) MS warning number 10 (wrn_num = 10)
Figure 13 Displaying messages on MS controller 7 – segment display
	INFORMATION
 	After MS reset, all types of faults are cleared. Before MS reset, fault should be resolved.

 
Upward enable/Downward enable 
^^^^^^^^^^^^^^^^^^^^^

	Upward enable/Downward enable are indicators for authorized direction of hoist movement. If one of the two directions is forbidden to move, it is necessary to move the hoist in the opposite direction in order to reset the system mechanically.
	Movements upward and downward of hoist are correspond to screwing and unscrewing movement of MS worm. Movement directions of worm are corresponding to directions of clock. Direction screwing is clockwise, unscrewing direction is anticlockwise, viewed from cam part of the screw shaft as is shown on figure 14.
 
1 – Screwing direction
2 – Unscrewing direction
Figure 14 MS Worm rotating directions
	ATTENTION
 	After MS reset or manual centering of the worm and MS restart, no movement is performed or faults appears, please contact SIGUREN technologies on address support@siguren.com

 
Backup/Recovery Off/On; Backup/Recovery Down/Up
^^^^^^^^^^^^^^^^^^^^^

	Backup function allows the load to be lowered down, by using minimal functionalities when MS is in Following operation mode. Backup function ignore all settings related with nominal following operation mode and allows movement of the hoist with limited speed.
	Recovery function is used when the main hoisting chain is faulty (for example damaged brake of the hoist motor). Recovery system allows lowering load safety to the ground.

4.1.5	Enable Override
^^^^^^^^^^^^^^^^^^^^^

	Enable override can be used if it is necessary to override Hoist enabled. This allows small movements for MS mechanically reset.

4.1.6	Lamp states
^^^^^^^^^^^^^^^^^^^^^

	Combination of active (ON) and inactive (OFF) signal lams gives current status of MS. In Appendix Table 1 signal combinations are presented and described.
 
5	MS operating modes
-------------------

5.1	MS controller internal check
^^^^^^^^^^^^^^^^^^^^^

	At power on (or restart) MS starts operating according figure 3. According sequence of MS operation modes first operation is MS controller internal check. Internal check is intended to hardware, firmware of MS controller, MS motor and MS motor resolver. 
	In case of fault, fault is visualized on 7 – segment display as described in 5.1.2. Further operations are prohibited. List with MS controller internal faults are listed in section 7.1.

5.2	Self-test operation mode
^^^^^^^^^^^^^^^^^^^^^
	After MS controller internal check finishes, Self-test operation mode (further called self – test) starts. On figure 15 a) symbols indicated self-test steps on MS controller 7 – segment display are shown. On figure 15 b) is shown sequence of self-test steps.
Symbol	Description	Symbol	Description
 	Homing	 	Un-screwing enable switch not made
 	Waiting piston return	 	Screwing enable switch not made
 	Blocked	 	Screwing enable switch not centered
 	Checking MS firmware (Soft)	 	Un-screwing enable switch not centered
 	Electrical test	 	Damping plus*
 	Switch test	 	Damping minus*
 	Damping*	 	Play minus
 	Air*	 	Play plus
 	Play	 / 	Error / Fault
* - steps are applicable only for hydraulic MS
a) Self-test steps symbols



 
Fields with *, ** and *** are related with Table 2 in section 7.2
b) sequence of self-test steps
Figure 15 Self – test operation mode

5.2.1	Electrical test
+++++++++++++++++++++++++++++
	On figure 16 steps of Electrical test are shown. Test checks for active signals on inputs of the MS controller before self-test begin.



















	ATTENTION
 	In case of repetitive faults, please contact SIGUREN technologies on address support@siguren.com!


 
5.2.2	Switch test
+++++++++++++++++++

	Switch test check connection between MS controller and SCRE/USCRE switches (figure 2, items 4, 5), centered position and functionality of switches. On figure 8 are shown steps of Switch test. In Table 2 located in appendix are shown steps for visual check of Switch test. Visual check of Switch test is necessary only in case if repetitive faults during the test appears.
 
Figure 17 Steps of Switch test
	INFORMATION
 	In case of repeatedly wrn_num occurs, please check:
	connection between MS control cabinet and SCRE/USCRE switches;
	functionality of SCRE and USCRE switches;
	- signals on inputs of MS controller and operational relays RSESw and RUESw located in MS control cabinet;

5.2.3	Play test
+++++++++++++++++++
	Play test measures play between worm and worm wheel. On figure 18 steps of Play test are shown.
 
Figure 18 Play test steps

	ATTENTION
 	In case of repetitive faults, please contact SIGUREN Technologies on address support@siguren.com!
 
5.3	Following operation mode
	Following operation mode starts after successful passed of self – test. The function of this operation mode is intended for follow movements of the hoist and to monitor for exceeding the rated speed (nominal speed) with defined positive tolerance. The speed, which is considered high is called Overspeed. By design MS will not allow Overspeed. Typically Overspeed is equal to:
Overspeed = Nominal speed + 10%				(1)
	Figure 19 is presents main principle of Following operation mode and overspeed detection. On figure 20 steps of following operation mode is presented. On figure 21 are shown symbols displayed on 7 – segment display during following operation mode.
 
1 – Acceleration	4 – Exceeding nominal speed
2 – Following	5 – Overspeed detection
3 – Deceleration	6 – Overspeed detected. MS is breaking
Figure 19 Main principle of following operation mode and overspeed detection
 
Figure 20 Principle of Following operation mode
At rest
Symbol	Description
 	Unscrewing enable switch sctivated
 	Screwing enable switch activated
 	Both commands
activated
 	Maintenance “A”
 	Maintenance “B”
 	Maintenance “C”
 	Maintenance “D”
 	Rest (normal)
During movement
Symbol	Description	Explanation
 	Centering	The worm is positioned to the center of its backlash, to prepare for the next
movement
 	Screwing Tackling	Upward movement start
 	Unscrewing
Tackling	Downward movement start
 	Screwing
Following	Upward movement following
 	Unscrewing
Following	Downward movement following
 	Near Overspeed	Starts blinking the more and more rapidly as the speed approaches the
'overspeed' threshold setting
 	Near Underspeed	Starts blinking the more and more rapidly as the speed approaches the
'underspeed' threshold setting
 	Fault	Fault detected



Figure 21 Symbols displayed on 7 – segment display on MS controller
 
5.4	Backup/Recovery operation mode
^^^^^^^^^^^^^^^^^^^^^

	Backup/Recovery operation mode functions are intended to unusual situations during MS operating. Controls and indicators of this functions are located on control panel front door – figure 3, items 4, 5, 10, 11.
	On figure 23 is shown principle of Backup/Recovery operation mode. Backup/Recovery decision figures located in figures 15 and 20 with dotted outline, represent the places where request for these operation modes are checked. 
	Switching on Recovery/Backup mode is performed through Backup/Recovery OFF/ON key – figure 2, item 4. After switching Backup/Recovery mode on, Backup mode start operating. On 7 – segment display indication for backup mode is displayed   and Recovery mode lamp is on. Backup function ignore all settings related with following operation and allows movement of hoist with hoist limited speed.
	In Backup operating mode, control is performed trough commands for lifting and lowering of the hoist. In case of hoist control chain is damaged, control can be performed manually directly on control terminals located in MS control cabinet via wire bridge. Example is shown on figure 22. In Backup mode no ON signal is required to perform movement of MS. 
 
Figure 22 Example for manual operation in backup mode
 
Figure 23 Principle of Backup/Recovery operation
	Recovery mode is second part of Backup/Recovery operation. This mode start operates the way is shown on figure 23. After reset, MS checks for active Backup/Recovery mode request (Backup/Recovery operational key is ON). If request is active 7 – segment display shows symbol for Recovery mode   and engagement start. Engagement function is used to engage recovery mechanism to the worm via recovery nut – figure 1, item 7.
	Completion of engagement is indicated by Recovery engaged indication lamp (figure 3, point 10). If lamp is off after first engagement, reset is needed. Reset will activate engagement again.
	Controlling of Recovery is with 3 – position key Backup/Recovery Down/Up located on front door of control cabinet – figure 3 item 5. Also Recovery can be controller remotely if that is provided by electrical circuit diagram.
	After engagement is complete and Recovery engagement lamp is on, brake of main hoist motor should be released. Otherwise motor brake will prohibit movements. Brake should remain open until recovery operation done.
	For disengagement, load should be on safe place, main hoist motor brake should be closed. Command for lowering should be given to MS until both lamps for Upward enable and Downward enable becomes on.
		ATTENTION
 	Recovery function is mainly designed for safety lowering of the load. Function allows very short lifting of the load only in case if it is absolutely necessary!

		ATTENTION
 	Before activating Backup/Recovery operation mode from local controls (figure 3, item 4), please make sure that operation mode is not activated remotely. The verification consists of the following steps:
	Recovery mode lamp and Recovery engaged lamp are off;
	Backup/Recovery control key is in position “0” (OFF);
	On 7 – segment display symbols   or   are not displayed.
	
    
6	Troubleshoot and maintenance
------------------------------

	Troubleshooting of MS can be done by few ways:
	- via signal lamps located on front door – Appendix 1;
	- via MS controller 7 – segment display – section 6.1;
	- via touchscreen HMI (MSHMI) – section 6.2. 

6.1	Troubleshooting via MS controller 7 – segment display
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

6.1.1	MS controller internal errors
++++++++++++++++++++++++++++


Message	Description	Possible cases
E01	DC bus overvoltage: An overvoltage has been detected on the internal DC bus. 	This fault may be due to overvoltage on the network or due to overloaded ballast resistor.
E02	Undervoltage DC Bus: The internal DC bus has dropped below the configured minimum voltage. 	This fault is managed while the drive is enabled.
E03	I²t motor: Overload on the motor.
	Mechanical hard point, bad power wiring, motor feedback problem, poorly controlled brake.
E04	Overcurrent: A current greater than the maximum measurable current has been detected on at least one of the motor phases.	The drive must be powered 24VDC for 15 min before it can be unlocked.
E05	Short circuit: A short-circuit between phases or the earthing of a motor phase has been detected.	The drive must be powered 24VDC for 15 min before it can be unlocked.
E06	IGBT temperature: maximum temperature reached in the drive.	It is impossible to acknowledge the fault until the temperature has gone back down.
E07	Motor temperature: maximum temperature reached in the motor.	It is impossible to acknowledge the fault until the temperature has gone back down.

E08	Resolver fault: Defective resolver signals.	Check resolver connection between motor and control cabinet and resolver connector.
E09	Coil temperature: maximum temperature reached in the self. 	It is impossible to acknowledge the fault until the temperature has gone back down.
E16	Resolver saturation: Sin / Cos resolver signals received too high.	Check resolver connection between motor and control cabinet and resolver connector.
E17	24V auxiliary supply error. 	This fault is triggered if the 24V auxiliary power supply is noisy or has a voltage dip (<15V). Check the 24V supply.

 
6.1.2	MS faults and warnings
Message	Description	Possible cases
E02	Screwing command during self-test *	Check for pressed/held down button for hoist lifting command. 
E03	Unscrewing command during self-test *	Check for pressed/held down button for hoist lowering command
E04	Both commands during self-test *	Check for pressed/held down button for hoist lifting and lowering command
E05	ON signal missing during self-test *	ON signal from hoist missing (figure 12). Check electrical connection between hoist control cabinet and MS hoist cabinet. ON signal from hoist to MS is available Check hoist control
E10	Blocked worm	Worm is locked to recovery mechanism. Worm is stuck. Mechanical reset is needed. In case of Downward enable off after recovery operation, moving I opposite side from hoist is needed. Moving should continue until lamps indicators for upward and downward are on. After manual reentering, MS reset is necessary.
E11	Unscrewing enable switch not centered **	Switch USCRE is not in correct position. Visual check is and centering is needed
E12	Screwing enable switch not centered **	Switch SCRE is not in correct position. Visual check is and centering is needed
E13	Unscrewing enable switch not made **	USCRE switch is not reached from worm during Switch test. Visual check is needed.
E14	Screwing enable switch not made **	SCRE switch is not reached from worm during Switch test. Visual check is needed.
E28	Incorrect MS firmware version	Please, contact Siguren technologies
F15	Worm backlash too big detected (Play too big) ***	Worm play is greater than defined.
F17	Worm backlash too small detected (Play too small) ***	Worm play is smaller than defined.
F20	Air detected	Presence of air into the oil inside the damping chamber
F22	Damping too soft	Damping nozzles too open
F23	Damping too hard	Damping nozzles too closed
F33	Unscrewing Overspeed. Overspeed during lowering	Hoist speed exceeds maximum defined speed during lowering
F34	Screwing Overspeed. Overspeed during lifting	Hoist speed exceeds maximum defined speed during lifting

	ATTENTION
 	In case of repetitive faults, please contact SIGUREN Technologies on address support@siguren.com!

 
6.2	MSHMI
	The MSHMI is a Schneider Magelis HMI STU 655/855 color graphic touchscreen terminal programmed with the MSHMI firmware by Siguren technologies. MSHMI communicates with MS controller via MODBUS RTU protocol – figure 24.
 
Figure 24 MSHMI
	Advantages if using MSHMI to operating with MS® are:
	- Display MotoSuiveur® status information in the form of messages, event listings, graphics and numerical values;
	- Change the MotoSuiveur® configuration. Configuration is a secure access code at different levels;
	- Change operating mode of MotoSuiveur®;
	- Display maintenance information of MotoSuiveur®.

	INFORMATION
 	MSHMI is not part from standard MS equipment and can be ordered additionally.
6.3	Maintenance
	Due to inherent dangers in the maintenance and testing of electrical equipment, special attention should be paid to safety, not only to the personnel working the immediate area but also to equipment under test, maintenance and repair.
	All personnel operating in the relevant area should observe these procedures and pay due regard to safety Local Safety Rules and Regulations.
It is advisable that at least two fully trained engineers be present at all times when the equipment is being tested, maintained or serviced.
	All equipment under electrical test should have WARNING NOTICES displayed saying that equipment tests are in progress. Any ancillary equipment, for example, test equipment and instruments, should be safe and prominent notices around the equipment should advertise any danger, which may exist. Any notices displayed in pursuing these procedures should be removed as soon as they are no longer applicable, to emphasize the special significance of their presence.
	If it becomes necessary to carry out maintenance, testing or setting up to work on the equipment requiring access by opening doors, removing covers etc., then safety hazards may arise. Then risk assessments should be carried out and safe-working practices followed.
	A duty holder should be responsible for ensuring that the equipment is made accessible only to authorized personnel to carry out specific tasks after receiving permission.
The user should ensure that maintenance setting up and authorized and competent persons only carry out testing of the equipment. The following basic rules should be adhered to: 
	1. Before commencing maintenance works, the supply to the equipment must be isolated, locked off and the appropriate safety documents issued.
	2. Comply with safe working conditions.
	3. Do not work on the equipment when it is energized.
	4. Ensure that all persons working on the equipment are familiar with instructions and information provided in this manual.
	5. Providing that the equipment is functioning correctly and all personnel responsible for operating it are complying with the conditions specified, the electrical equipment may be deemed to be “properly used” and should be safe and free from health hazards.
	The reliability of the Motosuiveur® will depend if the maintenance procedure is strictly adhered to. Maintenance operations are to be done based either on the Maintenance type displayed on MS controller 7 – segment display or on a time basis wherever the smallest value applies.
Maintenance Intervals: - A= Weekly, B= Monthly, C= 3 Monthly, D= 6 Monthly E= Annually, F= 2 Years, G=5 Years, H=10 Years
Table 2 MS maintenance intervals
MotoSuiveur® Unit	A	B	C	D	E	F	G	H	Worm Rotation Count (HMI)	Controller 7-Segment Display
MS fixation to barrel and to hoist structure									75E6	 ;  ;  ;  
	Visual inspection. Check Fasteners, etc.		
MS Motor Transmission Grease:
REPSOL NLGI 00									75E6	 ;  ;  ;  
	Add or Replace if necessary 		
Oil Level
SIGUREN MS Oil SQ32									75E6	 ;  ;  ;  
	Visual inspection. Add if necessary.		
Worm Outer Piston Assy
Part No: MSL-01-P04									150E6	 ;  ;  
	Replace *		
MS Oil
SIGUREN MS Oil SQ32									450E6	 ;  
	Replace. Clean magnet plugs.		
Wheel Lip Seal NBR 70 Sh A
Reference: 100x120x7.5									900E6	 
	Replace *		
O-Rings NBR 70 Sh A
References: 200x2; 53x4									900E6	D
	Replace *		

* Replace earlier if leaks are present and maintenance history is unknown
 
Table 3 Integrated recovery mechanism maintenance intervals
Integrated Recovery system of MotoSuiveur® Unit	A	B	C	D	E	F	G	H	Worm Rotation Count (HMI)	Controller 7-Segment Display
Fixation to MS Unit									75E6	 ;  ;  ;  
	Visual inspection. Check Fasteners		
Recovery Transmission Grease:
REPSOL NLGI 00									-		-	
	Add or Replace if necessary 		
IR system engagement 									75E6	 ;  ;  ;  
	Test Engagement / Disengagement Function		

* Replace earlier if leaks are present and maintenance history is unknown
 
7	Appendix 1: Signal Lamps
 Table 1 Combination of active and inactive signal lams
Signal lamp	Status	Correction
Fault	Enabled	Healthy	Recovery mode	Recovery engaged		
0	0	0	1	0	MS Power off. Recovery pre-engaged	Check MS electrical equipment and MS power supply. Check for fault or warning number.
0	0	0	1	1	MS Power off. Recovery engaged (Recovery mode)	Check MS electrical equipment and MS power supply. Check for fault or warning number.
0	1	0	0	0	Not allowed (Indication for hardware problem)	Check electrical equipment. Check for fault or warning number.
1	0	0	0	0	MS Hardware fault. (wiring, power supply, etc.)	Check MS fault number.
1	1	0	0	0	Not allowed (Indication for hardware problem)	Check MS electrical equipment. Check for MS fault or warning number.
0	0	1	1	0	Self-test or recovery pre-engagement	-
0	0	1	1	1	Self-test or recovery mode	-
0	1	1	0	0	Normal (ready or following)	-
1	0	1	0	0	MS Fault (overspeed, self-test, etc.)	Check fault or warning number.
1	1	1	0	0	Not allowed (Indication for hardware problem)	Check electrical equipment. Check for fault or warning number.

Legend:
	Mandatory signals/indicators
	Optional signals/indicators

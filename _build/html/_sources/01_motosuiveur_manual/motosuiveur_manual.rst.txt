MotoSuiveur Manual
========================

Revision history
----------------------

.. kept from word document, useful?

.. csv-table:: test table 2
   :file: 06_tables/revisionTable2020.csv
   :header-rows: 1

Introduction
----------------

The object of this manual is to present operation modes of MotoSuiveur® (further called MS). Manual describes electrical part of MS, MS operation modes, troubleshooting and maintenance. On :numref:`MotoSuiveur® main block diagram` is presented MS main block diagram.

.. _MotoSuiveur® main block diagram: 
.. figure:: 05_images/ms_main_block_diagram.png
	:scale: 75 %
	:align: center
	
	MotoSuiveur® main block diagram


Glossary
---------

.. figure:: 05_images/glossaryImage.png
	:scale: 75 %
	:align: center
   	
	MS unit components	

.. csv-table:: MS unit components
   :file: 06_tables/ms_unit_components.csv
   :header-rows: 1
   :width: 11
   :widths: 1 5 5

.. --------------------------------------------------------------

.. figure:: 05_images/glossaryImage2.png
	:scale: 75 %
	:align: center
   	
	General view of MS control cabinet front door	

.. csv-table:: MS control cabinet front door
   :file: 06_tables/generalViewMSCCfront.csv
   :header-rows: 1
   :width: 100
   :widths: 1, 5, 2

.. --------------------------------------------------------------

.. figure:: 05_images/generalViewOperationModes.png
	:scale: 75 %
	:align: center
   	
	General view of the sequence of MS operation modes	

.. -------------------------------------------------------------- 

Mechanical characteristics of MS are presented on the nameplate of the MS. The nameplate of the MS indicates the maximum rotating speed, the corresponding braking torque and other characteristics (mass, oil quantity, etc.). Example is shown on figure 5.

.. figure:: 05_images/MSnameplate.png
	:scale: 75 %
	:align: center
   	
	MS nameplate	

.. --------------------------------------------------------------



Connect MS to control cabinet
------------------------------------

After mechanical assembly of MS to hoist is done, electrical connection must be made between MS and control cabinet. Figure 7 shows general view of typical MS unit electrical components that should be connected according specific for the project electrical circuit diagram.

.. figure:: 05_images/electricalConnections.png
	:scale: 75 %
	:align: center
   	
	Electrical connections of MS unit

№	Description	№	Description
1	C8 - Recovery motor connector	3	C6 - Power connector
2	TSW - Position switches terminal	4	C7 - Resolver connector

Connectors C6 and C7 (figure 6 points 3 and 4) should be made according following specification:
For C7 connector screened cable with 4 twisted pairs, 0.25 mm² should be used. Ground the shield of the feedback should be connected to GND - figure 7 a);

For C6 connector should be used screened cable, 4 core, 1.5 mm². Ground the shield of the feedback should be connected to GND - Figure 7 b).

	Figure 7 c) shows signal arrangement of connector on motor side for motor type Kollmorgen. 
	Figure 7 d) shows general MS motor view. 
 
.. figure:: 05_images/C7connector.png
	:scale: 75 %
	:align: center
   	
	C7 connector
 
a) C7 connector

.. figure:: 05_images/C6connector.png
	:scale: 75 %
	:align: center
   	
	C6 connector

b) C6 connector

.. figure:: 05_images/connectorDrawing.png
	:scale: 100 %
	:align: center

	Kollmorgen motor (1)

.. csv-table:: Kollmorgen motor (1)
   :file: 06_tables/connectorTable01.csv
   :header-rows: 1
   :width: 100
   :widths: 1, 5, 5

.. figure:: 05_images/connectorDrawing2.png
	:scale: 100 %
	:align: center

	Kollmorgen motor (2)

.. csv-table:: Kollmorgen motor (2)
   :file: 06_tables/connectorTable02.csv
   :header-rows: 1
   :width: 100
   :widths: 1, 5, 5

c) Kollmorgen motor
 
.. figure:: 05_images/generalViewMSmotor.jpg
	:scale: 60 %
	:align: center

	Connectors C6 and C7

d) General view of MS motor

.. warning::
    ATTENTION
    C6 and C7 must be connected according specification! Wrong connection can cause motor damage!


On :numref:`MS recovery motor C8 terminal connection` is MS recovery motor electrical connector. Recovery motor is DC motor controlled by Siguren motor controller MSRM4514. Working voltage of motor is 48VDC therefore is very important motor to be connected correctly. Correct connection is shown on figure 8.

.. _MS recovery motor C8 terminal connection:
.. figure:: 05_images/MSrecoveryMotorTerminal.jpg
	:scale: 60 %
	:align: center

	MS recovery motor C8 terminal connection

Position switches are used for allowing or prohibiting hoist movement. Position switches are using in active output signal via NC contact. Signal from switches should be active in case when switches are not in contact with worm and worm is in correct position. Figure 9 a) combination of signals form position switches is shown. Position switches are shown on figure 9 b).

.. figure:: 05_images/combinationSignalsPositionSwitches.png
	:align: center

	Combination of signals from position switches

.. figure:: 05_images/positionSwitches.png
	:scale: 100 %
	:align: center
	
	position switches

Terminal block TSW (Terminal SWitches) is used for connection of worm position proxy sensors/switches and control cabinet. Figure 10 shows general view of TSW and description of terminals.

.. figure:: 05_images/terminalBlock.png
	:scale: 100 %
	:align: center
	
	Terminal block TSW

.. csv-table:: Terminal block TSW
   :file: 06_tables/terminalBlockTSW.csv
   :header-rows: 1
   :width: 100
   :widths: 1, 5


.. csv-table:: Terminal block TSW
   :file: 06_tables/terminalBlockTSW.csv
   :header-rows: 1
   :width: 100
   :widths: 1, 5

Terminal blocks in control cabinet are for connection between MS and control cabinet. Terminal blocks are described in :numref:`Control cabinet terminals`.

.. _Control cabinet terminals:
.. csv-table:: Control cabinet terminals
   :file: 06_tables/controlCabinetTerminals.csv
   :header-rows: 1
   :width: 100
   :widths: 1, 5

:numref:`General view of connection between MS and MSCC` shows general view of connection between MS and control cabinet (MSCC). For more detail about connection, please review electrical circuit diagram for the corresponding project.

.. _General view of connection between MS and MSCC:
.. figure:: 05_images/generalViewConnectionsMS-MSCC.png
	:scale: 80 %
	:align: center

	General view of connection between MS and MSCC

.. Figure 11 General view of connection between MS and MSCC



Indication lamps and controls
---------------------------------

Indication lamps and local controls are shown on figure 3. They are located on front door of control cabinet. 
Indication lamps indicates:
	- MS status - figure 3, items 2, 8;
	- allowed movement direction of hoist - figure 3, items 1, 3, 9;
	- recovery mode status - figure 3, items 10, 11.
  
Local controls are used for:
	- reset of MS - figure 3, item 7;
	- overrides MS enable signal (override ON signal) - figure 3, item 6;
	- enable and control MS Backup/ Recovery mode - figure 3 items 4, 5, 10, 11.

:numref:`Control signals between hoist and MS` shows schematically the control signals between hoist and MS. 
 
.. _Control signals between hoist and MS:
.. figure:: 05_images/controlSignals.png
	:scale: 100 %
	:align: center

	Control signals between hoist and MS

.. warning::
 	Local control commands can be duplicated with remotes!
	Please, check electrical circuit diagram!



Hoist enabled
^^^^^^^^^^^^^^^^^^^^^

Hoist enabled lamp indicate that the MS authorizes hoist movements. (figure 5). Hoist enabled signal will on only in case if ON signal from hoist is ON.

Hoist enabled signal will be ON when MS self-test pass successfully and ON signal is available then Hoist enabled and Healthy indicator lamps are on. The signals are indicating system ready (MS ready).



Fault 
^^^^^^^^^^^^^^^^^^^^^

Fault lamp (figure 3, item 2) indicates three different types of faults:
	- MS controller internal errors, described in section 7.1;
	- MS faults (further called flt_num), described in section 7.2;
	- MS warnings (further called wrn_num), described in section 7.2;

MS controller internal errors are related to MS controller internal hardware, firmware, and MS motor. This type of errors are with highest priority. If MS controller internal fault appear further operation is prohibited.
	
.. note::	
 	Fault lamp indicator is on during MS self-test.

.. warning:: 
	The system displays only last MS warning (wrn_num) or MS fault (flt_nim) occurred.

.. ------------- Substitution definitions for 7-segments digits -------------------
	to be able to include them INLINE in the next paragraph
.. |image001| image:: 05_images/_digits/image001.png 
.. |image003| image:: 05_images/_digits/image003.png 
.. |image007| image:: 05_images/_digits/image007.png 
.. |image009| image:: 05_images/_digits/image009.png 
.. |image011| image:: 05_images/_digits/image011.png 
.. |image013| image:: 05_images/_digits/image013.png 
.. |image015| image:: 05_images/_digits/image015.png 
.. |image017| image:: 05_images/_digits/image017.png 
.. |image019| image:: 05_images/_digits/image019.png 
.. |image021| image:: 05_images/_digits/image021.png 
.. |image023| image:: 05_images/_digits/image023.png 
.. |image025| image:: 05_images/_digits/image025.png 
.. |image027| image:: 05_images/_digits/image027.png 
.. |image029| image:: 05_images/_digits/image029.png
.. |image031| image:: 05_images/_digits/image031.png 
.. |image033| image:: 05_images/_digits/image033.png 
.. |image035| image:: 05_images/_digits/image035.png
.. |image036| image:: 05_images/_digits/image036.png
.. |image039| image:: 05_images/_digits/image039.png
.. |image041| image:: 05_images/_digits/image041.png 
.. --------------------------------

Faults and warnings are displayed on MS 7 - segment controller. The display indicates 
all types of MS warnings/faults and MS controller internal errors. 
Indication is a combination of letters and numbers. MS controller internal 
faults are indicated with blinked combination of |image035|, number and finish 
with symbol |image039|.

MS faults are displayed with combination of |image036| and number. 
MS warnings are displayed with combination of |image035| and number. 

.. rubric:: Displaying messages on MS controller 7 - segment display

On :numref:`MS controller internal error E01` is shown example for internal MS controller fault. 
On :numref:`MS warning number 10 (wrn_num = 10)` is shown example for MS warning.

.. _MS controller internal error E01:
.. figure:: 05_images/MScontrollerInternalErrorE01.png
	:scale: 100 %
	:align: center

	MS controller internal error E01 

.. _MS warning number 10 (wrn_num = 10):
.. figure:: 05_images/MSwarningNumber10.png
	:scale: 100 %
	:align: center

	MS warning number 10 (wrn_num = 10) 

.. note::		
 	After MS reset, all types of faults are cleared. Before MS reset, fault should be resolved.


Upward enable/Downward enable 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Upward enable/Downward enable are indicators for authorized direction of hoist movement. 
If one of the two directions is forbidden to move, it is necessary to move the hoist 
in the opposite direction in order to reset the system mechanically.

Movements upward and downward of hoist are correspond to screwing and unscrewing 
movement of MS worm. Movement directions of worm are corresponding to directions 
of clock. Direction screwing is clockwise, unscrewing direction is anticlockwise, 
viewed from cam part of the screw shaft as is shown 
on :numref:`MS Worm rotating directions`.
 
.. _MS Worm rotating directions:
.. figure:: 05_images/MSwormrotatingDirections.png
	:scale: 80 %
	:align: center

	MS Worm rotating directions 

.. line-block::
	1 - Screwing direction
	2 - Unscrewing direction

.. warning::
 	After MS reset or manual centering of the worm and MS restart, 
	no movement is performed or faults appears, please contact SIGUREN 
	technologies on address support@siguren.com


Backup/Recovery Off/On; Backup/Recovery Down/Up
^^^^^^^^^^^^^^^^^^^^^

Backup function allows the load to be lowered down, by using minimal functionalities 
when MS is in Following operation mode. Backup function ignore all settings related 
with nominal following operation mode and allows movement of the hoist with limited speed.

Recovery function is used when the main hoisting chain is faulty (for example damaged
brake of the hoist motor). Recovery system allows lowering load safety to the ground.

Enable Override
^^^^^^^^^^^^^^^^^^^^^

Enable override can be used if it is necessary to override Hoist enabled. This allows 
small movements for MS mechanically reset.

Lamp states
^^^^^^^^^^^^^^^^^^^^^

Combination of active (ON) and inactive (OFF) signal lams gives current status of MS. 
In Appendix Table 1 signal combinations are presented and described.



MS operating modes
-------------------

MS controller internal check
^^^^^^^^^^^^^^^^^^^^^

At power on (or restart) MS starts operating according figure 3. According sequence of 
MS operation modes first operation is MS controller internal check. Internal check is 
intended to hardware, firmware of MS controller, MS motor and MS motor resolver. 

In case of fault, fault is visualized on 7 - segment display as described in 5.1.2. 
Further operations are prohibited. List with MS controller internal faults are listed 
in section 7.1.

Self-test operation mode
^^^^^^^^^^^^^^^^^^^^^

After MS controller internal check finishes, Self-test operation mode (further called self - test) starts. On figure 15 a) symbols indicated self-test steps on MS controller 7 - segment display are shown. On figure 15 b) is shown sequence of self-test steps.

.. _Self-test steps symbols:
.. csv-table:: Self-test steps symbols
   :file: 06_tables/SelfTestStepsSymbols.csv
   :header-rows: 1
   :width: 100
..   :widths: 1, 5

"*" steps are applicable only for hydraulic MS.

.. _Sequence of self-test steps:
.. figure:: 05_images/SequenceSelfTestSteps.png
	:scale: 80 %
	:align: center

	Sequence of self-test steps 

Fields with *, ** and *** are related with Table 2 in section 7.2



Electrical test
+++++++++++++++++++++++++++++

On :numref:`Steps of Electrical test`  test are shown. Test checks for active signals on 
inputs of the MS controller before self-test begin.

.. _Steps of Electrical test:
.. figure:: 05_images/stepsElectricalTest.png
	:scale: 80 %
	:align: center

	Steps of Electrical test 


.. warning::
 	In case of repetitive faults, please contact SIGUREN technologies on address support@siguren.com!


Switch test
+++++++++++++++++++

Switch test check connection between MS controller and SCRE/USCRE switches 
(figure 2, items 4, 5), centered position and functionality of switches. 
On figure 8 are shown steps of Switch test. 

In Table 2 located in appendix are shown steps for visual check of Switch test. 
Visual check of Switch test is necessary only in case if repetitive faults during 
the test appears.
 
.. _Steps of Switch test:
.. figure:: 05_images/stepsSwitchTest.png
	:scale: 80 %
	:align: center

	Steps of Switch test 

.. note::
 	In case of repeatedly wrn_num occurs, please check:
	
    	- connection between MS control cabinet and SCRE/USCRE switches;
    	- functionality of SCRE and USCRE switches;
    	- signals on inputs of MS controller and operational relays RSESw and RUESw located in MS control cabinet;

Play test
+++++++++++++++++++

Play test measures play between worm and worm wheel. On :numref:`Play test steps` steps of Play 
test are shown.

.. _Play test steps:
.. figure:: 05_images/playTestSteps.png
	:scale: 80 %
	:align: center

	Play test steps

.. warning::
 	In case of repetitive faults, please contact SIGUREN Technologies on address support@siguren.com!

Following operation mode
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Following operation mode starts after successful passed of self - test. The function of this operation mode is intended for follow movements of the hoist and to monitor for exceeding the rated speed (nominal speed) with defined positive tolerance. The speed, which is considered high is called Overspeed. By design MS will not allow Overspeed. Typically Overspeed is equal to:
Overspeed = Nominal speed + 10%				(1)



:numref:`Main principle of following` presents main principle of Following operation mode and overspeed detection. 
On :numref:`Principle of Following operation mode` steps of following operation mode is 
presented. On :numref:`Symbols displayed on 7-segment display on MS controller` are shown symbols displayed on 7 - segment display during 
following operation mode.

.. _Main principle of following:
.. figure:: 05_images/mainPrincipleFollowing.png
	:scale: 100 %
	:align: center

	Main principle of following operation mode and overspeed detection

.. line-block::
	1 - Acceleration	
	2 - Following	
	3 - Deceleration 
	4 - Exceeding nominal speed 
	5 - Overspeed detection	
	6 - Overspeed detected. MS is braking

.. _Principle of Following operation mode:
.. figure:: 05_images/principleFollowingMode.png
	:scale: 100 %
	:align: center

	Principle of Following operation mode
 

.. _Symbols displayed on 7-segment display on MS controller:
.. figure:: 05_images/symbolsDisplayed.png
	:scale: 100 %
	:align: center

	Symbols displayed on 7-segment display on MS controller



Backup/Recovery operation mode
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Backup/Recovery operation mode functions are intended to unusual situations during MS 
operating. Controls and indicators of this functions are located on control panel front 
door - figure 3, items 4, 5, 10, 11.

On figure 23 is shown principle of Backup/Recovery operation mode. Backup/Recovery 
decision figures located in figures 15 and 20 with dotted outline, represent the 
places where request for these operation modes are checked. 

Switching on Recovery/Backup mode is performed through Backup/Recovery OFF/ON key - 
figure 2, item 4. After switching Backup/Recovery mode on, Backup mode start operating. 
On 7 - segment display indication for backup mode is displayed   and Recovery mode lamp 
is on. Backup function ignore all settings related with following operation and allows 
movement of hoist with hoist limited speed.

In Backup operating mode, control is performed trough commands for lifting and lowering 
of the hoist. In case of hoist control chain is damaged, control can be performed manually 
directly on control terminals located in MS control cabinet via wire bridge. Example is 
shown on figure 22. In Backup mode no ON signal is required to perform movement of MS. 

.. _Example for manual operation in backup mode:
.. figure:: 05_images/exampleManualOperationBackup.png
	:scale: 100 %
	:align: center

	Example for manual operation in backup mode

.. _Principle of Backup/Recovery operation:
.. figure:: 05_images/principleBackupRecoveryOperation.png
	:scale: 100 %
	:align: center

	Principle of Backup/Recovery operation

Recovery mode is second part of Backup/Recovery operation. This mode start operates 
the way is shown on figure 23. 

After reset, MS checks for active Backup/Recovery mode 
request (Backup/Recovery operational key is ON). If request is active 7 - segment display 
shows symbol for Recovery mode |image041| and engagement start. Engagement function is used to 
engage recovery mechanism to the worm via recovery nut - figure 1, item 7.

Completion of engagement is indicated by Recovery engaged indication lamp (figure 3, 
point 10). If lamp is off after first engagement, reset is needed. Reset will activate 
engagement again.

Controlling of Recovery is with 3 - position key Backup/Recovery Down/Up located on front 
door of control cabinet - figure 3 item 5. Also Recovery can be controller remotely if 
that is provided by electrical circuit diagram.

After engagement is complete and Recovery engagement lamp is on, brake of main hoist 
motor should be released. Otherwise motor brake will prohibit movements. Brake should 
remain open until recovery operation done.

For disengagement, load should be on safe place, main hoist motor brake should be 
closed. Command for lowering should be given to MS until both lamps for Upward enable 
and Downward enable becomes on.
	
.. warning::
 	Recovery function is mainly designed for safety lowering of the load. Function 
	 allows very short lifting of the load only in case if it is absolutely necessary!

.. warning::
 	Before activating Backup/Recovery operation mode from local controls 
	(figure 3, item 4), please make sure that operation mode is not activated 
	remotely. The verification consists of the following steps:
	 
	- Recovery mode lamp and Recovery engaged lamp are off;
	- Backup/Recovery control key is in position “0” (OFF);
	- On 7 - segment display symbols   or   are not displayed.
	

Troubleshoot and maintenance
------------------------------

Troubleshooting of MS can be done by few ways:
	
- via signal lamps located on front door - Appendix 1;
- via MS controller 7 - segment display - section 6.1;
- via touchscreen HMI (MSHMI) - section 6.2. 


Troubleshooting via MS controller 7 - segment display
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

MS controller internal errors
++++++++++++++++++++++++++++

.. _MS controller internal errors:
.. csv-table:: MS controller internal errors
   :file: 06_tables/MScontrollerErrors.csv
   :header-rows: 1
   :width: 100
..   :widths: 1, 5


MS faults and warnings
++++++++++++++++++++++++++++++

.. _MS faults and warnings:
.. csv-table:: MS faults and warnings
   :file: 06_tables/MSfaultsWarnings.csv
   :header-rows: 1
   :width: 100
..   :widths: 1, 5

.. warning::
 	In case of repetitive faults, please contact SIGUREN Technologies on address support@siguren.com!


MSHMI
^^^^^^^^^

The MSHMI is a Schneider Magelis HMI STU 655/855 color graphic touchscreen terminal programmed with the MSHMI firmware by Siguren technologies. MSHMI communicates with MS controller via MODBUS RTU protocol - figure 24.
 
Figure 24 MSHMI
	Advantages if using MSHMI to operating with MS® are:
	- Display MotoSuiveur® status information in the form of messages, event listings, graphics and numerical values;
	- Change the MotoSuiveur® configuration. Configuration is a secure access code at different levels;
	- Change operating mode of MotoSuiveur®;
	- Display maintenance information of MotoSuiveur®.

.. note::
	INFORMATION
 	MSHMI is not part from standard MS equipment and can be ordered additionally.

6.3	Maintenance
^^^^^^^^^^^^^^
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
	The reliability of the Motosuiveur® will depend if the maintenance procedure is strictly adhered to. Maintenance operations are to be done based either on the Maintenance type displayed on MS controller 7 - segment display or on a time basis wherever the smallest value applies.

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

Appendix 1: Signal Lamps
----------------------------

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

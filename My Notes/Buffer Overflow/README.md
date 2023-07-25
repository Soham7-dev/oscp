<span style="color:red"> <b>*NO LONGER REQUIRED FOR OSCP (REMOVED FROM THE SYLLABUS)*<b> </span>
 
 ## **Env setup**
		1. Mona working directory
		2. Run the binary/service
		3. Start immunity debugger as admin
		4. Attach the process
	
## **Fuzzing**
		1. Identify crashing point
		2. Msf pattern create -l crashpoint

## **Control EIP**
		1. Msf pattern offset -q EIP value
		2. Exploit code set offset and observe EIP value

## **Finding bad chars**
		1. Generate all bad chars with python
		2. Generate bad chars with mona bytearray
		3. Mona compare with esp address (or follow esp dump manually)
		4. Remove next bad char from payload, fire
		5. Generate new mona bytechar with excluded bad char
		6. Repeat steps e and f for all bad chars until unmodified

## **Find jump esp**
		1. Find with mona
		2. Select address with no money protections (jmp esp)

## **Generate shellcode**
		1. Msfvenom -f py EXITFUNC=thread
		2. Exclude all bad chars with -b
		3. -v exploit script payload variable name

## **Grand Finale!**
		1. Prepend NOPS! (4/8/16)
		2. Buffer = prefix + overflow + retn + padding + payload + postfix

https://github.com/Tib3rius/Pentest-Cheatsheets/blob/master/exploits/bufferoverflows.rst

**[BACK](ST101MIDTERM03)**

## Control Bus
- is used by the CPUs to communicate with other devices within the computer system.
	- As the address bus carries the location of the data being sent and the data bus carries the actual data being processed
	- The control bus carries the commands/instructions from the CPU.
- It also sends status signals from the devices, identifying if it is ready or not.
>[!EXAMPLE]
> The typical read/write commands are identified through the control bus.
>- e.g. if one tries to save a file to a flash drive that is already removed from the computer, the computer will notify the user with an error message saying that the folder or drive where the file is intended to be saved is no longer existing.
>	- This is because the original destination/location can no longer be sent through the address bus because of the disconnection. Therefore, the CPU sends a halt instruction via the control bus, stopping the data be sent through the data bus, often seen as an error message prompt.

>[!FAQ] Control Bus
> used to carry control signals.
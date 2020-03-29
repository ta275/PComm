# PComm
Parallel and synchronous communication between two embedded platforms using a 4-phase handshake.

The purpose of this short project is two fold:

to provide a fast, parallel communication protocol for communication between two embedded devices

to design the software in such a way that it's easily extensible so that it can support many new features

Features:
	Written in C so it's super-fast
	
	Careful object-oriented design done in C, hence easy to use, extensible, and easily modifiable

	"WHAT!! But C is not an object-oriented programming language!" - Have a look at this {http://faculty.washington.edu/gmobus/Academics/TCES202/Moodle/OO-ProgrammingInC.html} webpage from WashU.

	Supports master->slave configuration between a Raspberry Pi 3B+ and AVR microcontrollers.

	Parallel 8-bit synchronous communication protocol, with estimated 5x speedup over the UART serial protocol.

	The protocol is actually an n-bit protocol, the speedup can be even higher if more bits are used.

	Synchrony is independent of clock speeds of the platforms, i.e, don't have to worry about mismatch in clock speeds.



All said and done, there are still many improvements that can be made, components that can be better documented/explained. But if you're an intermediate/advanced embedded engineer or software engineer, you can use it in your own projects with relative ease.


The biggest advantage of the software along with the protocol is its wide applicability. The protocol requires a minimum of 2-bits (i.e, 2 GPIOs). So it can be used "like" a serial communication protocol, but it might be slower than traditional protocols. But instead, if you wish to use more GPIOs, then you can increase the speed significantly. And most importantly, you don't have to worry about the timing of the pins. It's a win-win for embedded developers and software developers alike - saving their time and effort!

The code currently supports master->slave (unidirectional) configuration but can be easily extended bidirectional communication and many platforms.

The current code is meant for communication between a Raspberry Pi 3B+ and AVR microcontrollers.

The master->slave configuration was tested on the Atmega2560 microcontroller.


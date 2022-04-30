# Computer Basics

## What makes a computer a computer?

Computers were developed to help with the mental side of work. Every computer has four common elements:

- Input: how information gets into the computer. This can range from a person typing numbers on a keyboard to the heartbeat sensor on a smart watch. 
- Store: where and how the computer keeps that information
- Process: the information is taken from storage, modified using a series of commands (an algorithm), and then returned to storage to either be output or modified again. 
- Output: just like input can come from a wide range of sources, the output can take many different forms, from text on a screen to a virtual reality game. In more complex systems, one computer's output often becomes another computer's input. 

## Binary & Data

At their most basic, computers communicate in binary, often represented as zeroes and ones. Computers are controlled by electrical signals; the only information electricity can communicate is whether it's on (1) or off (0). The on/off state of a single wire within a circuit is the most basic piece of information a computer can store, and is called a "bit." The more bits you have, the more complex information you can work with.

Binary can use ones and zeroes to represent any number. The more wires you have communicating in binary, the more numbers you can represent (try a [binary calculator](https://www.calculator.net/binary-calculator.html) to see how different numbers work). Those numbers can represent numbers, but they can also represent letters (A = 1, B = 2, etc.), sounds, or colors (like rgb(255, 23, 104)). Individual blocks of color, called pixels, can then be arranged (using instructions stored in binary) into images to display on a screen.

## Circuits & Logic

Every input to a computer is a piece of information stored in binary. The computer processes that information using millions of tiny electrical components, organized into circuits. 


One very simple type of circuit is known as a "not" circuit. It always outputs the opposite of its input. A slightly more complicated circuit is "and," which has two inputs and one output. This circuit will only out put a 1 if both inputs are 1; inputs of 0 and 1, 1 and 0, or 0 and 0 will all produce a 0 output.

These and other simple circuits can be connected together to make much more complicated calculations. An "adder," for example, can add two inputs together, and a series of adders connected together can add increasingly larger numbers. There are other circuits that can subtract or multiply, but more complex operations are always based on these simple building blocks. 

Modern computers are faster than old computers not only because they're more advanced, but literally because they're smaller. Electricity takes time to travel from one part of a circuit to another, so making the distance between those parts smaller lets the information travel faster. While this amount of time is tiny by human standards, over billions of calculations, it adds up considerably.

## CPU, Memory, Input & Output

When a computer receives input, it converts that input to a binary number. That number is stored in the computer's memory, and may be modified by its central processing unit (CPU). The information is then sent to the output.

For instance, if you type (input) a letter, that letter is converted to a number and sent to the computer's memory. The CPU, upon receiving a letter input, will look in the memory for instructions on how to display that letter. It executes those instructions, which outputs information to the computer's display telling it how to arrange pixels so you can see the letter you typed. All of this happens in less time than it takes to read a single word of this paragraph.

Displaying a letter on a screen is one of the simpler forms of output from a modern computer. A more complex output, like a 3D virtual world, requires so many simultaneous calculations that the computer may use multiple processors and lots of memory. 

## Hardware & Software

"Hardware" describes the physical components of a computer. "Software" describes the programs running on the machine, which tell the physical components how to behave. 

The CPU is the piece of hardware that controls all other parts of the computer and is made up of several simpler parts. Some circuits perform calculations, and others communicate with various parts of the computer. The CPU receives commands and information from memory, and uses those commands to understand what to do with the data.

While the CPU can only understand binary, writing code in binary would be extremely difficult, both for time and comprehensibility reasons. 

The master program on the computer that controls all the others is called the operating system. It contains the instructions that tell the CPU how to install and use other software. Because computers rarely do one thing at a time, the operating system also controls when and how each program uses the CPU, so everything can run together smoothly. 
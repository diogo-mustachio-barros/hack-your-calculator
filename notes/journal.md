# Focus
## The calculators
Our target calculators are the TI-83 and TI-84 (Plus or not) as they share the same software and 
    can share programs as well. These calculators are the standard for graphic calculators here in
    Portugal. The other calculators we use are the TI-Nspire and some Casio models. The TI-Nspire 
    is very different from the others and is much more powerful, but more importantly, is 
    programmed in different ways. The Casio models are more sparse (the vast majority are TI-84s)
    and are programmed in another language (which does not seems as appealing as TI's).

## The language
The TI-Basic language is a very simple language inspired on the Basic language.

## The goal
- To teach some programming basics
- Bring a programming tool with real effects closer to students
- Plant seeds of curiosity towards programming


# Setting up the environment
There are some tools we need here. The development cycle (if you can call it that) goes as follows:
1. Write on an editor
2. Compile into a binary
3. Transfer binary to calculator
4. Test/execute on the calculator

To support this cycle I've decided to recommend:
- **TokenIDE** as an editor and compiler
- The official **TI Connect** software to connect to the calculator
- For the cases where students might not bring their calculator or don't even have one, I'll be 
    using **Wabbitemu** as an emulator for the TI-84 Plus

## TokenIDE
TokenIDE is still (since 2016 from my experience) the best editor for TI-Basic. Although very 
    bare-bones, it has a simple editor with some highlighting to help with possible errors and
    can compile the binary.

Probably the best aspect of TokenIDE is that you download it as a `.zip` and it comes as a 
    single `.exe` so there is no installation, only a download (and unzipping).

## VSCode
I've tried to use VSCode as an editor/compiler but existing extensions are very lackluster and 
    building one would be too much of a time investment for what it's worth.

## Wabbitemu
Installing is very straightforward, the only step that requires some extra (legal) thought is 
    acquiring the TI-84 Plus' OS.

After all is setup, to transfer programs to the emulated calculator we simply open the compiled
    binaries (as long as they are valid) and they appear in the `PRGM` section.

# The Website
Although not necessary, a website would help streamline the activity.
Although we will not have a lab (just maybe 2 machines), this may be useful for students to later
    'participate' and try at home rather than lose contact. There is also a chance that they spread
    the word about this activity, and therefore spread word about FCUL.

# Planning
The activity will take place on the 3rd of may between 10:00 and 12:30, and between 14:00 and 16:30.
Each block of activity lasts for 20 min.

| ID |     Hour      | # Participants |
| -: | :-----------: | :------------: |
|  1 | 10:00 - 10:20 |       00       |
|  2 | 10:20 - 10:40 |       01       |
|  3 | 10:40 - 11:00 |       02       |
|  4 | 11:00 - 11:20 |       01       |
|  5 | 11:20 - 11:40 |       01       |
|  6 | 11:40 - 12:00 |       07       |
|  7 | 12:00 - 12:20 |       04       |
| -- |   **LUNCH**   |   **LUNCH**    |
|  8 | 14:00 - 14:20 |       00       |
|  9 | 14:20 - 14:40 |       10       |
| 10 | 14:40 - 15:00 |       00       |
| 11 | 15:00 - 15:20 |       00       |
| 12 | 15:20 - 15:40 |       00       |
| 13 | 15:40 - 16:00 |       02       |
| 14 | 15:40 - 16:00 |       06       |

**Total:**
- Manhã - 16
- Tarde - 18
- Dia - 34

## Plan

- Intro to the activity
    - Welcome to FCUL
    - Objectives
        - Program on the TI-84 (or 83)
        - Create entertainment apps or custom tools for learning
- Intro to the calculator
- Crash course into TI-BASIC
- Conclusion & aftermath

## Story

- Welcome to FCUL
- Welcome to 'Hack your calculator'
- The goal for today is learn how to 'bend' the calculator to our will
- Graphical calculators can be programmed
- TI-Basic is a complete programming language
- Programming cycle: write -> compile -> execute/run
- How to program in TI-Basic
    - Where to write (& compile): TokensIDE
    - How to run: send to calculator (TI Connect), or emulator (Wabbitemu)
- Goals for the activity (at least one of the following):
    - Guessing game
    - Slots
    - Defuse the bomb
- Choose one of the games and follow the tutorial
- Any questions/problems -> Feel free to ask!
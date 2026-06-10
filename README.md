\# Cryptographic System – Information and Cybersecurity (BCC2213/TNS4014)



\## Assignment 1 – Part 1: Cryptography and Data Protection



\### Student Information

\- \*\*Name\*\*: Tai Wen Hong  

\- \*\*Student ID\*\*: SUKD2502284  

\- \*\*Course\*\*: Bachelor of Computer Science (Hons) in Cybersecurity  

\- \*\*Semester\*\*: May 2026  

\- \*\*Submission Date\*\*: 10 June 2026  



\---



\## Overview



This project implements a browser‑based cryptographic system that demonstrates four traditional encryption techniques:



\- \*\*Additive (Caesar) Cipher\*\*  

\- \*\*Simple (Keyword) Cipher\*\*  

\- \*\*Vigenère Cipher\*\*  

\- \*\*Rail Fence Cipher\*\*  



The system provides an interactive graphical user interface where users can enter plaintext, select an algorithm, provide a key, and encrypt/decrypt messages. A step‑by‑step animated console shows every character transformation in real time.



\---



\## Features



\- Clean, responsive GUI with a dark theme and glowing border animations.

\- Dropdown menu to select any of the four ciphers.

\- Dynamic key input field with context‑sensitive placeholders.

\- \*\*Encrypt\*\* and \*\*Decrypt\*\* buttons with loading states.

\- Output area with a \*\*Copy\*\* button to copy results to the clipboard.

\- Real‑time step‑by‑step console (MacOS‑style terminal) that displays:

&#x20; - Substitution calculations (Caesar, Simple, Vigenère)

&#x20; - Row placement (Rail Fence)

&#x20; - Non‑alphabetic character preservation

\- Input validation:

&#x20; - Numeric keys required for Additive and Rail Fence.

&#x20; - Alphabetic keys required for Simple and Vigenère.

\- Handles long messages gracefully (console step truncation with omission notice).

\- Preserves spaces, punctuation, digits, and special characters (only letters A‑Z are transformed).



\---



\## Running the Program



The application is a \*\*single HTML file\*\* with inline CSS and JavaScript. No external dependencies, web servers, or installations are required.



\### Steps:



1\. Download or copy the file `index.html` (the provided HTML code).

2\. (Optional) Place a custom `computer.gif` in the same folder – the page references this image. If the file is missing, the browser will show a broken image icon (the system still works).

3\. Double‑click the HTML file to open it in any modern web browser (Chrome, Firefox, Edge, Safari).

4\. Start using the cryptographic system.



> \*\*Note\*\*: All encryption/decryption is performed locally in your browser. No data is sent to any server.



\---



\## Usage Instructions



1\. \*\*Enter your message\*\* in the “Message (Plaintext)” text area.  

&#x20;  \*Example:\* `CYBERSECURITY`



2\. \*\*Select a cipher\*\* from the dropdown menu.



3\. \*\*Enter the appropriate key\*\*:  

&#x20;  - Additive Cipher → a number (e.g., `8`)  

&#x20;  - Simple Cipher → a keyword consisting only of letters (e.g., `BLUE`)  

&#x20;  - Vigenère Cipher → a keyword consisting only of letters (e.g., `KEY`)  

&#x20;  - Rail Fence Cipher → an integer ≥ 2 (e.g., `3`)



4\. Click \*\*Encrypt Message\*\* to transform the plaintext into ciphertext, or \*\*Decrypt Message\*\* to reverse the process.



5\. Watch the right‑hand console animate each step of the algorithm.



6\. The result appears in the “Output Result” field. Click \*\*Copy Result\*\* to copy it to your clipboard.



\---



\## Example Test Cases (Encryption)



| Cipher          | Plaintext         | Key   | Ciphertext (actual output) |

|----------------|-------------------|-------|-----------------------------|

| Additive        | CYBERSECURITY     | 8     | KGMZMAMKCZQBG                |

| Simple          | ATTACK            | BLUE  | BSSBUI                      |

| Vigenère        | HELLO             | KEY   | RIJVS                       |

| Rail Fence      | SEGI UNIVERSITY   | 3     | S VIEIUIESTGNRY              |



\*Note: For Rail Fence, the space in the plaintext is preserved and placed according to the zig‑zag pattern.\*



\## Example Test Cases (Decryption)



| Cipher          | Ciphertext                    | Key   | Restored Plaintext        |

|----------------|-------------------------------|-------|---------------------------|

| Additive        | KGMZMAMKCZQBG                 | 8     | CYBERSECURITY             |

| Simple          | BSSBUI                        | BLUE  | ATTACK                    |

| Vigenère        | RIJVS                         | KEY   | HELLO                     |

| Rail Fence      | S VIEIUIESTGNRY               | 3     | SEGI UNIVERSITY           |



\---



\## File Structure

BCC2213\_MAY26SEM\_ASSIGNMENT1\_SUKD2502284/

├── crypto\_system.html (main program – all code in one file)

├── computer.gif (optional animation, referenced by the HTML)

├── README.md (this file)

└── \[assignment report PDF] (submitted separately)



\---



\## Technologies Used



\- \*\*HTML5\*\* – page structure and semantic elements  

\- \*\*CSS3\*\* – responsive layout, animations, custom theming, and glowing borders  

\- \*\*JavaScript (ES6+)\*\* – cipher logic, DOM manipulation, async step‑by‑step console, clipboard API  



No external libraries are required. Font Awesome icons are loaded from a CDN (optional, improves visual icons).



\---



\## Known Limitations



\- The system only transforms \*\*alphabetic characters (A‑Z, a‑z)\*\*. Digits, punctuation, and spaces remain unchanged (spaces are kept as‑is, but are included in the Rail Fence zig‑zag pattern).

\- The Simple (Keyword) Cipher is case‑insensitive – all letters are converted to uppercase before processing.

\- For very long messages (> 150 transformation steps), the console truncates the display to avoid performance issues (the final result is still correct).

\- Rail Fence encryption includes spaces as characters; therefore the ciphertext may contain spaces in unexpected positions.



\---



\## Academic Integrity Note



This implementation was developed independently for the Information and Cybersecurity assignment. The code is original, with comments explaining each major section. Assistance from ChatGPT (GPT‑5.5) was used only for UI styling references and animation optimisation, as declared in the assignment report.



\---



\## Contact



For any questions regarding this submission, please contact the course instructor via Spark LMS.



\---



\*\*© 2026 Tai Wen Hong – All rights reserved for academic submission purposes.\*\*




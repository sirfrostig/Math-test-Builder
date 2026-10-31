 
Math test builder
Version: v0.1.4 (beta) · a single HTML file, no installation, no server

Math test builder is a browser tool for teachers who want every student to get their own version of the same math test. You write a question once, using blocks that generate random numbers and calculate the answer, and the program gives each student a different, reproducible variant, prints the tests and produces the answer key.

It runs entirely in your browser. Nothing is sent anywhere. Your questions, tests and classes are stored in the browser, and you can also keep them in a folder or export them as a file.

What it does
Question editor with blocks. Build a question from text and code blocks: random numbers, sets of different numbers, decimals and fractions, calculations, variables, fractions and mixed numbers, powers and roots, trigonometry, complex numbers, functions, "biggest/smallest/filter" over sets, if/then/else, algebra (solve), and shuffled answer boxes. Undo and redo with Ctrl+Z / Ctrl+Y.

Random numbers you can control. Exclude numbers or groups of numbers: divisible by, common factor with, primes, squares, cubes, palindromes, whole numbers, a number ending in zero, a given digit, and more. The editor warns you when the exclusions leave too few numbers.

Reproducible variants. Every student has a seed, so a test can be printed again and gives exactly the same numbers. The same question twice on one test never comes out identical.
Parts and points. Split a question into parts a), b), c) ... with E/C/A points per part. Variant groups let several versions of one task be drawn at random.

Images and figures. Add images (PNG, JPG, GIF, WebP, SVG, or paste a screenshot) or draw graphs and geometry figures with code: coordinate systems with grid and subgrid, functions, points, lines, segments, rays, circles, arcs, angles and intersection points. Text boxes on a figure can be rotated and can contain calculations, so the numbers in a figure change with the student. "Not drawn to scale" keeps the values but distorts the drawing slightly, and "scale to fit" fits the window to the points. Position, text wrapping, anchoring to a row of the question, and size are adjustable.

Tests, classes and printing. Combine questions into tests with parts, assign tests to classes, and print one test per student with a name, class, seed, an optional QR code and optional E/C/A points. An optional box for the student's points (with the maximum next to it) and one for the grade can be added to the first page.

Answers. An answer key for every student's test.
Import and export. Import questions from Word (.docx), text, Markdown or CSV, and export or import your questions, tests and classes as JSON.


Getting started

Download math-test-builder-vX.Y.Z.html and open it in Chrome or Edge.

Create questions in the Questions tab, build a test in Tests, add students in Classes, and use Assign and print to print and Answers for the answer key.

Export your data now and then. It lives in the browser's storage, which holds about 5 MB, and images take a lot of room.


Limitations


All data is stored in the browser (about 5 MB) unless you connect a folder. Export regularly.

The interface is in English and the printed tests use Swedish labels (for example "Namn", "Klass", "Poäng").

The program cannot set printer options such as stapling. Every student is sent as a separate print job, so you can set the options in your printer's own settings.
Versions

The file name contains the version, and the full history is in the comment at the top of the HTML file. Versions up to 5.52 (numbered 4.x and 5.x) are the alpha history. The beta history starts at v0.1.x.

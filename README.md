# Subtle Data Corruption with MOVE CORRESPONDING in COBOL

This repository demonstrates a common yet subtle bug in COBOL programs involving the `MOVE CORRESPONDING` statement.  Improperly used, it can lead to data truncation or corruption without immediately obvious error messages.

The `bug.cob` file shows the problematic code.  The `bugSolution.cob` file provides a corrected version with detailed explanations.

**Problem:** The `MOVE CORRESPONDING` statement assumes a one-to-one correspondence in data types and sizes between source and target structures.  Any mismatch can cause silent data corruption.

**Solution:** Always meticulously verify that data structures used with `MOVE CORRESPONDING` are perfectly aligned. Consider using explicit `MOVE` statements for better control and clarity, especially in situations with potentially different field lengths or types.
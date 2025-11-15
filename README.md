Git-Like Version Control System (C++)

This project implements a lightweight Git-style version control system for large CSV datasets using tree structures and Merkle hashing. It is designed for the healthcare dataset included in the repository, but the code can be modified to support any CSV file.

Features

Initialize a repository (init): upload CSV, choose tree type (AVL, B-Tree, Red-Black Tree), select key column, and store each tree node as a separate file.
Commit changes (commit "message"): saves a new version.
Branch management (branch, checkout, delete-branch, branches, current-branch).
View history (log).
Merge branches (merge source target).
Save and load repository state (save, load).
Visualize structure (visualize-tree branch_name).

Tree & File Handling

Supports AVL, B-Tree, and Red-Black Tree. All node additions, deletions, and updates synchronize with the filesystem. Each node is stored independently to avoid loading the full dataset into memory.

Hashing & Data Integrity

Offers Instructor Hash (modulo-29) or SHA-256. A Merkle Tree ensures fast corruption detection and efficient synchronization by transmitting only modified or corrupted nodes.

Dataset

The default dataset (dataset.csv) is a healthcare dataset containing demographics, medical conditions, billing details, and hospital service information. The system is optimized for this dataset but can be adapted for other use cases by adjusting parsing and column selection.

User Interface

Includes a friendly, interactive command-line interface that guides users through all operations and can visualize the underlying tree structure.

Purpose

Demonstrates versioning, branching, hashing, tree storage, and distributed synchronization concepts in a simplified Git-like system suitable for learning and experimentation.


# Handnotes

Handnotes is a TypeScript project for managing hand-written notes digitally. The project aims to provide a simple and effective way to create, store, and manage notes.

## Features

- Add new notes
- Retrieve all notes
- Basic TypeScript setup and project structure

## Getting Started

### Prerequisites

- Node.js
- npm

### Installation

1. Clone the repository:
   \`\`\`sh
   git clone https://github.com/your-username/handnotes.git
   cd handnotes
   \`\`\`

2. Install dependencies:
   \`\`\`sh
   npm install
   \`\`\`

3. Build the project:
   \`\`\`sh
   npx tsc
   \`\`\`

4. Run the project:
   \`\`\`sh
   npx ts-node src/index.ts
   \`\`\`

## Project Structure

\`\`\`
handnotes/
├── src/
│   ├── index.ts
│   ├── models/
│   ├── services/
│   └── utils/
├── dist/
├── node_modules/
├── .gitignore
├── package.json
├── tsconfig.json
└── README.md
\`\`\`

## Create the GitHub Repository

1. **Log in to GitHub** and create a new repository.
2. **Repository Name:** \`handnotes\`
3. **Description:** A TypeScript project for managing hand-written notes digitally.
4. **Initialize with a README:** Yes
5. **Add .gitignore:** Choose \`Node\`
6. **Choose a License:** MIT (or any preferred license)

## Clone the Repository Locally
\`\`\`sh
git clone https://github.com/your-username/handnotes.git
cd handnotes
\`\`\`

## Initialize a TypeScript Project

1. **Initialize npm:**
   \`\`\`sh
   npm init -y
   \`\`\`

2. **Install TypeScript and other dependencies:**
   \`\`\`sh
   npm install typescript ts-node @types/node --save-dev
   \`\`\`

3. **Initialize TypeScript configuration:**
   \`\`\`sh
   npx tsc --init
   \`\`\`

## Project Structure

\`\`\`
handnotes/
├── src/
│   ├── index.ts
│   ├── models/
│   ├── services/
│   └── utils/
├── dist/
├── node_modules/
├── .gitignore
├── package.json
├── tsconfig.json
└── README.md
\`\`\`

## Example Code

**src/index.ts:**
\`\`\`typescript
import { Note } from './models/Note';
import { NoteService } from './services/NoteService';

const main = () => {
  const noteService = new NoteService();
  
  const note1 = new Note('Meeting notes', 'Discuss project updates.');
  noteService.addNote(note1);
  
  console.log('All Notes:', noteService.getAllNotes());
};

main();
\`\`\`

**src/models/Note.ts:**
\`\`\`typescript
export class Note {
  constructor(public title: string, public content: string) {}
}
\`\`\`

**src/services/NoteService.ts:**
\`\`\`typescript
import { Note } from '../models/Note';

export class NoteService {
  private notes: Note[] = [];

  addNote(note: Note): void {
    this.notes.push(note);
  }

  getAllNotes(): Note[] {
    return this.notes;
  }
}
\`\`\`

## Update \`tsconfig.json\`

Ensure the \`outDir\` and \`rootDir\` are set:
\`\`\`json
{
  "compilerOptions": {
    "outDir": "./dist",
    "rootDir": "./src",
    "strict": true
  }
}
\`\`\`

## Update \`.gitignore\`

Make sure the \`dist/\` folder and \`node_modules/\` are ignored:
\`\`\`
node_modules/
dist/
\`\`\`

## Build and Run the Project

1. **Build the project:**
   \`\`\`sh
   npx tsc
   \`\`\`

2. **Run the project using ts-node:**
   \`\`\`sh
   npx ts-node src/index.ts
   \`\`\`

## License

This project is licensed under the MIT License.

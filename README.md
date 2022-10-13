## 🫖 The Tea Round Picker

### Brief

The business has identified the need for a new productivity tool for company-wide use. It
has been established that a large quantity of tea is drunk throughout the working day and
that it’s more efficient for one person to make a round of tea for their team than for each
team member to make their own. Having decided upon this new approach to tea-making, it
was observed that a considerable amount of time is typically spent deciding who should
make the next round of tea.
The required tool, named The Tea Round Picker, should allow a team to fairly (either
randomly or algorithmically) pick a team member who should make tea for anyone else in
their team who choses to participate. Participation is optional, but inclusive in the eventual
result delivered by the tool. If you’re on the list, the next tea-maker could be you.

An example of a user journey might be as simple as:

1. User enters the names of this round’s participants and selects Pick Tea Maker
2. Tool picks one of the round participant names and displays it to the user
   Additional functionality could include logging, data storage, team preference management,
   score tracking or result notifications, AI to ensure fair distribution, integration with an
   external API to leverage delivery from a local café. The choice is yours.

## 🧰 Tools

- Vue 3 in Vite - [VueJs](https://vuejs.org/)
- [TypeScript](https://www.typescriptlang.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [ESLint](https://eslint.org/)

## ✨ What I learned

- The little details that are different to using React... class instead of className / defining props in the script and the template for displaying the information
- State management is pretty cool in VueJs

## Improvements

- I’d have like to have added some additional interaction to make it less boring
- The way in which I have written the code could be reusable (for example making buttons a component so there’s not duplicated code)
- Add validation to the names (no duplications or at least initials)
- Maybe creating a user profile for each person and how they like their tea (kind of like a list of everyone but the person who was picked)

## ⚒️ Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Type-Check, Compile and Minify for Production

```sh
npm run build
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```

## ✍🏻 Author

- GitHub - [@jadetrue](https://github.com/jadetrue/)

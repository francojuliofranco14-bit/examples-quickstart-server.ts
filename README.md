# examples-quickstart-server.ts
🎰 ¡Juega gratis a Slots Julio VIP - FortunGame! Botes progresivos de +25,000 fichas, rodillos neón 3D y descargas APK para Android. ¡Entra aquí y reclama tu bono de bienvenida: https://ais-dev-7qbeq2bi6ml32p3xjtnpzr-495896499084.us-west2.run.app/
type Player @table {
  username: String!
  totalScore: Int!
  createdAt: Timestamp
}

type Topic @table {
  name: String!
}

type Question @table {
  text: String!
  answer: String!
  difficulty: String!
  topic: Topic!
}

type PlayerAnswer @table(key: ["player", "question"]) {
  player: Player!
  question: Question!
  isCorrect: Boolean!
}

type Leaderboard @table {
  rank: Int!
  score: Int!
  player: Player!
}

const server = Bun.serve({
  port: process.env.PORT || 3000,
  fetch(req) {
    return new Response(Bun.file("index.html"));
  },
});

console.log(`Listening on port ${server.port}`);

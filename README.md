# Typescript Labs

## Lab 10: Passing Type Arguments

file: `/src/10-set.problem.ts`

For this exercise, we'll be working with the Set data structure from JavaScript.

Here we're creating a set of guitarists and adding Jimi Hendrix and Eric Clapton to it.

```ts
const guitarists = new Set();

guitarists.add("Jimi Hendrix");
guitarists.add("Eric Clapton");
```

We also have the `// @ts-expect-error` directive because we expect an error to be thrown we try to add a non-string to the set.

```ts
it("Should give a type error when you try to pass a non-string", () => {
  // @ts-expect-error
  guitarists.add(2);
});
```

However, our error isn't being thrown because the guitarists set is not strictly typed as a set of strings.

We see this same issue when hovering over the guitaristsAsArray variable inside of the array test:

```ts
const guitaristsAsArray = Array.from(guitarists);
```

Hovering shows us that guitaristsAsArray is an unknown array.

Challenge
Your challenge is to update guitarists to be typed a set of strings.
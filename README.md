## Bug Report

I wanted to share an issue I've run into while working on a project. I appreciate your time and help.

### Summary

There's two related issues:

1. I have a `collection` with a root `object` "container" and a child that has a `collision-object` and a `sprite`

- **The issue:** When I place it on the `main.collection` and set a position different from zero it will fire off taking that direction. If the position it's `vec3(0, 0, 0)` then nothing happens.

2. I have two objects `foo` and `bar`. `bar` has a `collision-object` and a `sprite`. `foo` has as factory to `bar`

- **The issue:** On code when I create `bar` and set the parent to `.` it will fire off taking that direction

### Record

![Record](./doc/record.mp4)

### Notes

- No velocity was set.
- Disabling the `collision-object` stop it from doing that
- Disabling the `allow_dynamic_transforms` it will fix, but i also notice it disable `euler.z` ;/

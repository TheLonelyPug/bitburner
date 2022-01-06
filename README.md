## Bitburner script
This script automates the hacking process entirely for early game. Make easy bucks quickly.

You can play the game here: [Bitburner](https://danielyxie.github.io/bitburner/) or get it from [Steam](https://store.steampowered.com/app/1812820/Bitburner/)

## Installation

1. Create a new script called `start.ns` by issuing the following command: `nano start.ns`. Make sure you're on your home server if you're not (you can quickly go home by running `home` in the console).
2. Paste the following content:

```javascript
export async function main(ns) {
  if (ns.getHostname() !== "home") {
    throw new Exception("Run the script from home");
  }

  await ns.wget(
    `https://raw.githubusercontent.com/TheLonelyPug/bitburner/main/src/download.ns?ts=${new Date().getTime()}`,
    "download.ns"
  );
  ns.spawn("download.ns", 1);
}
```

3. Exit the nano and write in console: `run start.ns`

4. Watch the magic happen.

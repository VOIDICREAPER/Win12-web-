win12-web/
├─ public/
│   └─ index.html
├─ src/
│   ├─ App.js
│   ├─ index.js
│   └─ components/
│       ├─ Taskbar.js
│       ├─ DesktopIcon.js
│       └─ Window.js
├─ package.json{
  "name": "win12-web",
  "version": "1.0.0",
  "private": true,
  "scripts": {
    "start": "parcel src/index.html --open",
    "build": "parcel build src/index.html --public-url ./"
  },
  "dependencies": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0"
  },
  "devDependencies": {
    "parcel": "^2.9.3"
  }
}import React from "react";

export default function DesktopIcon({ name, action }) {
  return (
    <div
      onClick={action}
      style={{
        width: 100,
        height: 100,
        margin: 10,
        backgroundColor: "#333",
        color: "white",
        display: "inline-flex",
        alignItems: "center",
        justifyContent: "center",
        cursor: "pointer",
        border: "1px solid #0f0"
      }}
    >
      {name}
    </div>
  );
}

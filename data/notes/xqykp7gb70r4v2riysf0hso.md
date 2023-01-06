# Extensions
## Terminals Manager
### ERPNext
**.vscode/terminals.json**
```
{
    "autorun": true,
    "autokill": true,
    "terminals": [
        {
            "name": "Git",
            "description": "For running git commands",
            "open": true,
            "focus": true,
            "commands": [
                "cd frappe-bench/apps/CUSTOM_APP"
            ]
        },
        {
            "name": "Bench",
            "description": "Running Bench commands",
            "open": true,
            "focus": false,
            "commands": [
                "cd frappe-bench"
            ]
        },
        {
            "name": "Bench Console",
            "description": "For running python commands",
            "open": true,
            "focus": false,
            "commands": [
                "cd frappe-bench",
                "bench console"
            ]
        }
    ]
}
```
# AgentForceLegend

Proyecto Salesforce DX para completar el Trailhead **Agentforce Legend**, usando el org de desarrollo `DEV-AgentLeg1`.

## Org

| Alias           | Username                          | Tipo              |
| --------------- | --------------------------------- | ----------------- |
| `DEV-AgentLeg1` | `jbetas@salesforce.com.agentleg1` | Developer Edition |

```bash
cd AgentForceLegend
sf config set target-org DEV-AgentLeg1
sf org display
sf org open
```

Ejecuta los comandos `sf` desde esta carpeta. El workspace padre (`agentforce-ai-framework`) tiene otro `sfdx-project.json` y otro default org.

## Estructura

```
AgentForceLegend/
├── force-app/main/default/   # metadata (Apex, LWC, agents, flows)
├── manifest/package.xml      # retrieve/deploy estándar
├── specs/                    # agent specs y test specs (Agentforce DX)
├── config/                   # scratch org definition (opcional)
├── scripts/                  # Apex anónimo y SOQL
└── sfdx-project.json         # API 67.0
```

## Comandos frecuentes

```bash
sf project retrieve start -x manifest/package.xml -o DEV-AgentLeg1
sf project deploy start -x manifest/package.xml -o DEV-AgentLeg1
sf project retrieve start --metadata AiAuthoringBundle -o DEV-AgentLeg1
```

## Tooling

- Salesforce CLI (`sf`)
- Salesforce Extension Pack + Agentforce DX (`salesforcedx-vscode-agents`)
- Prettier, ESLint y Jest para LWC (`npm install`)

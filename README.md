# Monster Gaming Examples

Example integrations showing how to use [Monster Gaming](https://monstergaming.ai) with popular game engines and frameworks.

## Quick Start

```bash
# Install the SDK for your language
npm install @monstergaming/sdk   # TypeScript/JavaScript
pip install monstergaming         # Python
cargo add monstergaming           # Rust
```

```typescript
import { MonsterGaming } from '@monstergaming/sdk';

const client = new MonsterGaming({ apiKey: 'mg_your_api_key' });

const response = await client.chat.completions.create({
  model: 'monster-gpt',
  messages: [
    { role: 'system', content: 'Engine: Unreal Engine 5. Language: C++.' },
    { role: 'user', content: 'Create a character controller with double jump and wall run' },
  ],
});
```

## Engine Examples

| Engine | Language | What It Shows |
|--------|----------|---------------|
| Unreal Engine 5 | C++ | Character controllers, gameplay abilities, Slate UI, networking |
| Unity 6 | C# | MonoBehaviour patterns, ECS, shader graphs, object pooling |
| Godot 4 | GDScript | Scene trees, signals, physics, procedural generation |

## How Monster-GPT Works

`monster-gpt` auto-detects your game engine from context and routes to the right specialist agent. We run 145+ agents across 30+ disciplines — shader programming, netcode, animation, level design, QA, VFX, audio, and more.

Set the engine explicitly in the system prompt for best results:

```python
response = client.chat.completions.create(
    model="monster-gpt",
    messages=[
        {"role": "system", "content": "Engine: Godot 4.3. Language: GDScript."},
        {"role": "user", "content": "Procedural dungeon generator with room templates"},
    ],
)
```

## Free Tier

No credit card required. Get started at [monstergaming.ai/pricing](https://monstergaming.ai/pricing).

## Links

- **Quickstart:** [monstergaming.ai/quickstart](https://monstergaming.ai/quickstart)
- **SDKs:** [TypeScript](https://github.com/Monster-Gaming-ai/sdk-js) · [Python](https://github.com/Monster-Gaming-ai/sdk-python) · [Rust](https://github.com/Monster-Gaming-ai/sdk-rust)
- **Blog:** [blog.monstergaming.ai](https://blog.monstergaming.ai)
- **Newsletter:** [Man in the Machine](https://blog.monstergaming.ai/newsletter/)

## License

Apache License 2.0. See [LICENSE](LICENSE).

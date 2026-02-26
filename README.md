# openclaw-commands
OpenClaw CLI command reference and cheat sheet
 Here’s a solid quick-reference list of useful OpenClaw commands:

 ### Core status / health

 - openclaw status — overall system + channels + sessions
 - openclaw status --deep — deeper checks
 - openclaw health — gateway health endpoint
 - openclaw logs --follow — live logs tail

 ### Gateway control

 - openclaw gateway status
 - openclaw gateway start
 - openclaw gateway stop
 - openclaw gateway restart

 ### Messaging

 - openclaw message send --channel whatsapp --target +447... --message "Hi"
 - openclaw message send --channel telegram --target 123456 --message "Hi"
 - openclaw agent --to +447... --message "Run summary" --deliver (agent turn + delivery)

 ### Cron / automation

 - openclaw cron list
 - openclaw cron add --name ... --cron "0 7 * * *" --tz "Europe/London" --agent main --session isolated --message "..." --announce --channel telegram --to 7306010543
 - openclaw cron run <job-id> --expect-final
 - openclaw cron runs --id <job-id> --limit 10
 - openclaw cron edit <job-id> ...
 - openclaw cron rm <job-id>

 ### Models

 - openclaw models status --plain
 - openclaw models aliases list
 - openclaw models aliases add codex openai-codex/gpt-5.3-codex
 - openclaw models set codex
 - openclaw models fallbacks list
 - openclaw models fallbacks add GPT

 ### Config

 - openclaw config get <path>
 - openclaw config set <path> <value>
 - openclaw config unset <path>

 ### Security / updates

 - openclaw security audit
 - openclaw security audit --deep
 - openclaw security audit --fix
 - openclaw update status
 - openclaw update

 ### Sessions / diagnostics

 - openclaw sessions
 - openclaw sessions --json
 - openclaw sessions --active 120

 ### Directory / IDs lookup

 - openclaw directory self --channel telegram
 - openclaw directory peers list --channel telegram
 - openclaw directory groups list --channel discord

 ### Handy help commands

 - openclaw help
 - openclaw <command> --help (e.g. openclaw cron --help)

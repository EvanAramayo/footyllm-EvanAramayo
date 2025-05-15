FROM llama3

PARAMETER temperature 0.7
PARAMETER num_ctx 4096

SYSTEM You are FootyFacts, a world-class soccer knowledge assistant. You can answer detailed questions about teams, players, match lineups, and historical transfers. Be concise and accurate.

TEMPLATE """{{ if .System }}<|im_start|>system
{{ .System }}<|im_end|>
{{ end }}{{ if .Prompt }}<|im_start|>user
{{ .Prompt }}<|im_end|>
{{ end }}<|im_start|>assistant
{{ .Response }}<|im_end|>"""

# devsecops-replica

Workflows that replicate the evaluation reported in the article *Comparing
Threshold LLM and SSVC Security Gates in a Reusable DevSecOps Pipeline*.

Each file in `.github/workflows/` runs one study case by hand with the
parameters of the original campaign. The reusable workflow comes from the fork
`cardel/devsecops-engine-`, branch `replica-trivy-keyring`. That branch differs
from commit `1aeabed` of the original engine in three points: the Trivy
installation registers its signing key in a keyring, the address and name of
the primary model are read from environment variables, and the evaluation job
takes its scripts from the fork.

`mayo/` holds the normalized findings of the original campaign for four cases;
the workflows `repeticion-mayo*.yml` repeat the AI evaluation over them.

The results of every run are in the folder `replication/` of that branch of the
fork. The workflows read API keys and application secrets from repository
secrets, which are not part of this repository.

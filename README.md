# cicd-pipeline-python-cd

Calculadora web en Flask con pipeline de CI/CD que despliega en AWS ECS (Staging y Producción) con Terraform (Entregable 3 – Integración y Entrega Continua, EAFIT).

## Integrantes

1. Santiago Alvarez — usuario de GitHub: `pendiente`
2. Emmanuel Correa — usuario de GitHub: `imKorr` (propietario del repositorio)
3. Tomás Echavarria — usuario de GitHub: `pendiente`
4. José David Toro — usuario de GitHub: `pendiente`

## Dependencias bloqueadas

`requirements.txt` y `requirements-dev.txt` declaran las dependencias directas. El `Dockerfile` y el pipeline instalan desde `requirements.lock` y `requirements-dev.lock`, que fijan todas las dependencias (incluidas las transitivas) con versión exacta y hash, y se instalan con `--require-hashes --only-binary :all:`. Si cambias un `requirements*.txt`, regenera los archivos de bloqueo:

```bash
uv pip compile requirements.txt --universal --python-version 3.13 --generate-hashes -o requirements.lock
uv pip compile requirements-dev.txt --universal --python-version 3.13 --generate-hashes -o requirements-dev.lock
```

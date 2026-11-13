# Deploy (Dokploy)

O deploy é feito pelo próprio Dokploy, com provider GitHub: repositório `reforma-facil`, branch `main`, Build Type Dockerfile (o `Dockerfile` da raiz), deploy automático a cada push. Porta do app: 3000.

Não há workflow de deploy nem imagem publicada no GHCR; o workflow de CI fica para uma entrega futura.

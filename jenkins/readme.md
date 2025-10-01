# หา GID ของกลุ่ม docker บนโฮสต์

DOCKER_GID=$(getent group docker | cut -d: -f3)

cat > .env <<EOF
DOCKER_GID=${DOCKER_GID}
EOF
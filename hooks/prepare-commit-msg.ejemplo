#!/bin/sh

#Recuerda hacer
# cp prepare-commit-msg.ejemplo prepare-commit-msg
# chmod +x prepare-commit-msg

SOB=$(git config github.user)
grep -qs "^$SOB" "$1" || echo ". Cambio por @$SOB" >> "$1"

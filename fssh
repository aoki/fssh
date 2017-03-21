# fssh is filterd ssh
function fssh() {
  local DESTINATION=$(eval ${FSSH_LS_INSTANCE:="els --no-header"} | grep ${GREP_WORD:=dev} | ${FSSH_FILTER:=fzf} | tr -s ' ' | cut -d' ' -f 8)
  \ssh -oLogLevel=QUIET -oProxyCommand="ssh -W %h:%p ${BASTION:=} -oLogLevel=QUIET" -oStrictHostKeyChecking=no -oUserKnownHostsFile=/dev/null ${DESTINATION}
}

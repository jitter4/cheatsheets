#### PodIP
kubectl describe pods -n dep-ns-inst-gnryooaxblheuuwjwszspfef -l <key>-<value> | grep -F IP: | grep -E '[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}' -m 1 | sed 's/^.*:           //'
cockroachdb
==================================================

# NAME

  cockroachdb

# SYNOPSIS

  kpt get https://github.com/pwittrock/examples/staging/cockroachdb@v1.0 ./cockroachdb

# Description

  The *cockroachdb* package runs an instance of cockroachdb as a StatefulSet.

  Default ports:

    http: 26257
    grpc: 8080


# Examples

  apply the package to a cluster

	kubectl apply -f cockroachdb/ --recursive

  set the replicas

	kpt cockroachdb/ set replicas cockroachdb --value 5

  set the cpu.limits

	kpt cockroachdb/ set cpu-limits cockroachdb --value 500m

  set the cpu.requests

	kpt cockroachdb/ set cpu-requests cockroachdb --value 500m

## etcd-disco

Create etcd cluster

### Synopsis

Create etcd cluster

```
etcd-disco [flags]
```

### Examples

```
etcd-disco cluster create <name>
```

### Options

```
      --advertise-client-urls URLs                   List of this member's client URLs to advertise to the public. (default http://localhost:2379)
      --alsologtostderr                              log to standard error as well as files
      --auth-token string                            Specify auth token specific options. (default "simple")
      --auto-compaction-mode string                  interpret 'auto-compaction-retention' one of: periodic|revision. 'periodic' for duration based retention, defaulting to hours if no time unit is provided (e.g. '5m'). 'revision' for revision number based retention. (default "periodic")
      --auto-compaction-retention string             Auto compaction retention for mvcc key value store. 0 means disable auto compaction.
      --auto-disaster-recovery                       Defines whether the operator will attempt to seed a new cluster from a snapshot after the managed cluster has lost quorum (default true)
      --auto-tls                                     Client TLS using generated certificates
      --ca-file string                               DEPRECATED: Path to the client server TLS CA file.
      --cert-file string                             Path to the client server TLS cert file.
      --check-interval duration                      The interval between each cluster verification by the operator. (default 30m0s)
      --client-cert-auth                             Enable client cert authentication.
      --client-crl-file string                       Path to the client certificate revocation list file.
      --cluster-active-size IgnoredFlag[=true]       
      --cluster-remove-delay IgnoredFlag[=true]      
      --cluster-sync-interval IgnoredFlag[=true]     
      --config IgnoredFlag[=true]                    
      --config-file string                           Path to the server configuration file
      --cors CORSInfo                                Comma-separated white list of origins for CORS (cross-origin resource sharing).
      --data-dir string                              Path to the data directory.
      --debug                                        Enable debug-level logging for etcd.
      --discovery string                             Discovery URL used to bootstrap the cluster.
      --discovery-fallback StringsFlag               Valid values include proxy, exit (default proxy)
      --discovery-proxy string                       HTTP proxy to use for traffic to discovery service.
      --discovery-srv string                         DNS domain used to bootstrap initial cluster.
      --election-timeout uint                        Time (in milliseconds) for an election to timeout. (default 1000)
      --enable-pprof                                 Enable runtime profiling data via HTTP server. Address is at client URL + "/debug/pprof/"
      --enable-v2                                    Accept etcd V2 client requests. (default true)
      --experimental-corrupt-check-time duration     Duration of time between cluster corruption check passes. (default 0s)
      --experimental-enable-v2v3 string              v3 prefix for serving emulated v2 state.
      --experimental-initial-corrupt-check           Enable to check data corruption before serving any client/peer traffic.
      --force IgnoredFlag[=true]                     
      --force-new-cluster                            Force to create a new one member cluster.
      --grpc-keepalive-interval duration             Frequency duration of server-to-client ping to check if a connection is alive (0 to disable). (default 2h0m0s)
      --grpc-keepalive-min-time duration             Minimum interval duration that a client should wait before pinging server. (default 5s)
      --grpc-keepalive-timeout duration              Additional duration of wait before closing a non-responsive connection (0 to disable). (default 20s)
      --heartbeat-interval uint                      Time (in milliseconds) of a heartbeat interval. (default 100)
  -h, --help                                         help for etcd-disco
      --initial-advertise-peer-urls URLs             List of this member's peer URLs to advertise to the rest of the cluster. (default http://localhost:2380)
      --initial-cluster string                       Initial cluster configuration for bootstrapping. (default "default=http://localhost:2380")
      --initial-cluster-state StringsFlag            Initial cluster state ('new' or 'existing'). (default new)
      --initial-cluster-token string                 Initial cluster token for the etcd cluster during bootstrap. (default "etcd-cluster")
      --key-file string                              Path to the client server TLS key file.
      --listen-client-urls URLs                      List of URLs to listen on for client traffic. (default http://localhost:2379)
      --listen-metrics-urls string                   List of URLs to listen on for metrics.
      --listen-peer-urls URLs                        List of URLs to listen on for peer traffic. (default http://localhost:2380)
      --log-output string                            Specify 'stdout' or 'stderr' to skip journald logging even when running under systemd. (default "default")
      --log-package-levels string                    Specify a particular log level for each etcd package (eg: 'etcdmain=CRITICAL,etcdserver=DEBUG').
      --log_backtrace_at traceLocation               when logging hits line file:N, emit a stack trace (default :0)
      --log_dir string                               If non-empty, write log files in this directory
      --logtostderr                                  log to standard error instead of files
      --max-request-bytes uint                       Maximum client request size in bytes the server will accept. (default 1572864)
      --max-result-buffer IgnoredFlag[=true]         
      --max-retry-attempts IgnoredFlag[=true]        
      --max-snapshots uint                           Maximum number of snapshot files to retain (0 is unlimited). (default 5)
      --max-txn-ops uint                             Maximum number of operations permitted in a transaction. (default 128)
      --max-wals uint                                Maximum number of wal files to retain (0 is unlimited). (default 5)
      --metrics string                               Set level of detail for exported metrics, specify 'extensive' to include histogram metrics (default "basic")
      --name string                                  Human-readable name for this member. (default "default")
      --peer-auto-tls                                Peer TLS using generated certificates
      --peer-ca-file string                          DEPRECATED: Path to the peer server TLS CA file.
      --peer-cert-allowed-cn string                  Allowed CN for inter peer authentication.
      --peer-cert-file string                        Path to the peer server TLS cert file.
      --peer-client-cert-auth                        Enable peer client cert authentication.
      --peer-crl-file string                         Path to the peer certificate revocation list file.
      --peer-election-timeout IgnoredFlag[=true]     
      --peer-heartbeat-interval IgnoredFlag[=true]   
      --peer-key-file string                         Path to the peer server TLS key file.
      --peer-trusted-ca-file string                  Path to the peer server TLS trusted CA file.
      --proxy StringsFlag                            Valid values include off, readonly, on (default off)
      --proxy-dial-timeout uint                      Time (in milliseconds) for a dial to timeout. (default 1000)
      --proxy-failure-wait uint                      Time (in milliseconds) an endpoint will be held in a failed state. (default 5000)
      --proxy-read-timeout uint                      Time (in milliseconds) for a read to timeout.
      --proxy-refresh-interval uint                  Time (in milliseconds) of the endpoints refresh interval. (default 30000)
      --proxy-write-timeout uint                     Time (in milliseconds) for a write to timeout. (default 5000)
      --quota-backend-bytes int                      Raise alarms when backend size exceeds the given quota. 0 means use the default quota.
      --retry-interval IgnoredFlag[=true]            
      --server-address stringArray                   List of URLs to listen on for peer traffic. (required for join)
      --snapshot IgnoredFlag[=true]                  
      --snapshot-count uint                          Number of committed transactions to trigger a snapshot to disk. (default 100000)
      --stderrthreshold severity                     logs at or above this threshold go to stderr (default 2)
      --strict-reconfig-check                        Reject reconfiguration requests that would cause quorum loss. (default true)
      --test.coverprofile IgnoredFlag[=true]         
      --test.outputdir IgnoredFlag[=true]            
      --trusted-ca-file string                       Path to the client server TLS trusted CA cert file.
      --unhealthy-member-ttl duration                The time after which, an unhealthy member will be removed from the cluster. (default 2m0s)
  -v, --v IgnoredFlag[=true]                         
      --version                                      Print the version and exit.
      --vmodule moduleSpec                           comma-separated list of pattern=N settings for file-filtered logging
      --vv IgnoredFlag[=true]                        
      --wal-dir string                               Path to the dedicated wal directory.
```


### Reading Material

A collection of resources that I found interesting and useful across various domains.

> [The Tao of Programming](http://www.mit.edu/~xela/tao.html)

> [Rob Pike's 5 Rules of Programming](http://users.ece.utexas.edu/~adnan/pike.html)

## Contents

- [Go](#go)
    - [Pilot Run](#go-pilot-run)
    - [Concepts](#concepts)
        - [Concurrency](#concurrency)
        - [Profiling](#profiling-mag)
    - [Go Internals](#go-internals)
        - [Scheduler](#scheduler)
        - [Garbage Collector](#garbage-collector)
        - [Compiler](#compiler)
        - [Memory](#memory)
    - [Networking with Go](#networking-with-go)
    - [Papers](#go-papers)
- [Containers](#containers)
    - [Docker](#docker)
    - [Kubernetes](#kubernetes-construction)
- [Data Structures and Algorithms](#data-structures-and-algorithms)
    - [Algorithms](#algorithms)
    - [Data Structures](#data-structures)
        - [Advanced Data Structures](#advanced-data-structures)
            - [Bloom filter](#bloom-filter)
- [Internet](#internet)
    - [Webservers](#webservers)
    - [Protocols](#protocols)
        - [HTTP(S)](#https)
            - [HTTP/2](#http2)
            - [HTTP/3](#http3)
        - [TCP/UDP](#tcpudp)
        - [DNS](#dns)
        - [BGP](#bgp)
        - [Websockets](#websockets)
        - [WebRTC](#webrtc)
    - [Load Balancing](#load-balancing)
    - [Books](#networking-books-books)
- [Git](#git)
- [Linux](#linux)
    - [Linux](#linux)
    - [SSH](#ssh)
    - [Linux Security](#linuxsecurity)
    - [Bash](#bash)
    - [Books](#linux-books)
- [OS Dev](#os-dev)
- [C](#c)
- [Ruby](#ruby)
- [Rails](#rails)
- [Haskell](#haskell)
- [Javascript](#js)
    - [Pilot Run](#pilot-run)
    - [Advanced Concepts](#advanced-concepts)
    - [React, Redux](#react-redux)
    - [v8](#v8)
    - [Books](#js-books)
- [Rust](#rust)
- [Database](#database)
- [Tor](#tor)
- [Functional Programming](#functional-programming)
- [OAuth](#oauth)
- [Regex](#regex)
- [Distributed Systems](#distributed-systems)
- [Kafka](#kafka)
- [Spark](#spark)
- [Monitoring](#monitoring)
- [System Design](#system-design)
    - [Guides](#guides)
    - [Systems](#systems)
    - [Scalability](#scalability)
    - [Event driven Architecture](#event-driven-architecture)
    - [AWS](#aws)
    - [Netflix](#netflix)
- [Privacy](#privacy)
- [Security](#security)
    - [Tools](#tools)
    - [Attacks](#attacks)
    - [Guides](#guides)
    - [Games and CTF's](#games-and-ctfs)
    - [Crypto](#crypto)
    - [Papers](#security-papers)
- [x vs y :hocho:](#x-vs-y-hocho)
- [Useful Command Line Tools](#useful-command-line-tools)
- [Blogs](#blogs)
- [More](#more)
- [Fun](#fun)
- [More Books](#more-books)
    - [Software Development](#software-development)
    - [Lisp](#lisp)
    - [Random](#random)
- [Courses](#courses)
- [Papers](#papers)
- [Notes](/Notes) [WIP]

## Legend

You might see some emojis (:sparkles:, :construction: etc) crawling all over this collection.

| emoji  |  meaning |
| ------------ | ------------ |
| :sparkles:  | More the number, the more I liked the blog :3 |
| :zap:  | super duper awesome blog |
| :construction:  | Pending learning on this :( |
| :tv:  | It's video! |
| :books:  | It's a book! |
| :page_with_curl:  | It's a white paper! |
| :wrench:  | It's Debugging related |
| :hocho:  | faceoff |
| :file_folder: | It's a list |

## Go

> [Go FAQ](https://golang.org/doc/faq)

### Go Pilot run

- [Tour of Go](https://tour.golang.org/)
- [Go by example](https://gobyexample.com/)
- [Effective Go](https://golang.org/doc/effective_go.html)
- [Golang channels tutorial](http://guzalexander.com/2013/12/06/golang-channels-tutorial.html)
- [Resources for new Go programmers](https://dave.cheney.net/resources-for-new-go-programmers)
- [The zero value](https://golang.org/ref/spec#The_zero_value)
- [Darker Corners of Go](https://rytisbiel.com/2021/03/06/darker-corners-of-go/) :sparkles:
- [Know Your Nil](http://jeremymikkola.com/posts/2017_03_29_know_your_nil.html)

### Concepts

> Do not communicate by sharing memory; instead, share memory by communicating.

#### Concurrency

> Concurrency is not Parallelism

- [Go Concurrency from the Ground Up](http://www.doxsey.net/blog/go-concurrency-from-the-ground-up)
- [How Goroutines Work](http://blog.nindalf.com/how-goroutines-work/) :sparkles:
- [Concurrency is not Parallelism](https://talks.golang.org/2012/waza.slide) :sparkles: :zap:
- [Concurrency in golang and a mini Load-balancer](https://gist.github.com/rushilgupta/228dfdf379121cb9426d5e90d34c5b96)
- [Channels in Go](https://go101.org/article/channel.html)
- [Go Concurrency Patterns](https://talks.golang.org/2012/concurrency.slide#33)
- [Concurrent programming, with examples](https://begriffs.com/posts/2020-03-23-concurrent-programming.html?hn=1)
- [Slow down your code with goroutines](https://appliedgo.net/concurrencyslower/)
- [How to Gracefully Close Channels](https://go101.org/article/channel-closing.html) :sparkles:
- [Go channels on steroids](https://docs.google.com/document/d/1yIAYmbvL3JxOKOjuCyon7JhW4cSv1wy5hC0ApeGMV9s/pub)
- [Visualizing Concurrency in Go](http://divan.github.io/posts/go_concurrency_visualize/)
- [Go’s Extended Concurrency: Semaphores (Part 1)](https://medium.com/@deckarep/gos-extended-concurrency-semaphores-part-1-5eeabfa351ce)
- [Channel Axioms](https://dave.cheney.net/2014/03/19/channel-axioms) :sparkles:
- [Go Concurrency Patterns: Pipelines and cancellation](https://blog.golang.org/pipelines)
- [Using contexts to avoid leaking goroutines](https://rakyll.org/leakingctx/)
- [Why is a Goroutine’s stack infinite ?](https://dave.cheney.net/2013/06/02/why-is-a-goroutines-stack-infinite)
- [Advanced Go Concurrency Patterns](https://talks.golang.org/2013/advconc.slide#1)
- [sync.RWMutex](https://medium.com/golangspec/sync-rwmutex-ca6c6c3208a0)

#### Profiling :mag:

> [Go Diagnostics](https://golang.org/doc/diagnostics.html) :wrench:

- [Profiling Go](http://www.integralist.co.uk/posts/profiling-go/)
- [Profiling and optimizing Go web applications](https://artem.krylysov.com/blog/2017/03/13/profiling-and-optimizing-go-web-applications/)
- [Profiling Go Programs](https://blog.golang.org/profiling-go-programs)
- [pprof](https://jvns.ca/blog/2017/09/24/profiling-go-with-pprof/)
- [go tool trace](https://making.pusher.com/go-tool-trace/)
- [Various go profiling methods](https://github.com/DataDog/go-profiler-notes/)
- [pprof++: A Go Profiler with Hardware Performance Monitoring](https://eng.uber.com/pprof-go-profiler/)

### Go Internals

> [Everything about Go: internals, concurrency, compiler, or packages available in the Go community.](https://medium.com/a-journey-with-go)

- [Go Internals](https://github.com/teh-cmc/go-internals)
- [How does the go build command work?](https://dave.cheney.net/2013/10/15/how-does-the-go-build-command-work)
- [Introducing the Go Race Detector](https://blog.golang.org/race-detector)
- String interning in Go
    - [String interning in Go](https://artem.krylysov.com/blog/2018/12/12/string-interning-in-go/)
    - [Interning strings in Go](https://commaok.xyz/post/intern-strings/)
- [Arrays, slices (and strings): The mechanics of 'append'](https://blog.golang.org/slices)
- [Go’s hidden #pragmas](https://dave.cheney.net/2018/01/08/gos-hidden-pragmas)
- [Detecting Race Conditions With Go](https://www.ardanlabs.com/blog/2013/09/detecting-race-conditions-with-go.html)

#### Scheduler

- [The Go scheduler](https://morsmachine.dk/go-scheduler) :sparkles:
- [Scheduler Tracing In Go](https://www.ardanlabs.com/blog/2015/02/scheduler-tracing-in-go.html)
- [Analysis of the Go runtime scheduler](http://www.cs.columbia.edu/~aho/cs6998/reports/12-12-11_DeshpandeSponslerWeiss_GO.pdf) :page_with_curl:
- [Go's work-stealing scheduler](https://rakyll.org/scheduler/)

#### Garbage Collector

- [Golang’s Real-time GC in Theory and Practice](https://making.pusher.com/golangs-real-time-gc-in-theory-and-practice/) :sparkles:
- [Getting to Go: The Journey of Go's Garbage Collector](https://blog.golang.org/ismmkeynote)
- [runtime: Large maps cause significant GC pauses](https://github.com/golang/go/issues/9477)
- [How We Saved 70K Cores Across 30 Mission-Critical Services (Large-Scale, Semi-Automated Go GC Tuning @Uber)](https://eng.uber.com/how-we-saved-70k-cores-across-30-mission-critical-services/)

#### Compiler

- [Go compiler internals](https://eli.thegreenplace.net/2019/go-compiler-internals-adding-a-new-statement-to-go-part-1/)
- [Go & Assembly](http://www.doxsey.net/blog/go-and-assembly)
- [Dissecting Go Binaries](https://www.grant.pizza/dissecting-go-binaries/)

#### Memory

- [The Go Memory Model](https://golang.org/ref/mem) :sparkles:
- [Go memory ballast: How I learnt to stop worrying and love the heap](https://blog.twitch.tv/en/2019/04/10/go-memory-ballast-how-i-learnt-to-stop-worrying-and-love-the-heap-26c2462549a2/)
- [Memory Leaking Scenarios](https://go101.org/article/memory-leaking.html)
- [Memory Order Guarantees in Go](https://go101.org/article/memory-model.html)
- [GO MEMORY MANAGEMENT](https://povilasv.me/go-memory-management/)
- [Contiguous stacks in Go](https://agis.io/post/contiguous-stacks-golang/)
- [Memory Optimizations for Go Systems](https://medium.com/swlh/memory-optimizations-for-go-systems-48d95cf64a13)
- [A few bytes here, a few there, pretty soon you’re talking real memory](https://dave.cheney.net/2021/01/05/a-few-bytes-here-a-few-there-pretty-soon-youre-talking-real-memory) :construction:
- [Golang escape analysis](http://www.agardner.me/golang/garbage/collection/gc/escape/analysis/2015/10/18/go-escape-analysis.html) :construction:
- [Are large slices more expensive than smaller ones?](https://dave.cheney.net/2020/03/01/are-large-slices-more-expensive-than-smaller-ones) :mag:
- [There is no pass-by-reference in Go](https://dave.cheney.net/2017/04/29/there-is-no-pass-by-reference-in-go)
- [Allocation efficiency in high-performance Go services](https://segment.com/blog/allocation-efficiency-in-high-performance-go-services/)

### Networking with Go

- [Network Programming with Go](http://tumregels.github.io/Network-Programming-with-Go/)
- [A Million WebSockets and Go](https://medium.freecodecamp.org/million-websockets-and-go-cc58418460bb)
- [TCP/IP Networking in Go](https://appliedgo.net/networking/)
- [An Implementation and Analysis of a Kernel Network Stack in Go with the CSP Style](https://arxiv.org/abs/1603.05636) :page_with_curl:
- [Gotchas in the Go Network Packages Defaults](https://martin.baillie.id/wrote/gotchas-in-the-go-network-packages-defaults/) :sparkles:

### More

- [Interfaces in Go](http://jordanorelli.com/post/32665860244/how-to-use-interfaces-in-go)
- [Go Data Structures: Interfaces](https://research.swtch.com/interfaces)
- [Applied Go](https://appliedgo.net/)
- [Golang Has Generics](http://blog.jonathanoliver.com/golang-has-generics/)
- [Go-tcha: When nil != nil](https://dev.to/pauljlucas/go-tcha-when-nil--nil-hic)
- [SOLID Go Design](https://dave.cheney.net/2016/08/20/solid-go-design)
- [Simple techniques to optimise Go programs](https://stephen.sh/posts/quick-go-performance-improvements)
- [A whirlwind tour of Go’s runtime environment variables](https://dave.cheney.net/tag/godebug)
- [How we optimized our DNS server using go tools](https://medium.com/@arash.cordi/how-we-optimized-our-dns-server-using-go-tools-d753e1a5e709) :sparkles:
- [Optimizing M3: How Uber Halved Our Metrics Ingestion Latency by (Briefly) Forking the Go Compiler](https://eng.uber.com/optimizing-m3/) :sparkles:
- [Writing a very fast cache service with millions of entries in Go](https://allegro.tech/2016/03/writing-fast-cache-service-in-go.html)
- [Go, without package scoped variables](https://dave.cheney.net/2017/06/11/go-without-package-scoped-variables)
- [How to generate a random string of a fixed length in Go?](https://stackoverflow.com/a/31832326)
- [Building efficient statsd library in Go](https://talks.godoc.org/github.com/smira/gopherconru2018/go-statsd.slide#1)
- [Gopher Puzzlers](https://talks.godoc.org/github.com/davecheney/presentations/gopher-puzzlers.slide#1) :zap:
- [Visually Understanding Worker Pool](https://medium.com/coinmonks/visually-understanding-worker-pool-48a83b7fc1f5)
- [The Case For A Go Worker Pool](https://brandur.org/go-whttps://www.ardanlabs.com/blog/2015/02/scheduler-tracing-in-go.htmlorker-pool)
- [Go at Google: Language Design in the Service of Software Engineering](https://talks.golang.org/2012/splash.article)
- [Life of an HTTP request in a Go server](https://eli.thegreenplace.net/2021/life-of-an-http-request-in-a-go-server/)
- [Send data from file without loading into memory](https://stackoverflow.com/questions/42261421/send-os-stdin-via-http-post-without-loading-file-into-memory)
- [Data Race Patterns in Go](https://eng.uber.com/data-race-patterns-in-go/)

## Containers

- [A Practical Introduction to Container Terminology](https://developers.redhat.com/blog/2018/02/22/container-terminology-practical-introduction/) :zap:
- [Container networking is simple](https://iximiuz.com/en/posts/container-networking-is-simple/) :construction:
- [Introduction to Container Security](https://www.docker.com/sites/default/files/WP_IntrotoContainerSecurity_08.19.2016.pdf) :page_with_curl:
- [Linux Containers in 500 lines](https://blog.lizzie.io/linux-containers-in-500-loc.html)
- [Container security best practices: Comprehensive guide](https://sysdig.com/blog/container-security-best-practices/)
- [Three bugs in the Go MySQL Driver](https://github.blog/2020-05-20-three-bugs-in-the-go-mysql-driver/) :zap:

### Docker

- [Docker Internals](http://docker-saigon.github.io/post/Docker-Internals/)
- [Understanding Docker Internals](https://medium.com/@nagarwal/understanding-the-docker-internals-7ccb052ce9fe)
- [Docker Secure Deployment](https://github.com/GDSSecurity/Docker-Secure-Deployment-Guidelines)
- [Docker Curriculum](https://prakhar.me/docker-curriculum/)
- [A tiny but valid `init` for containers](https://github.com/krallin/tini)
- [Intro Guide to Dockerfile Best Practices](https://blog.docker.com/2019/07/intro-guide-to-dockerfile-best-practices/)
- [Docker security](https://docs.docker.com/engine/security/)
- [3 simple tricks for smaller Docker images](https://learnk8s.io/blog/smaller-docker-images)
- [Best practices for building containers](https://cloud.google.com/solutions/best-practices-for-building-containers)
- [Reverse Engineering a Docker Image](https://theartofmachinery.com/2021/03/18/reverse_engineering_a_docker_image.html)
- [docker pause](https://docs.docker.com/engine/reference/commandline/pause/)

### Kubernetes :construction:

- [What even is a kubelet?](http://kamalmarhubi.com/blog/2015/08/27/what-even-is-a-kubelet/)
- [Kubernetes from the ground up: the API server](http://kamalmarhubi.com/blog/2015/09/06/kubernetes-from-the-ground-up-the-api-server/)
- [Kubernetes from the ground up: the scheduler](http://kamalmarhubi.com/blog/2015/11/17/kubernetes-from-the-ground-up-the-scheduler/)
- [Kubernetes: Getting Started With a Local Deployment](https://blog.jetstack.io/blog/k8s-getting-started-part2/)
- [Awesome Kubernetes](https://github.com/ramitsurana/awesome-kubernetes)
- [There and Back Again: The Unexpected Journey of a Request](https://sookocheff.com/post/networking/there-and-back-again/)
- [Life of a Packet in Kubernetes — Part 1](https://dramasamy.medium.com/life-of-a-packet-in-kubernetes-part-1-f9bc0909e051)

## Data Structures and Algorithms

### Algorithms

> [Know Thy Complexities!](http://bigocheatsheet.com/#)

- [Complexity of Python Operations](https://www.ics.uci.edu/~pattis/ICS-33/lectures/complexitypython.txt)
- [Heap Algorithm](http://ruslanledesma.com/2016/06/17/why-does-heap-work.html)
- [Linked lists are still hard](https://brennan.io/2017/04/21/linked-lists-are-still-hard/)
- [Understanding Dijkstra's Algorithm](https://aos.github.io/2018/02/24/understanding-dijkstras-algorithm/)
- [How to think in graphs](https://medium.freecodecamp.org/i-dont-understand-graph-theory-1c96572a1401)
- [Ask HN: What's your favorite elegant/beautiful algorithm?](https://news.ycombinator.com/item?id=18236396)
- [Algorithms Behind Modern Storage Systems](https://queue.acm.org/detail.cfm?id=3220266)
- [The Knuth-Morris-Pratt Algorithm in my own words](http://jakeboxer.com/blog/2009/12/13/the-knuth-morris-pratt-algorithm-in-my-own-words/)
- [Why is processing a sorted array faster than processing an unsorted array?](https://stackoverflow.com/questions/11227809/why-is-processing-a-sorted-array-faster-than-processing-an-unsorted-array) :sparkles: :zap:
- [Introduction to Algorithms](https://www.amazon.com/Introduction-Algorithms-3rd-MIT-Press/dp/0262033844) :books:
- [10 Optimizations on Linear Search](https://queue.acm.org/detail.cfm?id=2984631)

### Data Structures

- [Data Structures & Algorithms I Actually Used Working at Tech Companies](https://blog.pragmaticengineer.com/data-structures-and-algorithms-i-actually-used-day-to-day/)

### Advanced Data Structures

#### Bloom filter

- [What are Bloom filters?](https://blog.medium.com/what-are-bloom-filters-1ec2a50c68ff)
- [When Bloom filters don't bloom](https://blog.cloudflare.com/when-bloom-filters-dont-bloom/)

## Internet

> [Latency Numbers](https://gist.github.com/jboner/2841832)

### Webservers

- [Apache vs Nginx: Practical Considerations](https://www.digitalocean.com/community/tutorials/apache-vs-nginx-practical-considerations)
- [The C10K problem](http://www.kegel.com/c10k.html)
- [nginx](http://www.aosabook.org/en/nginx.html)
- [How WebSocket server handles multiple incoming connection requests?](https://stackoverflow.com/questions/28516962/how-websocket-server-handles-multiple-incoming-connection-requests)
- [Inside NGINX: How We Designed for Performance & Scale](https://www.nginx.com/blog/inside-nginx-how-we-designed-for-performance-scale/)
- [Tuning NGINX for Performance](https://www.nginx.com/blog/tuning-nginx/)

### Web Caching

- [Web Cache - Everything you need to know](http://kamranahmed.info/blog/2017/03/14/quick-guide-to-http-caching/)
- [Cache Docs](https://www.mnot.net/cache_docs/)

### Protocols

#### HTTP(S)

- [HTTP](https://www.jmarshall.com/easy/http/)
- [Capturing HTTP Packets](https://medium.com/@cjoudrey/capturing-http-packets-the-hard-way-b9c799bfb6)
- [HTTPS in the real world](https://robertheaton.com/2018/11/28/https-in-the-real-world/)
- [How does HTTPS actually work?](https://robertheaton.com/2014/03/27/how-does-https-actually-work/)
- [Designing Headers for HTTP Compression](https://www.mnot.net/blog/2018/11/27/header_compression)
- [HTTP headers for the responsible developer](https://www.twilio.com/blog/a-http-headers-for-the-responsible-developer)
- [Evolution of HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Evolution_of_HTTP)
- [The First Few Milliseconds of an HTTPS Connection](http://www.moserware.com/2009/06/first-few-milliseconds-of-https.html) :sparkles:
- [The HTTP part 1 - Let's start small](http://dyszkiewicz.me/programming/http/server/kotlin/2018/07/31/http-part1.html)
- [How HTTPS works ...in a comic!](https://howhttps.works/)
- [How HTTPS Works in Layman's Terms - TLS 1.2 and 1.3](https://vinta.ws/code/how-https-works-in-laymans-terms-tls-1-2-and-1-3.html)
- [HTTP Caching](https://roadmap.sh/guides/http-caching)
- [HTTP Security Headers - A Complete Guide](https://nullsweep.com/http-security-headers-a-complete-guide/)

##### HTTP/2

- [Journey to HTTP/2](https://kamranahmed.info/blog/2016/08/13/http-in-depth/) :sparkles:
- [The Evolution of HTTP – HTTP/2 Deep Dive](https://www.ably.io/topic/http2)

##### HTTP/3

- [Comparing HTTP/3 vs. HTTP/2 Performance](https://blog.cloudflare.com/http-3-vs-http-2/)
- [HTTP3](https://blog.cloudflare.com/http-3-from-root-to-tip/)
- [QUIC](https://blog.cloudflare.com/the-road-to-quic/)
- [Employing QUIC Protocol to Optimize Uber’s App Performance](https://eng.uber.com/employing-quic-protocol/)
- [HTTP/3: the past, the present, and the future](https://blog.cloudflare.com/http3-the-past-present-and-future/)
- [HTTP/3 Deep Dive](https://www.ably.io/topic/http3)
- [HTTP/3 explained](https://http3-explained.haxx.se/)

#### TLS

- [How does SSL/TLS work?](https://security.stackexchange.com/questions/20803/how-does-ssl-tls-work)
- [The Illustrated TLS Connection](https://tls.ulfheim.net/)
- [The New Illustrated TLS Connection](https://tls13.ulfheim.net/)
- [What is TLS (Transport Layer Security)?](https://www.cloudflare.com/en-gb/learning/ssl/transport-layer-security-tls/)
- [Even faster connection establishment with QUIC 0-RTT resumption](https://blog.cloudflare.com/even-faster-connection-establishment-with-quic-0-rtt-resumption/)
- [A Detailed Look at RFC 8446 (a.k.a. TLS 1.3)](https://blog.cloudflare.com/rfc-8446-aka-tls-1-3/)

#### TCP/UDP

- [Discussion: UDP in web](https://news.ycombinator.com/item?id=13741155)
- [Let's code a TCP/IP stack](http://www.saminiir.com/lets-code-tcp-ip-stack-5-tcp-retransmission/)
- [When TCP sockets refuse to die](https://idea.popcount.org/2019-09-20-when-tcp-sockets-refuse-to-die/)
- [Messing With Telnet](https://jott.live/markdown/telnet_writeup)
- [How TCP Sockets Work](https://eklitzke.org/how-tcp-sockets-work)
- [How Does TCP Work?](https://sookocheff.com/post/networking/how-does-tcp-work/)
- [Once Again on TCP vs UDP](https://accu.org/index.php/journals/2180)
- [Nagle's algorithm](https://en.wikipedia.org/wiki/Nagle%27s_algorithm)
    - [40 millisecond bug](https://vorner.github.io/2020/11/06/40-ms-bug.html)
    - [TCP Performance problems caused by interaction between Nagle’s Algorithm and Delayed ACK](http://www.stuartcheshire.org/papers/NagleDelayedAck/)
- [What every developer should know about TCP](https://robertovitillo.com/what-every-developer-should-know-about-tcp/)
- [What I learned attempting the TCP Reset attack](https://squidarth.com/article/networking/2020/05/03/tcp-resets.html)

#### DNS

- [DNS in One Picture](https://medium.com/@kamranahmedse/dns-in-one-picture-d7f4783db06a)
- [The Web Developer's Guide to DNS](https://rjzaworski.com/2019/04/the-web-developers-guide-to-dns)
- [The uncertainty of measuring the DNS](https://blog.apnic.net/2018/07/18/the-uncertainty-of-measuring-the-dns/)
- [DNS Encryption Explained](https://blog.cloudflare.com/dns-encryption-explained/)
- [A cartoon intro to DNS over HTTPS](https://hacks.mozilla.org/2018/05/a-cartoon-intro-to-dns-over-https/)
- [Hello and welcome to DNS!](https://github.com/ahupowerdns/hello-dns)
- [How DNS Works](https://howdns.works/ep1/)
- [Beyond DNS over HTTPS: Trustless DNS Privacy](https://alyssa.is/proposing-dns-over-tcp-over-tor/)

#### BGP

- [What Is BGP? | BGP Routing Explained](https://www.cloudflare.com/learning/security/glossary/what-is-bgp/)
- [THE TWO-NAPKIN PROTOCOL](https://computerhistory.org/blog/the-two-napkin-protocol/?key=the-two-napkin-protocol)
- [Playing battleships over BGP](https://blog.benjojo.co.uk/post/bgp-battleships)

#### Websockets

- [WebSockets for fun and profit](https://stackoverflow.blog/2019/12/18/websockets-for-fun-and-profit/)
- [The WebSocket Protocol: RFC 6455](https://tools.ietf.org/html/rfc6455)
- [How WebSockets Work](https://blog.teamtreehouse.com/an-introduction-to-websockets)
- [HTTP and Websockets: Understanding the capabilities of today’s web communication technologies](https://medium.com/platform-engineer/web-api-design-35df8167460)
- [WebSockets - A Conceptual Deep Dive](https://www.ably.io/topic/websockets)
- [How HTML5 Web Sockets Interact With Proxy Servers](https://www.infoq.com/articles/Web-Sockets-Proxy-Servers/)
- [How Do Websockets Work?](https://sookocheff.com/post/networking/how-do-websockets-work/)
- [What are Long-Polling, Websockets, Server-Sent Events (SSE) and Comet?](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)
- [Building realtime apps with Go and WebSockets: client-side considerations](https://www.ably.io/topic/websockets-golang)

#### WebRTC

- [WebRTC for the Curious](https://webrtcforthecurious.com/)

### Load Balancing

- [Load Balancing](https://blog.vivekpanyam.com/scaling-a-web-service-load-balancing/)
- [GLB: GitHub's open source load balancer](https://githubengineering.com/glb-director-open-source-load-balancer/)
- [What Is Load Balancing?](https://www.nginx.com/resources/glossary/load-balancing/)
- [Understanding Nginx HTTP Proxying, Load Balancing, Buffering, and Caching](https://www.digitalocean.com/community/tutorials/understanding-nginx-http-proxying-load-balancing-buffering-and-caching)
- [Introduction to modern network load balancing and proxying](https://blog.envoyproxy.io/introduction-to-modern-network-load-balancing-and-proxying-a57f6ff80236)

### NAT

- [How NAT traversal works](https://tailscale.com/blog/how-nat-traversal-works/)
- [NAT Slipstreaming](https://samy.pl/slipstream/)

### Random

- [The future of the open internet](https://medium.freecodecamp.com/inside-the-invisible-war-for-the-open-internet-dd31a29a3f08)
- [What happens when...](https://github.com/alex/what-happens-when) :sparkles::zap:
- [How Wi-Fi Works](http://www.verizoninternet.com/bookmark/how-wifi-works/)
- [How Does the Internet Work?](https://web.stanford.edu/class/msande91si/www-spr04/readings/week1/InternetWhitepaper.htm) :page_with_curl:
- [The Law of Leaky Abstractions](https://www.joelonsoftware.com/2002/11/11/the-law-of-leaky-abstractions/) :sparkles:
- [How to crawl a quarter billion webpages in 40 hours](http://www.michaelnielsen.org/ddi/how-to-crawl-a-quarter-billion-webpages-in-40-hours/)
- [Setting up your server for IPv6 (nginx)](https://bubblin.io/blog/ipv6-nginx)
- [The world in which IPv6 was a good design](https://apenwarr.ca/log/20170810)
- [The Non-complexity of /etc/nsswitch.conf](https://developers.redhat.com/blog/2018/11/26/etc-nsswitch-conf-non-complexity/) :sparkles:
- [What is Envoy](https://www.envoyproxy.io/docs/envoy/latest/intro/what_is_envoy)
- [High Performance Browser Networking](https://hpbn.co/) :books:
- [HAProxy](http://www.haproxy.org/)
- [Kerberos: The Network Authentication Protocol](https://web.mit.edu/kerberos/)
- [Network Protocols – Programmer's Compendium](https://www.destroyallsoftware.com/compendium/network-protocols?share_key=97d3ba4c24d21147)
- [curl HTTP cheat sheet](https://curl.github.io/curl-cheat-sheet/http-sheet.html)
- [cURL security anti-patterns](https://blog.pan-net.cloud/posts/curl-security-anti-patterns/)
- [Staying out of TTL hell](http://calpaterson.com/ttl-hell.html)
- [Stateful vs Stateless Authentication](https://www.openidentityplatform.org/blog/stateless-vs-stateful-authentication)
- [How to win at CORS](https://jakearchibald.com/2021/cors/)
- [The perils of the “real” client IP](https://adam-p.ca/blog/2022/03/x-forwarded-for/)

### Networking Books :books:

- [The Architecture of Open Source Applications](http://www.aosabook.org/en/index.html)
- [Understanding IP Addressing: Everything You Ever Wanted To Know](http://pages.di.unipi.it/ricci/501302.pdf)
- [Kurose and Ross - Top Down Networking](http://amzn.in/d/3S7Wd4s)
- TCP/IP Illustrated

## Git

- [Making Commit in past](http://stackoverflow.com/questions/3895453/how-do-i-make-a-git-commit-in-the-past)
- [A Successul Git Branching Model](http://nvie.com/posts/a-Successul-git-branching-model/)
- [Oh shit, git!](http://ohshitgit.com/)
- [What’s Wrong With Git? - Git Merge 2017](https://www.youtube.com/watch?v=31XZYMjg93o) :tv:
- [Git Aliases of the Gods!](https://www.youtube.com/watch?v=3IIaOj1Lhb0) :tv:
- [High-level Problems with Git and How to Fix Them](https://gregoryszorc.com/blog/2017/12/11/high-level-problems-with-git-and-how-to-fix-them/)
- [Git from the bottom up](https://jwiegley.github.io/git-from-the-bottom-up/) :books:
- [Commit Often, Perfect Later, Publish Once: Git Best Practices](http://sethrobertson.github.io/GitBestPractices/)
- [Rebase with history -- implementation ideas](http://softwareswirl.blogspot.in/2009/08/rebase-with-history-implementation.html)
- [How bad can it git? Characterizing secret leakage in public GitHub repositories](https://blog.acolyer.org/2019/04/08/how-bad-can-it-git-characterizing-secret-leakage-in-public-github-repositories/)
- [git add --patch and --interactive](https://nuclearsquid.com/writings/git-add/)
- [Pro Git](https://git-scm.com/book/en/v2) :books:
- [How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/)
- [Git Hooks](https://githooks.com/)
- `git rebase --onto`
    - https://twitter.com/mluisbrown/status/1291756770445099009
    - https://git-scm.com/docs/git-rebase
- `git push --force-with-lease`
    - https://git-scm.com/docs/git-push#Documentation/git-push.txt---force-with-leaseltrefnamegtltexpectgt
- [Commits are snapshots, not diffs](https://github.blog/2020-12-17-commits-are-snapshots-not-diffs/)
- http://whatthecommit.com/
- [Think Like (a) Git](http://think-like-a-git.net)
- [The Thing About Git](https://tomayko.com/blog/2008/the-thing-about-git)

### Git Internals

- [Git Internals - Git References](https://git-scm.com/book/en/v2/Git-Internals-Git-References)
- [Git Internals - Packfiles](https://git-scm.com/book/en/v2/Git-Internals-Packfiles)
- [Git gc](https://www.atlassian.com/git/tutorials/git-gc)
- [Git Compression of Blobs and Packfiles](https://gist.github.com/matthewmccullough/2695758)
- [Git Submodules: Adding, Using, Removing, Updating](https://chrisjean.com/git-submodules-adding-using-removing-and-updating/)
- [Understanding git for real by exploring the .git directory](https://www.daolf.com/posts/git-series-part-1/)
- [The Git Parable](https://tom.preston-werner.com/2009/05/19/the-git-parable.html) :sparkles: :zap:
- [Some of git internals](https://yurichev.com/news/20201220_git/)

## Linux

- [Linux Insides](https://0xax.gitbooks.io/linux-insides/content/index.html)
- [chmod Tutorial](http://catcode.com/teachmod/)
- [Orphan vs Zombie vs Daemon Processes](https://www.gmarik.info/blog/2012/orphan-vs-zombie-vs-daemon-processes/)
- [inetd Vs xinetd in linux](http://unixadminschool.com/blog/2011/07/inetd-vs-xinetd-in-linux/)
- [rm -rf remains](https://lambdaops.com/rm-rf-remains/) :sparkles:
- [What happens when you start a process on Linux?](https://jvns.ca/blog/2016/10/04/exec-will-eat-your-brain/)
- [How does the system shutdown of a linux kernel work internally?](https://unix.stackexchange.com/a/122667/)
- [The Definitive Guide to Linux System Calls](https://blog.packagecloud.io/eng/2016/04/05/the-definitive-guide-to-linux-system-calls/) :sparkles:
- [grep your way to freedom](https://anniecherkaev.com/grep-your-way-to-freedom)
- [The real power of Linux executables](https://ownyourbits.com/2018/05/23/the-real-power-of-linux-executables/)
- [x86 Assembly Guide](http://www.cs.virginia.edu/~evans/cs216/guides/x86.html) :sparkles:
- [Linux file descriptors](https://monometric.io/article/file-descriptors-in-2018)
- [UNIX Syscalls](https://john-millikin.com/unix-syscalls)
- [How statically linked programs run on Linux](https://eli.thegreenplace.net/2012/08/13/how-statically-linked-programs-run-on-linux) :sparkles:
- [File Types in Linux](https://linuxconfig.org/identifying-file-types-in-linux)
- [Killing processes that don't want to die](https://lwn.net/Articles/754980/)
- [Threads and fork(): think twice before mixing them](https://www.linuxprogrammingblog.com/threads-and-fork-think-twice-before-using-them)
- [Loading and ptrace'ing a process on Linux](http://system.joekain.com/2015/06/08/debugger.html)
- [Understanding glibc malloc](https://sploitfun.wordpress.com/2015/02/10/understanding-glibc-malloc/)
- [Systemd as tragedy](https://lwn.net/SubscriberLink/777595/a71362cc65b1c271/)
- [Rethinking PID 1](http://0pointer.de/blog/projects/systemd.html)
- [What is Overcommit? And why is it bad?](https://www.etalabs.net/overcommit.html)
- [Your terminal is not a terminal: An Introduction to Streams](https://lucasfcosta.com/2019/04/07/streams-introduction.html)
- [How fast are Unix domain sockets?](https://blog.myhro.info/2017/01/how-fast-are-unix-domain-sockets)
- [The 101 of ELF files on Linux: Understanding and Analysis](https://linux-audit.com/elf-binaries-on-linux-understanding-and-analysis/)
- [Linux namespaces](http://ifeanyi.co/posts/linux-namespaces-part-1/)
- [Why should text files end with a newline?](https://stackoverflow.com/questions/729692/why-should-text-files-end-with-a-newline)
- [What has to happen with Unix virtual memory when you have no swap space](https://utcc.utoronto.ca/~cks/space/blog/unix/NoSwapConsequence)
- [htop explained](https://peteris.rocks/blog/htop/)
- [The Linux Scheduler: a Decade of Wasted Cores](https://blog.acolyer.org/2016/04/26/the-linux-scheduler-a-decade-of-wasted-cores/)
- [Linux Log Files that are Located under /var/log Directory](https://www.thegeekstuff.com/2011/08/linux-var-log-files/)
- [Basic Linux Privilege Escalation](https://blog.g0tmi1k.com/2011/08/basic-linux-privilege-escalation/)
- [“zero copy networking” vs “kernel bypass”?](https://stackoverflow.com/a/18346526)
- [Understanding cgroups](https://www.grant.pizza/blog/understanding-cgroups/)
- [The brokenness of the sendfile() system call](https://blog.phusion.nl/2015/06/04/the-brokenness-of-the-sendfile-system-call/)
- [Understanding Daemons](https://blog.digitalbunker.dev/2020/09/03/understanding-daemons-unix/)
- [Myths Programmers Believe about CPU Caches](https://software.rajivprab.com/2018/04/29/myths-programmers-believe-about-cpu-caches/) :sparkles:
- [Systemd is not Magic Security Dust](https://www.agwa.name/blog/post/systemd_is_not_magic_security_dust) :construction:
- [Pushing the Limits of Kernel Networking](https://rhelblog.redhat.com/2015/09/29/pushing-the-limits-of-kernel-networking/)
- [eBPF](https://filipnikolovski.com/posts/ebpf/) :construction:
- [Process resource limits under the hood](https://ops.tips/blog/proc-pid-limits-under-the-hood/)

### SSH

- [Secure Secure Shell](https://stribika.github.io/2015/01/04/secure-secure-shell.html) :zap:
- [Endlessh: an SSH Tarpit](https://nullprogram.com/blog/2019/03/22/)
- [A visual guide to SSH tunnels](https://robotmoon.com/ssh-tunnels/) :sparkles:
- [A Visual Guide to SSH Tunnels](https://iximiuz.com/en/posts/ssh-tunnels/)

### Linux Security

- [Linux Kernel Exploitation](https://github.com/xairy/linux-kernel-exploitation)
- [Dirty Cow](https://chao-tic.github.io/blog/2017/05/24/dirty-cow)
- [Explaining Dirty COW local root exploit - CVE-2016-5195](https://www.youtube.com/watch?v=kEsshExn7aE) :tv:
- [Linux Firewall Tutorial: IPTables Tables, Chains, Rules Fundamentals](http://www.thegeekstuff.com/2011/01/iptables-fundamentals/)
- [Security Tips for Linux Servers](https://www.tecmint.com/linux-server-hardening-security-tips/)
- [Three kinds of memory leaks](https://blog.nelhage.com/post/three-kinds-of-leaks/)
- [Running Untrusted Programs in Linux](https://stackoverflow.com/questions/4249063/run-an-untrusted-c-program-in-a-sandbox-in-linux-that-prevents-it-from-opening-f)
- [Writing a simple rootkit for linux](https://w3.cs.jmu.edu/kirkpams/550-f12/papers/linux_rootkit.pdf)
- [Do sudo and .profile/.bashrc enable trivial privilege escalation?](https://security.stackexchange.com/questions/187502/do-sudo-and-profile-bashrc-enable-trivial-privilege-escalation)
- [How to break out of a chroot() jail](https://web.archive.org/web/20160127150916/http://www.bpfh.net/simes/computing/chroot-break.html)

### Bash

- [Creating a bash completion script](https://iridakos.com/tutorials/2018/03/01/bash-programmable-completion-tutorial.html)
- [Explain Shell](https://explainshell.com/)
- [Writing a Unix Shell](https://indradhanush.github.io/blog/writing-a-unix-shell-part-1/)
- [Bash Pitfalls](https://mywiki.wooledge.org/BashPitfalls#for_f_in_.24.28ls_.2A.mp3.29)
- [Minimal safe Bash script template](https://betterdev.blog/minimal-safe-bash-script-template/) :zap:
- http://www.bashoneliners.com/ :sparkles: :zap:
- [Illustrated Redirection Tutorial](https://wiki.bash-hackers.org/howto/redirection_tutorial) :zap: :zap:

### BPF

- [BPF: Tracing and More](http://www.brendangregg.com/Slides/LCA2017_BPF_tracing_and_more.pdf)
- [Cloudflare architecture and how BPF eats the world](https://blog.cloudflare.com/cloudflare-architecture-and-how-bpf-eats-the-world/)

## OS dev

- [Operating Systems Lecture Notes](http://people.csail.mit.edu/rinard/osnotes/)
- [Kernel 101 – Let’s write a Kernel](http://arjunsreedharan.org/post/82710718100/kernel-101-lets-write-a-kernel)
- [Kernel development](http://www.osdever.net/bkerndev/Docs/intro.htm)
- [Computer architecture for network engineers](https://github.com/lukego/blog/issues/18)
- [Building a simple Kernel](http://wiki.osdev.org/Bare_Bones)
- [How Does an Intel Processor Boot?](https://binarydebt.wordpress.com/2018/10/06/how-does-an-x86-processor-boot/)
- [implement your own Linux kernel](https://david942j.blogspot.com/2018/10/note-learning-kvm-implement-your-own.html)

### Books

- [Operating Systems: Three Easy Pieces](http://pages.cs.wisc.edu/~remzi/OSTEP/)
- [Rute User's Tutorial and Exposition](https://rlworkman.net/howtos/rute/)
- [The OS Classics](https://www.allthingsdistributed.com/2020/07/the-os-classics.html)

## C

- [Lightweight HTTP Server](http://kukuruku.co/hub/cpp/lightweight-http-server-in-less-than-40-lines-on-libevent-and-c-11)
- [Understanding C by learning assembly](https://www.recurse.com/blog/7-understanding-c-by-learning-assembly) :sparkles::sparkles:
- [Smashing The Stack For Fun And Profit](http://cecs.wright.edu/~pmateti/InternetSecurity/Lectures/BufferOverflow/alephOne.html)
- [GNU Make: A Program for Directing Recompilation](http://web.mit.edu/gnu/doc/html/make_toc.html)
- [ncurses Programming HOWTO](http://www.tldp.org/HOWTO/NCURSES-Programming-HOWTO/)
- [Make your own build system](http://jstimpfle.de/blah/buildsystem/buildsystem.html)
- [Malloc tutorial](https://danluu.com/malloc-tutorial/)
- [Let's Build a Compiler, by Jack Crenshaw](https://compilers.iecc.com/crenshaw/)
- [Back to Basics](https://www.joelonsoftware.com/2001/12/11/back-to-basics/)
- [Tearing apart printf()](http://www.maizure.org/projects/printf/index.html) :sparkles::sparkles:

## Ruby

- [Metaprogramming in Ruby](http://ruby-metaprogramming.rubylearning.com/)
- [Visualizing Your Ruby Heap](http://tenderlovemaking.com/2017/09/27/visualizing-your-ruby-heap.html)
- [7 Deadly Sins of Ruby Metaprogramming](https://www.codeschool.com/blog/2015/04/24/7-deadly-sins-of-ruby-metaprogramming/)
- [Guide to Ruby](http://poignant.guide/book/) :book:
- [Ruby Under a Microscope](http://patshaughnessy.net/ruby-under-a-microscope) :book:

## Rails

- [RoR Tutorial](https://www.railstutorial.org/book/frontmatter) :book:
- [Predicting Test Failures](http://tenderlovemaking.com/2015/02/13/predicting-test-failues.html)
- [XSS and Rails](http://blog.bigbinary.com/2012/05/10/xss-and-rails.html)
- [RailsConf 2014 - All the Little Things by Sandi Metz](https://www.youtube.com/watch?v=8bZh5LMaSmE) :tv:

## Haskell

- [Official Documentation](https://www.haskell.org/documentation)
- [How to learn Haskell](https://github.com/bitemyapp/learnhaskell)
- [Fighting spam with Haskell](https://code.facebook.com/posts/745068642270222/fighting-spam-with-haskell/) :sparkles:
- [Huge list of videos, talks, courses for Haskell programming language](https://github.com/hzlmn/haskell-must-watch)
- [Happy Learn Haskell Tutorial](http://www.happylearnhaskelltutorial.com/)
- [Some Notes About How I Write Haskell](https://blog.infinitenegativeutility.com/2017/12/some-notes-about-how-i-write-haskell)
- [Learn You a Haskell for Great Good!](http://learnyouahaskell.com/chapters)

<details>
<summary>Books</summary>
<p>

- [Open-source Haskell books](http://hn.premii.com/#/article/14392423)
- [Learn You a Haskell](http://learnyouahaskell.com)
- [Real World Haskell](http://book.realworldhaskell.org/read/)
- [Haskell Programming from first principles](http://haskellbook.com/)

</p>
</details>

## JS

### Pilot Run

- [Objects in javascript](https://stackoverflow.com/questions/3691125/objects-in-javascript/3691209#3691209)
- [Two Pillars of Javascript](https://medium.com/javascript-scene/the-two-pillars-of-javascript-ee6f3281e7f3)
- [How are the Event Loop, Callback Queue, and Javascript’s single thread connected?](https://stackoverflow.com/questions/29421781/how-are-the-event-loop-callback-queue-and-javascript-s-single-thread-connected) :sparkles:
- [Philip Roberts: What the heck is the event loop anyway?](https://www.youtube.com/watch?v=8aGhZQkoFbQ) :tv:
- [Types in Javascript](https://jcemer.com/types-in-javascript-what-you-should-care.html)
- [Modern JavaScript Cheatsheet](https://github.com/mbeaudru/modern-js-cheatsheet)
- [Arrow function vs function declaration / expressions: Are they equivalent / exchangeable?](https://stackoverflow.com/a/34361380)

### Advanced Concepts

- [this in JS](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)
- [What is a Promise?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-promise-27fc71e77261)
- [Lazy, composable, and modular JavaScript](https://codewords.recurse.com/issues/four/lazy-composable-and-modular-javascript)
- [Advanced JS](http://htmldog.com/guides/javascript/advanced/)
- [The Dao of Immutability](https://medium.com/javascript-scene/the-dao-of-immutability-9f91a70c88cd)
- [Composing Software](https://medium.com/javascript-scene/composing-software-an-introduction-27b72500d6ea) :sparkles::sparkles:
- [What is the Difference Between Class and Prototypal Inheritance?](https://medium.com/javascript-scene/master-the-javascript-interview-what-s-the-difference-between-class-prototypal-inheritance-e4cd0a7562e9)
- [What is a Closure?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-closure-b2f0d2152b36)
- [Circular dependencies in JavaScript](https://medium.com/content-uneditable/circular-dependencies-in-javascript-a-k-a-coding-is-not-a-rock-paper-scissors-game-9c2a9eccd4bc)
- [Hoisting in Javascript](https://codeburst.io/hoisting-in-javascript-515c987336d3)
- [Async-Await](https://thomashunter.name/presentations/async-await-javascript-v1/)
- [Await and Async Explained with Diagrams and Examples](http://nikgrozev.com/2017/10/01/async-await/)
- [JavaScript engine fundamentals: Shapes and Inline Caches](https://mathiasbynens.be/notes/shapes-ics) :sparkles:
- [Javascript : The Curious Case of Null >= 0](https://blog.campvanilla.com/javascript-the-curious-case-of-null-0-7b131644e274)
- [How to Fix the ES6 `class` keyword](https://medium.com/javascript-scene/how-to-fix-the-es6-class-keyword-2d42bb3f4caf#.mcpw9sl95)
- [Elements of JavaScript Style](https://medium.com/javascript-scene/elements-of-javascript-style-caa8821cb99f)
- [Javascript Debugging](https://developer.chrome.com/devtools/docs/javascript-debugging)
- [Headless Chromium](https://chromium.googlesource.com/chromium/src/+/lkgr/headless/README.md)
- [Rich JavaScript Applications – the Seven Frameworks](http://blog.stevensanderson.com/2012/08/01/rich-javascript-applications-the-seven-frameworks-throne-of-js-2012/)
- [Essential Image Optimization](https://images.guide/) :sparkles:
- [Why does Google prepend while(1); to their JSON responses?](https://stackoverflow.com/questions/2669690/why-does-google-prepend-while1-to-their-json-responses)
- [In defense of Functional CSS](https://www.mikecr.it/ramblings/functional-css/)
- [Douglas Crockford: Really. JavaScript.](https://www.youtube.com/watch?v=lTWGoL1N-Kc) :tv:
- [Defensive JavaScript](https://www.javascriptjanuary.com/blog/defensive-javascript)
- [What is `this`? The Inner Workings of JavaScript Objects](https://medium.com/javascript-scene/what-is-this-the-inner-workings-of-javascript-objects-d397bfa0708a)
- [Responsible JavaScript](https://alistapart.com/article/responsible-javascript-part-1/)
- [JavaScript Event Loop And Call Stack Explained](https://felixgerschau.com/javascript-event-loop-call-stack/) :zap:
- [Looking into assembly code of coercion](https://wanago.io/2018/04/02/1-2-3-9-looking-into-assembly-code-of-coercion/)
- [A cartoon intro to WebAssembly](https://hacks.mozilla.org/2017/02/a-cartoon-intro-to-webassembly/)
    - [What makes WebAssembly fast?](https://hacks.mozilla.org/2017/02/what-makes-webassembly-fast/)
- [The Lost Art of the Makefile](http://www.olioapps.com/blog/the-lost-art-of-the-makefile/) :sparkles::sparkles:
- [Streams—The definitive guide](https://web.dev/streams/)

### React, Redux

- [Under the hood ReactJS](https://github.com/Bogdan-Lyashenko/Under-the-hood-ReactJS)
- [Thinking in React](https://reactjs.org/docs/thinking-in-react.html)
- [React Implementation Notes](https://reactjs.org/docs/implementation-notes.html)
- [React Internals](http://www.mattgreer.org/articles/react-internals-part-one-basic-rendering/)
- [Scheduling in React](https://philippspiess.com/scheduling-in-react/)

### v8

- [v8 Resource](https://github.com/ray-cp/browser_pwn_resources/blob/master/v8_resources.md)
- [Understanding V8’s Bytecode](https://medium.com/dailyjs/understanding-v8s-bytecode-317d46c94775)
- [Concurrent marking in V8](https://v8project.blogspot.com/2018/06/concurrent-marking.html)
- [V8 / Chrome Architecture Reading List - For Vulnerability Researchers](https://zon8.re/posts/v8-chrome-architecture-reading-list-for-vulnerability-researchers/)

### JS Books

- [You Don't Know JS](https://github.com/getify/You-Dont-Know-JS)
- [Javascript: The Good Parts](http://www.amazon.in/Javascript-Good-Parts-D-Crockford/dp/0596517742)
- [Mostly Adequate Guide to Functional Programming](https://drboolean.gitbooks.io/mostly-adequate-guide/)
- [Programming JavaScript Applications](http://chimera.labs.oreilly.com/books/1234000000262/)
- [The JavaScript Way](https://github.com/bpesquet/thejsway)

## Rust

- [A Gentle Introduction To Rust](https://stevedonovan.github.io/rust-gentle-intro/1-basics.html)
- [Rust Docs](https://doc.rust-lang.org/rust-by-example/std/result.html) :book:
- [Rust Design Patterns](https://github.com/rust-unofficial/patterns)
- [Rethinking Systems Programming](https://thoughtram.io/rust-and-nickel/#/) :sparkles:
- [The Rust Programming Language](https://doc.rust-lang.org/book/)
- [Learning systems programming with Rust](https://jvns.ca/blog/2016/09/11/rustconf-keynote/)
- [Learn Rust With Entirely Too Many Linked Lists](https://rust-unofficial.github.io/too-many-lists/index.html)
- [Fearless Concurrency with Rust](https://blog.rust-lang.org/2015/04/10/Fearless-Concurrency.html)

## Database

- [Secure PostgreSQL](https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps) :lock:
- [SQL vs NoSQL](https://www.airpair.com/postgresql/posts/sql-vs-nosql-ko-postgres-vs-mongo)
- [Build a simple database](https://cstack.github.io/db_tutorial/)
- [One Giant Leap For SQL: MySQL 8.0 Released](https://modern-sql.com/blog/2018-04/mysql-8.0) :sparkles:
- [MongoDB is to NoSQL like MySQL to SQL — in the most harmful way](https://use-the-index-luke.com/blog/2013-10/mysql-is-to-sql-like-mongodb-to-nosql)
- [How Postgres Makes Transactions Atomic](https://brandur.org/postgres-atomicity)
- [Building Robust Systems with ACID and Constraints](https://brandur.org/acid) :sparkles:
- [Awesome Database Learning](https://github.com/pingcap/awesome-database-learning)
- [Database Internals](https://www.databass.dev/) :book: :construction:
- [Things I Wished More Developers Knew About Databases](https://rakyll.medium.com/things-i-wished-more-developers-knew-about-databases-2d0178464f78) :construction:
- [PostgreSQL LISTEN/NOTIFY](https://tapoueh.org/blog/2018/07/postgresql-listen-notify/)
- [Maximizing MongoDB Performance on AWS](https://www.mongodb.com/blog/post/maximizing-mongodb-performance-on-aws)
- [Read Consistency with Database Replicas](https://shopify.engineering/read-consistency-database-replicas)
- [Zero downtime Postgres migration, done right](https://engineering.theblueground.com/blog/zero-downtime-postgres-migration-done-right/)
- [Inconsistent thoughts on database consistency](https://www.alexdebrie.com/posts/database-consistency/)

### Sharding

- [Understanding Database Sharding](https://www.digitalocean.com/community/tutorials/understanding-database-sharding)
- [An Unorthodox Approach To Database Design : The Coming Of The Shard](http://highscalability.com/blog/2009/8/6/an-unorthodox-approach-to-database-design-the-coming-of-the.html) :sparkles:
- [Spanner's High Availability Writes](https://rakyll.org/spanner-ha-writes/)

<details>
<summary>Papers</summary>
<p>

- [Spanner: Google’s Globally Distributed Database](http://delivery.acm.org/10.1145/2500000/2491245/a8-corbett.pdf)
- [A Call to Arms: Revisiting Database Design](https://arxiv.org/pdf/1105.6001.pdf)
- [Architecture of a Database System](http://db.cs.berkeley.edu/papers/fntdb07-architecture.pdf)
- [ACIDRain: Concurrency-Related Attacks on Database-Backed Web Applications](http://www.bailis.org/papers/acidrain-sigmod2017.pdf)

</p>
</details>

## Tor

- [Research problems: Ten ways to discover Tor bridges](https://blog.torproject.org/blog/research-problems-ten-ways-discover-tor-bridges)
- [Selected Papers in Anonymity](https://www.freehaven.net/anonbib/topic.html) :page_with_curl:
- [Onion Router](https://www.onion-router.net/)
- [Anti-Censorship & Transparency - Roger Dingledine](https://www.youtube.com/watch?v=35l56KjTCb8) :tv:
- [How does Tor work?](https://robertheaton.com/2019/04/06/how-does-tor-work/)
- [How Tor Works](https://jordan-wright.com/blog/2015/02/28/how-tor-works-part-one/)

### Tor Papers

- [Tor Design](https://svn.torproject.org/svn/projects/design-paper/tor-design.pdf)
- [Tor Bridge Discovery](http://www.cs.uml.edu/~xinwenfu/paper/Bridge.pdf)
- [A Model of Onion Routing with Provable Anonymity](https://www.onion-router.net/Publications/or-iomodel.pdf)
- [Locating Hidden Servers](https://www.onion-router.net/Publications/locating-hidden-servers.pdf)

## Functional Programming

- [What is Functional Programming ?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0)
- [Functional Programming Jargon](https://github.com/hemanth/functional-programming-jargon)
- [What is a Functional Composition](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-function-composition-20dfb109a1a0)
- [What is Pure function?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-pure-function-d1c076bec976)
- [Functional Programming](http://wiki.c2.com/?FunctionalProgramming)
- [So You Want to be a Functional Programmer](https://medium.com/@cscalfani/so-you-want-to-be-a-functional-programmer-part-1-1f15e387e536)
- [Practical Functional Programming](https://hackernoon.com/practical-functional-programming-6d7932abc58b)
- [Mostly Adequate Guide to Functional Programming](https://mostly-adequate.gitbooks.io/mostly-adequate-guide/) :sparkles:
- [Parse, don’t validate](https://lexi-lambda.github.io/blog/2019/11/05/parse-don-t-validate/)
- [Functors, Applicatives, And Monads In Pictures](http://adit.io/posts/2013-04-17-functors,_applicatives,_and_monads_in_pictures.html) :sparkles: :sparkles: :zap: :zap:
- [A Glossary of Functional Programming](https://degoes.net/articles/fp-glossary)
- [Scala Italy 2019 - John A De Goes - A Tour of Functional Design](https://vimeo.com/370819261) :tv:

## OAuth

- [An Introduction to OAuth 2](https://www.digitalocean.com/community/tutorials/an-introduction-to-oauth-2)
- [The OAuth 2.0 Authorization Framework RFC](https://tools.ietf.org/html/rfc6749)
- [Securing API with OAuth 2.0](https://alexbilbie.com/2013/02/securing-your-api-with-oauth-2/) :lock:

## Regex

- [Learn Regex](http://regexr.com/)
- [Interactive Exercise](https://regexone.com/)
- https://github.com/zeeshanu/learn-regex
- [Regex For Noobs](https://www.janmeppe.com/blog/regex-for-noobs/)

## Distributed Systems

> [Distributed Systems for fun and profit](http://book.mixu.net/distsys/) :books:

- [Introduction to Distributed System Design](http://www.hpcs.cs.tsukuba.ac.jp/~tatebe/lecture/h23/dsys/dsd-tutorial.html)
- [Raft: Understandable Distributed Consensus](http://thesecretlivesofdata.com/raft/) :sparkles:
    - [In Search of an Understandable Consensus Algorithm](https://raft.github.io/raft.pdf) :page_with_curl: :construction:
- [HTTP is obsolete. It's time for the Distributed Web](https://blog.neocities.org/blog/2015/09/08/its-time-for-the-distributed-web.html)
- [Rack Model](https://arxiv.org/abs/1302.5657) :page_with_curl:
- [If you need a global lock in your distributed system, then you're already in trouble](https://news.ycombinator.com/item?id=11066258) :sparkles:
    - Parent Thread: [Is Redlock Safe? Reply to Redlock Analysis](https://news.ycombinator.com/item?id=11065933)
- [Towards Robust Distributed Systems](https://people.eecs.berkeley.edu/~brewer/cs262b-2004/PODC-keynote.pdf)
- [CAP Theorem](https://en.wikipedia.org/wiki/CAP_theorem)
    - [How to beat the CAP theorem](http://nathanmarz.com/blog/how-to-beat-the-cap-theorem.html) :sparkles:
    - [CAP Theorem: Revisited](https://robertgreiner.com/cap-theorem-revisited/)
    - [FLP and CAP aren't the same thing](https://www.the-paper-trail.org/post/2012-03-25-flp-and-cap-arent-the-same-thing/)
    - https://news.ycombinator.com/item?id=1768312 :zap:
        - [You Can’t Sacrifice Partition Tolerance](https://codahale.com/you-cant-sacrifice-partition-tolerance/) :zap:
    - https://www.infoq.com/articles/cap-twelve-years-later-how-the-rules-have-changed/
    - [An Illustrated Proof of the CAP Theorem](https://mwhittaker.github.io/blog/an_illustrated_proof_of_the_cap_theorem/)
- [Designing Distributed Systems: Patterns and Paradigms for Scalable, Reliable Services](https://www.oreilly.com/library/view/designing-distributed-systems/9781491983638/) :book: :construction:
- [Distributed systems theory for the distributed systems engineer](https://www.the-paper-trail.org/post/2014-08-09-distributed-systems-theory-for-the-distributed-systems-engineer/) :sparkles: :file_folder:
- [Fallacies of distributed computing](https://en.wikipedia.org/wiki/Fallacies_of_distributed_computing)
- Consesus Protocols
    - [Consensus Protocols: Two-Phase Commit](https://www.the-paper-trail.org/post/2008-11-27-consensus-protocols-two-phase-commit/)
    - [Consensus Protocols: Three-phase Commit](https://www.the-paper-trail.org/post/2008-11-29-consensus-protocols-three-phase-commit/)
    - [Consensus Protocols: Paxos](https://www.the-paper-trail.org/post/2009-02-03-consensus-protocols-paxos/) :construction:
    - [Notes on Paxos](https://matklad.github.io/2020/11/01/notes-on-paxos.html)
- [Keeping CALM: When Distributed Consistency Is Easy](https://cacm.acm.org/magazines/2020/9/246941-keeping-calm/fulltext)
- [Brewer’s Conjecture and the Feasibility of Consistent, Available, Partition-Tolerant Web Services](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.67.6951&rep=rep1&type=pdf) :page_with_curl: :construction:
- [Thinking about Availability in Large Service Infrastructures](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/46181.pdf)
- [Questioning the Lambda Architecture](https://www.oreilly.com/ideas/questioning-the-lambda-architecture)
- [Avoiding fallback in distributed systems](https://aws.amazon.com/builders-library/avoiding-fallback-in-distributed-systems/)
- [Consistency Models](https://jepsen.io/consistency) :construction:
- [A Distributed Systems Reading List](https://dancres.github.io/Pages/) :file_folder:
- [Please stop calling databases CP or AP](https://martin.kleppmann.com/2015/05/11/please-stop-calling-databases-cp-or-ap.html)
- [The network is reliable](https://aphyr.com/posts/288-the-network-is-reliable)
- [Managing Critical State: Distributed Consensus for Reliability](https://sre.google/sre-book/managing-critical-state/)

## Kafka

- ["Apache Kafka and the Next 700 Stream Processing Systems" by Jay Kreps](https://www.youtube.com/watch?v=9RMOc0SwRro) :tv:
- [Streaming 101: The world beyond batch](https://www.oreilly.com/ideas/the-world-beyond-batch-streaming-101)
- [Kafka and Zookeeper with Docker](https://medium.com/rahasak/kafka-and-zookeeper-with-docker-65cff2c2c34f)
- [A Guide To The Kafka Protocol](https://cwiki.apache.org/confluence/display/KAFKA/A+Guide+To+The+Kafka+Protocol#AGuideToTheKafkaProtocol-Introduction)
- [The Unofficial Kafka Rebalance How-To](https://tomlee.co/2019/03/the-unofficial-kafka-rebalance-how-to/)
- [High Performance Kafka Producers](https://www.jesseyates.com/2020/01/01/high-performance-kafka-producers.html)
- [\_\_consumer_offsets topic in kafka](https://kafka.apache.org/0110/documentation.html#impl_offsettracking)
- [Vertically scaling Kafka consumers](https://www.jesseyates.com/2019/12/04/vertically-scaling-kafka-consumers.html)
- [Apache Kafka Rebalance Protocol, or the magic behind your streams applications](https://medium.com/streamthoughts/apache-kafka-rebalance-protocol-or-the-magic-behind-your-streams-applications-e94baf68e4f2)
- [Apache Kafka Supports 200K Partitions Per Cluster](https://www.confluent.io/blog/apache-kafka-supports-200k-partitions-per-cluster/)
- [It’s Okay To Store Data In Apache Kafka](https://www.confluent.io/blog/okay-store-data-apache-kafka/)
- [Kafka: The Definitive Guide](https://www.confluent.io/resources/kafka-the-definitive-guide/) :book:
- [Disaster Recovery for Multi-Region Kafka at Uber](https://eng.uber.com/kafka/)
- [A Practical Introduction to Kafka Storage Internals](https://medium.com/@durgaswaroop/a-practical-introduction-to-kafka-storage-internals-d5b544f6925f)

## Spark

- [Memory Management Overview](http://spark.apache.org/docs/latest/tuning.html#memory-management-overview)
- [Tricks of the Trade: Tuning JVM Memory for Large-scale Services](https://eng.uber.com/jvm-tuning-garbage-collection/)
- [Managing Spark Partitions with Coalesce and Repartition](https://medium.com/@mrpowers/managing-spark-partitions-with-coalesce-and-repartition-4050c57ad5c4#.36o8a7b5j)
- [The hidden cost of Spark withColumn](https://manuzhang.github.io/output/2018-07-11-spark-catalyst-cost/index.html)

### Logging

- [Spark Streaming Logging Configuration](http://shzhangji.com/blog/2015/05/31/spark-streaming-logging-configuration/)
- [S3 Log4j Appender](https://www.therealvan.com/s3loggerappender.html)
- [Log4j appender with S3 and search publishing](https://github.com/bluedenim/log4j-s3-search)

## Monitoring

### Prometheus

- [When to use the Pushgateway](https://prometheus.io/docs/practices/pushing/)
- [Common pitfalls when using the Pushgateway](https://www.robustperception.io/common-pitfalls-when-using-the-pushgateway)
- [On the naming of things](https://www.robustperception.io/on-the-naming-of-things) :sparkles:
- [Prometheus Recording Rules](https://deploy.live/blog/today-i-learned-prometheus-recording-rules/)
- [Prometheus Counters and how to deal with them](https://www.innoq.com/en/blog/prometheus-counters/)
- [Thanos](https://github.com/thanos-io/thanos)
- [PromQL Queries for Exploring Your Metrics](https://promlabs.com/blog/2020/12/17/promql-queries-for-exploring-your-metrics)
- [How to learn PromQL with Prometheus Playground](https://iximiuz.com/en/posts/prometheus-learning-promql/)

### More

- [Statsd: Measure Anything, Measure Everything](https://codeascraft.com/2011/02/15/measure-anything-measure-everything/)
- [JVM Profiler: An Open Source Tool for Tracing Distributed JVM Applications at Scale](https://eng.uber.com/jvm-profiler/)
- [Telltale: Netflix Application Monitoring Simplified](https://netflixtechblog.com/telltale-netflix-application-monitoring-simplified-5c08bfa780ba)
- [Understanding the Top 5 Redis Performance Metrics](https://www.datadoghq.com/pdf/Understanding-the-Top-5-Redis-Performance-Metrics.pdf)

## System Design

### Guides

- [Metcalfe's law](https://en.wikipedia.org/wiki/Metcalfe%27s_law)
- [Learn how to design large-scale systems](https://github.com/donnemartin/system-design-primer) :sparkles:
- [A Brief History of High Availability](https://www.cockroachlabs.com/blog/brief-history-high-availability/)
- [Introduction to Microservices](https://www.nginx.com/blog/introduction-to-microservices/)
- [What is Kappa Architecture?](http://milinda.pathirage.org/kappa-architecture.com/)
- [Principles of chaos engineering](http://principlesofchaos.org/)
- [Microservices — architecture nihilism in minimalism's clothes](https://vlfig.me/posts/microservices) :sparkles:
- [Failing over without falling over](https://stackoverflow.blog/2020/10/23/adrian-cockcroft-aws-failover-chaos-engineering-fault-tolerance-distaster-recovery/) :zap:
- [Timeouts, retries, and backoff with jitter](https://aws.amazon.com/builders-library/timeouts-retries-and-backoff-with-jitter/)
- [Why are services slow sometimes?](https://dev.to/aws/why-are-services-slow-sometimes-mn3) :zap:
    - [If at first you don't get an answer...](https://dev.to/aws/if-at-first-you-don-t-get-an-answer-3e85)
- [Understanding Connections & Pools](https://sudhir.io/understanding-connections-pools/) :zap: :zap:
- [The Big Little Guide to Message Queues](https://sudhir.io/the-big-little-guide-to-message-queues/)
- [MonolithFirst](https://martinfowler.com/bliki/MonolithFirst.html)
- [A List of Post-mortems!](https://github.com/danluu/post-mortems)
- [Exponential Backoff And Jitter](https://aws.amazon.com/blogs/architecture/exponential-backoff-and-jitter/)

### Systems

> [(A few) Ops Lessons We All Learn The Hard Way](https://www.netmeister.org/blog/ops-lessons.html)

- [Reddit: How We Built r/Place](https://redditblog.com/2017/04/13/how-we-built-rplace/) :sparkles:
- [Uber: Why Uber Engineering Switched from Postgres to MySQL](https://eng.uber.com/mysql-migration/)
- [Dropbox: How we migrated Dropbox from Nginx to Envoy](https://dropbox.tech/infrastructure/how-we-migrated-dropbox-from-nginx-to-envoy)
- [Cloudflare: How Cloudflare’s Architecture Can Scale to Stop the Largest Attacks](https://www.cloudflare.com/media/pdf/cf-wp-dns-attacks.pdf)
- Making Instagram.com faster
    - [Part 1](https://instagram-engineering.com/making-instagram-com-faster-part-1-f350c8fba0d4) - Prefetching data
    - [Part 2](https://instagram-engineering.com/making-instagram-com-faster-part-2-f350c8fba0d4) - Pushing data directly to the client rather than waiting for the client to request the data
    - [Part 3](https://instagram-engineering.com/making-instagram-com-faster-part-3-cache-first-6f3f130b9669) - Cache-first rendering
    - [Part 4](https://instagram-engineering.com/making-instagram-com-faster-code-size-and-execution-optimizations-part-4-57668be796a8) - Code size and execution optimizations
- [Billions of Messages a Day - Yelp's Real-time Data Pipeline](https://engineeringblog.yelp.com/2016/07/billions-of-messages-a-day-yelps-real-time-data-pipeline.html)
- [The WhatsApp Architecture Facebook Bought For $19 Billion](http://highscalability.com/blog/2014/2/26/the-whatsapp-architecture-facebook-bought-for-19-billion.html)
- [Airbnb: Avoiding Double Payments in a Distributed Payments System](https://medium.com/airbnb-engineering/avoiding-double-payments-in-a-distributed-payments-system-2981f6b070bb)
- [How We Developed DingTalk: Implementing the Message System Architecture](https://www.alibabacloud.com/blog/how-we-developed-dingtalk-implementing-the-message-system-architecture_595905)
- [Intelligent DNS based load balancing at Dropbox](https://dropbox.tech/infrastructure/intelligent-dns-based-load-balancing-at-dropbox)
- [Redis Explained](https://architecturenotes.co/redis/)

### Scalability

- [Jeremy Edberg - Scalable Cloud Architectures | Tech Talk](https://www.youtube.com/watch?v=cCAO9moDucI&t=1s) :tv:
- [CS75 (Summer 2012) Lecture 9 Scalability Harvard Web Development](https://www.youtube.com/watch?v=-W9F__D3oY4) :tv: :zap:
- [A Word on Scalability](https://www.allthingsdistributed.com/2006/03/a_word_on_scalability.html)
- [Scalability for Dummies](https://www.lecloud.net/post/7295452622/scalability-for-dummies-part-1-clones) :sparkles:
- [Scalable System Design Patterns](https://horicky.blogspot.com/2010/10/scalable-system-design-patterns.html)
- [Scalable Web Architecture and Distributed Systems](https://www.aosabook.org/en/distsys.html)
- [The Tail at Scale](https://cseweb.ucsd.edu/~gmporter/classes/fa17/cse124/post/schedule/p74-dean.pdf) :page_with_curl:
- [Automating chaos experiments in production](https://arxiv.org/pdf/1905.04648.pdf)
- [Eventually Consistent - Revisited](https://www.allthingsdistributed.com/2008/12/eventually_consistent.html)

### Event driven Architecture

- [Build Services on a Backbone of Events](https://www.confluent.io/blog/build-services-backbone-events/)

### AWS

- [Everything You Need To Know About Networking On AWS](https://grahamlyons.com/article/everything-you-need-to-know-about-networking-on-aws)
- [Deep Dive on Amazon ECS Cluster Auto Scaling](https://aws.amazon.com/blogs/containers/deep-dive-on-amazon-ecs-cluster-auto-scaling/) :sparkles: :construction:
- [Designing scalable API on AWS spot instances](https://blog.adapty.io/designing-scalable-api-on-aws-stop-instance/)
- [Workload isolation using shuffle-sharding](https://aws.amazon.com/builders-library/workload-isolation-using-shuffle-sharding/)
- [The Hitchhiker's Guide to AWS ECS and Docker](https://start.jcolemorrison.com/the-hitchhikers-guide-to-aws-ecs-and-docker/)
- [AWS IAM Policies in a Nutshell](https://start.jcolemorrison.com/aws-iam-policies-in-a-nutshell/)
- [What You Need to Know About IOPS](https://cloudcasts.io/article/what-you-need-to-know-about-iops)
- [Why was a query to my Amazon RDS MySQL DB instance blocked when there is no other active session?](https://aws.amazon.com/premiumsupport/knowledge-center/blocked-mysql-query/)

### Netflix

- [Mastering Chaos - A Netflix Guide to Microservices](https://www.youtube.com/watch?v=CZ3wIuvmHeM) :tv: :sparkles:
- [How we scaled nginx and saved the world 54 years every day](https://blog.cloudflare.com/how-we-scaled-nginx-and-saved-the-world-54-years-every-day)
- [Building fast.com](https://netflixtechblog.com/building-fast-com-4857fe0f8adb)
- [AWS re:Invent 2017: How Netflix Tunes Amazon EC2 Instances for Performance (CMP325)](https://www.youtube.com/watch?v=89fYOo1V2pA) :tv:
- [AWS re:Invent 2015: A Day in the Life of a Netflix Engineer (DVO203)](https://www.youtube.com/watch?v=-mL3zT1iIKw) :tv: :zap:
- [Edge Authentication and Token-Agnostic Identity Propagation](https://netflixtechblog.com/edge-authentication-and-token-agnostic-identity-propagation-514e47e0b602)

### Cloudflare

- [A deep-dive into Cloudflare’s autonomous edge DDoS protection](https://blog.cloudflare.com/deep-dive-cloudflare-autonomous-edge-ddos-protection/)

## Privacy

- [Cutting Google out of your life](https://degoogle.jmoore.dev/)
- [The Fantasy of Opting Out](https://thereader.mitpress.mit.edu/the-fantasy-of-opting-out/)
- [The Hitchhiker's Guide to Online Anonymity](https://anonymousplanet.org/)
- [You should turn off autofill in your password manager](https://marektoth.com/blog/password-managers-autofill/)

## Security

### Attacks

- [SSL Strip](https://github.com/moxie0/sslstrip)
- [SQL Injection](https://www.owasp.org/index.php/Testing_for_SQL_Injection_(OTG-INPVAL-005))
- [Binary Exploitation](https://github.com/CodeMaxx/Binary-Exploitation)
- [SQL Attack Constraint Based](https://dhavalkapil.com/blogs/SQL-Attack-Constraint-Based/)
- [DNS Reconnaissance – DNSRecon](https://pentestlab.blog/2012/11/13/dns-reconnaissance-dnsrecon/)
- [What is a DDoS Attack?](https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/)
- [Server Side Request Forgery (SSRF)?](https://www.acunetix.com/blog/articles/server-side-request-forgery-vulnerability/)
- [All you need to know about SYN floods](https://blog.dubbelboer.com/2012/04/09/syn-cookies.html)
- ["kernel: Possible SYN flooding on port X. Sending cookies" is logged](https://access.redhat.com/solutions/30453)
- [SSL Strip for Newbies](https://avicoder.me/2016/02/22/SSLstrip-for-newbies/)
- [Cold Boot Attack](https://en.wikipedia.org/wiki/Cold_boot_attack)
- [Heartbleed Bug](http://heartbleed.com/)
- [Shellshock](https://en.wikipedia.org/wiki/Shellshock_%28software_bug%29)
- [Mirai Botnet](https://en.wikipedia.org/wiki/Mirai_(malware))
- [POODLE](https://en.wikipedia.org/wiki/POODLE)
- [Format string attack](https://www.owasp.org/index.php/Format_string_attack)
- [Off-by-one error](https://en.wikipedia.org/wiki/Off-by-one_error)
- [EFAIL](https://efail.de/)
- [HTTP Desync Attacks: Request Smuggling Reborn](https://portswigger.net/research/http-desync-attacks-request-smuggling-reborn)
- [The SSL FREAK vulnerability explained](https://robertheaton.com/2015/04/06/the-ssl-freak-vulnerability/)
- [Abusing HTTP hop-by-hop request headers](https://nathandavison.com/blog/abusing-http-hop-by-hop-request-headers)
- [Memcrashed - Major amplification attacks from UDP port 11211](https://blog.cloudflare.com/memcrashed-major-amplification-attacks-from-port-11211/amp/)
- [Analyzing the Attacks on my Website](https://dev.to/pluralsight/analyzing-the-attacks-on-my-website-30jf)
- [How does a TCP reset attack work](https://robertheaton.com/2020/04/27/how-does-a-tcp-reset-attack-work/)
- [Cracking the lens: targeting HTTP's hidden attack-surface](https://portswigger.net/research/cracking-the-lens-targeting-https-hidden-attack-surface)
- [Web Cache Entanglement: Novel Pathways to Poisoning](https://portswigger.net/research/web-cache-entanglement)
- [Reading Data via CSS Injection](https://curesec.com/blog/article/blog/Reading-Data-via-CSS-Injection-180.html)
- [Network Ingress Filtering: Defeating Denial of Service Attacks which employ IP Source Address Spoofing](https://tools.ietf.org/html/bcp38)
- [SAD DNS Explained](https://blog.cloudflare.com/sad-dns-explained/) :sparkles: :zap:
- [Hidden OAuth attack vectors](https://portswigger.net/research/hidden-oauth-attack-vectors)
- [HTTP request smuggling](https://portswigger.net/web-security/request-smuggling)

### Tools

- [GDB: The GNU Project Debugger](https://www.gnu.org/software/gdb/documentation/)
    - [gdb Debugging Full Example (Tutorial): ncurses](http://www.brendangregg.com/blog/2016-08-09/gdb-example-ncurses.html)
    - [GDB Cheatsheet](https://darkdust.net/files/GDB%20Cheat%20Sheet.pdf)
    - [CppCon 2015: Greg Law "Give me 15 minutes & I'll change your view of GDB"](https://www.youtube.com/watch?v=PorfLSr3DDI) :tv:
- [Cipher Tools](http://rumkin.com/tools/cipher/)

### Guides

- [CTF Field Guide](https://trailofbits.github.io/ctf) :sparkles:
- [Buffer Overflow](http://cecs.wright.edu/~pmateti/InternetSecurity/Lectures/BufferOverflow/alephOne.html)
- [Sometimes HTTP > HTTPS](https://stormpath.com/blog/why-http-is-sometimes-better-than-https)
- [Security list for fun and profit](https://github.com/zbetcheckin/Security_list)
- [What “hacking” competitions/challenges exist?](https://security.stackexchange.com/questions/3592/what-hacking-competitions-challenges-exist)
- [Reverse Shell Cheat Sheet](http://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet) :sparkles:
- [Beware of strncpy() and strncat()](https://eklitzke.org/beware-of-strncpy-and-strncat)
- [Lessons learned and misconceptions regarding encryption and cryptology](https://security.stackexchange.com/questions/2202/lessons-learned-and-misconceptions-regarding-encryption-and-cryptology) :sparkles:
- [GOT and PLT for pwning](https://systemoverlord.com/2017/03/19/got-and-plt-for-pwning.html)
- [A Look at The Draft for JWT Best Current Practices](https://auth0.com/blog/a-look-at-the-latest-draft-for-jwt-bcp/)
- [LiveOverflow Binary Hacking](https://www.youtube.com/playlist?list=PLhixgUqwRTjxglIswKp9mpkfPNfHkzyeN) :tv:
- [Advanced web security topics](https://blog.georgovassilis.com/2016/04/16/advanced-web-security-topics/)
- [Don't publicly expose .git](https://en.internetwache.org/dont-publicly-expose-git-or-how-we-downloaded-your-websites-sourcecode-an-analysis-of-alexas-1m-28-07-2015/) :sparkles:
- [The State Of Software Security In 2019](https://noncombatant.org/2019/01/06/state-of-security-2019/) :lock:
- [The definitive super list for "Google Hacking"](https://gist.github.com/cmartinbaughman/5877945)
- [A list of useful payloads and bypass for Web Application Security and Pentest/CTF](https://github.com/swisskyrepo/PayloadsAllTheThings/)
- [Now you C me, now you don't: An introduction to the hidden attack surface of interpreted languages](https://securitylab.github.com/research/now-you-c-me)
- [Simple Bugs With Complex Exploits](https://www.elttam.com/blog/simple-bugs-with-complex-exploits/#content)

### Games and CTF's

- [Web for Pentesters](https://www.pentesterlab.com/exercises/web_for_pentester/course)
- [Overthewire](http://overthewire.org/wargames/)
- [Crypto Challenges](http://cryptopals.com/)
- https://picoctf.com/
- https://pwnable.kr
- http://gracker.org/
- http://websec.fr/
- https://365.csaw.io/
- https://crackmes.one/

### Crypto

- [So, You Want To Learn To Break Ciphers](https://littlemaninmyhead.wordpress.com/2015/09/28/so-you-want-to-learn-to-break-ciphers/)
- [Alice & Bob : A History of The World’s Most Famous Cryptographic Couple](http://cryptocouple.com/)
- [Implementing AES](http://blog.nindalf.com/implementing-aes/)
- [A Stick Figure Guide to the Advanced Encryption Standard (AES)](http://www.moserware.com/2009/09/stick-figure-guide-to-advanced.html)
- [An Intensive Introduction to Cryptography](https://intensecrypto.org/public/) :book:
- [First SHA1 Collision](https://security.googleblog.com/2017/02/announcing-first-sha1-collision.html)
- [Myths about /dev/urandom](https://www.2uo.de/myths-about-urandom/#blocking)
- [The Joy of Cryptography](http://web.engr.oregonstate.edu/~rosulekm/crypto/)
- [Bcrypt Step by Step](https://qvault.io/2020/08/24/bcrypt-step-by-step/)
- [Bcrypt](https://auth0.com/blog/hashing-in-action-understanding-bcrypt/)
- [Why shouldn't we roll our own?](http://security.stackexchange.com/questions/18197/why-shouldnt-we-roll-our-own) :sparkles:
- [How to securely hash passwords?](https://security.stackexchange.com/a/31846/179997)
- [How To Safely Store A Password](https://codahale.com/how-to-safely-store-a-password/) :zap:
- [So you want to roll your own crypto?](https://vnhacker.blogspot.com/2020/08/so-you-want-to-roll-your-own-crypto.html?m=1)

### Security Papers

- [Untraceable electronic mail, return addresses, and digital pseudonyms](https://mirror.robert-marquardt.com/anonbib/cache/chaum-mix.pdf)
- [Understanding the Mirai Botnet](https://www.usenix.org/system/files/conference/usenixsecurity17/sec17-antonakakis.pdf)
- [Exposing Private Information by Timing Web Applications](https://crypto.stanford.edu/~dabo/papers/webtiming.pdf)
- [Security, Authentication, and Public Key Systems](http://www.merkle.com/papers/Thesis1979.pdf)
- [A Future-Adaptable Password Scheme](https://www.usenix.org/legacy/events/usenix99/provos/provos.pdf)
- [Too Much Crypto](https://eprint.iacr.org/2019/1492.pdf)

## x vs y :hocho:

- [Ruby vs Python](https://hackernoon.com/ruby-vs-python-the-definitive-faq-5cb0046292be#.xptk2egps)
- [Weapon of Mass Destruction](http://www.kitploit.com/2017/02/wmd-weapon-of-mass-destruction-python.html)
- [Leaving Clojure for Ruby](https://blog.appcanary.com/2017/hard-isnt-simple-ruby-clojure.html)
- [Why Rust and not Go](https://blog.juliobiason.me/thoughts/why-rust-and-not-go/) :sparkles:
- [Why Go and Rust are Competitors](http://www.doxsey.net/blog/why-go-and-rust-are-competitors)
- [A Response to Hello World](http://www.doxsey.net/blog/a-response-to-hello-world)
- [Kafka vs. Pulsar vs. RabbitMQ: Performance, Architecture, and Features Compared](https://www.confluent.io/kafka-vs-pulsar/)

## Useful Command Line Tools

- [tldr](https://github.com/tldr-pages/tldr)
- [Rofi: A window switcher, application launcher and dmenu replacement](https://github.com/DaveDavenport/rofi)
- [fd: A simple, fast and user-friendly alternative to find](https://github.com/sharkdp/fd)
- [SCM breeze: Adds numbered shortcuts to the output git status, and much more ](https://github.com/scmbreeze/scm_breeze)
- [Pass: Simple password manager using gpg and ordinary unix directories](https://www.passwordstore.org/)
- [peerflix](https://github.com/mafintosh/peerflix)
- [kaf: Modern CLI for Apache Kafka](https://github.com/birdayz/kaf)
- [curl statistics made simple](https://github.com/reorx/httpstat)
- [mkcert](https://github.com/FiloSottile/mkcert)
- [sshuttle - Transparent proxy server that works as a poor man's VPN.](https://github.com/sshuttle/sshuttle)
- [jq](https://stedolan.github.io/jq/)

## Blogs

- http://arjunsreedharan.org/
- https://jvns.ca/
- https://githubengineering.com/
- http://nullprogram.com/index/
- https://zwischenzugs.com/
- https://mkdev.me/en/posts
- https://blog.cloudflare.com/
- http://prog21.dadgum.com/
- https://increment.com/programming-languages/ :sparkles:
- https://blog.filippo.io/
- http://highscalability.com
- https://notes.shichao.io/
- https://blog.acolyer.org/ - If you are into research papers
- https://lwn.net/
- https://queue.acm.org/
- https://www.the-paper-trail.org/
- https://overreacted.io/
- https://robertheaton.com/
- https://www.mnot.net/blog/
- https://systemoverlord.com/
- https://blog.rpis.ec/
- https://blog.jessfraz.com/
- https://www.hackinglinuxexposed.com/articles/
- https://rpis.ec/
- https://dave.cheney.net/ - Mostly Golang related
- http://www.brendangregg.com/
- https://www.scalescale.com/
- https://medium.com/@blanchon.vincent :sparkles:
- https://sysadvent.blogspot.com/
- [A handbook for making programming languages](http://craftinginterpreters.com/)
- https://codewithoutrules.com/
- https://code.flickr.net/
- https://microservices.io/index.html :sparkles:
- https://engineering.fb.com/
- [Cryptography Services Archives](https://cryptoservices.github.io/archives/) :lock:
- https://timilearning.com/ :construction:
- https://aws.amazon.com/builders-library/ - How Amazon builds and operates software
- https://rhinosecuritylabs.com/blog/?category=aws
- https://how.complexsystems.fail/
- https://ops.tips

## More

- [Password storage in source control](https://stackoverflow.com/questions/559611/password-storage-in-source-control)
- [Difference b/w Integration and Unit Tests](https://stackoverflow.com/questions/10752/what-is-the-difference-between-integration-and-unit-tests/7876055#7876055)
- [The language of choice](https://codewords.recurse.com/issues/four/the-language-of-choice)
- [Programmer Competency Matrix](http://sijinjoseph.com/programmer-competency-matrix/)
- [Hacker's guide to Neural Networks](http://karpathy.github.io/neuralnets/)
- [Return to the Source](http://www.cipht.net/2017/10/05/why-read-code.html)
- [A list of everything that could go in the \<head\> of your document](https://github.com/joshbuchea/HEAD)
- [Design Patterns](https://sourcemaking.com/design_patterns) :sparkles:
- [Ask HN: “Write your own” or “Build your own” software projects](https://news.ycombinator.com/item?id=16591918)
- [Software Testing Anti-patterns](http://blog.codepipes.com/testing/software-testing-antipatterns.html) *
- [Detecting the use of "curl | bash" server side](https://www.idontplaydarts.com/2016/04/detecting-curl-pipe-bash-server-side/)
- [Constructors Considered Mildly Confusing](http://zeekat.nl/articles/constructors-considered-mildly-confusing.html)
- [Clojure - the perfect language to expand your brain?](http://eli.thegreenplace.net/2017/clojure-the-perfect-language-to-expand-your-brain/)
- [International Journal of Proof-of-Concept or Get The Fuck Out](https://www.alchemistowl.org/pocorgtfo/)
- [Making a virtual machine in Google Sheets](https://briansteffens.github.io/2017/07/03/google-sheets-virtual-machine.html)
- [How Did Software Get So Reliable Without Proof?](http://www.gwern.net/docs/math/1996-hoare.pdf) :page_with_curl:
- [The Forgotten History of OOP](https://medium.com/javascript-scene/the-forgotten-history-of-oop-88d71b9b2d9f)
- [Meet the Flexbox Inspector](https://gedd.ski/) :sparkles:
- [A better zip bomb](https://www.bamsoftware.com/hacks/zipbomb/)
- [Race Condition vs. Data Race](https://blog.regehr.org/archives/490) :sparkles:
- [The Absolute Minimum Every Software Developer Absolutely, Positively Must Know About Unicode and Character Sets (No Excuses!)](https://www.joelonsoftware.com/2003/10/08/the-absolute-minimum-every-software-developer-absolutely-positively-must-know-about-unicode-and-character-sets-no-excuses/) :sparkles: :zap:
- [A byte’s not 8 bits.](https://burstingdynamics.wordpress.com/2015/11/10/a-byte-is-not-8-bits/) :sparkles:
- [Epigrams in programming](http://www.cs.yale.edu/homes/perlis-alan/quotes.html)
- [The Danger of “Simplicity”](https://asthasr.github.io/posts/danger-of-simplicity)
- [Front End Checklist](https://github.com/thedaviddias/Front-End-Checklist) :file_folder:
- [See Python, See Python Go, Go Python Go](https://blog.heroku.com/see_python_see_python_go_go_python_go)
- [Why stack grows down](https://gist.github.com/cpq/8598782)
- [Programmer's critique of missing structure of operating systems](http://blog.rfox.eu/en/Programmer_s_critique_of_missing_structure_of_oper.html)
- [JVM Profiler: An Open Source Tool for Tracing Distributed JVM Applications at Scale](https://eng.uber.com/jvm-profiler/)
- [Queryparser, an Open Source Tool for Parsing and Analyzing SQL](https://eng.uber.com/queryparser/)
- [Enabling Machine Learning with Apache Flink - Sherin Thomas](https://www.youtube.com/watch?v=_4lXkjqpMxI&t=12s) :tv:
- [High-Throughput, Thread-Safe, LRU Caching](https://tech.ebayinc.com/engineering/high-throughput-thread-safe-lru-caching/)
- [Sorting 1 million 8-decimal-digit numbers with 1 MB of RAM](https://stackoverflow.com/questions/12748246/sorting-1-million-8-decimal-digit-numbers-with-1-mb-of-ram)
- Null References: The Billion Dollar Mistake - Tony Hoare :tv:
- [Mathematical attack on RSA](https://www.nku.edu/~christensen/Mathematical%20attack%20on%20RSA.pdf)
- [In defence of swap: common misconceptions](https://chrisdown.name/2018/01/02/in-defence-of-swap.html)
- [The Twelve-Factor App](https://12factor.net/)
- [Epigrams on Programming](http://pu.inf.uni-tuebingen.de/users/klaeren/epigrams.html)
- [Choose Boring Technology](https://mcfunley.com/choose-boring-technology)
- [Essays on programming I think about a lot](https://www.benkuhn.net/progessays/) :sparkles:
- [PHP The Wrong Way](https://phpthewrongway.com/)
- [Laws of UX](https://lawsofux.com/)
- [How to stop procrastinating by using the Fogg Behavior Model](https://www.deprocrastination.co/blog/how-to-stop-procrastinating-by-using-the-fogg-behavior-model)
- [lzop vs compress vs gzip vs bzip2 vs lzma vs lzma2/xz benchmark, reloaded](https://stephane.lesimple.fr/blog/lzop-vs-compress-vs-gzip-vs-bzip2-vs-lzma-vs-lzma2xz-benchmark-reloaded/)
- [Andrei Pangin - Everything you wanted to know about Stack Traces and Heap Dumps](https://www.youtube.com/watch?v=FTsAXJdrJbI&t=1s) :tv:
- [The Log: What every software engineer should know about real-time data's unifying abstraction](https://engineering.linkedin.com/distributed-systems/log-what-every-software-engineer-should-know-about-real-time-datas-unifying) :sparkles: :zap:
- [The Life of a Data Byte](https://queue.acm.org/detail.cfm?id=3419941) :sparkles: :zap: :construction:
- [How To Design A Good API and Why it Matters](https://www.youtube.com/watch?v=heh4OeB9A-c) :tv:
- [The 13 immutable reads on choosing what to work on](https://vasilishynkarenka.com/13-reads-on-choosing-what-to-work-on/)
- [The Duct Tape Programmer](https://www.joelonsoftware.com/2009/09/23/the-duct-tape-programmer/)
- [The Hitchhiker’s Guide to Compression](https://go-compression.github.io/) :construction:
- [Parsing Algorithms](http://dmitrysoshnikov.com/courses/parsing-algorithms/) :construction:
- [The Differences Between Interpreter and Compiler Explained](https://thevaluable.dev/difference-between-compiler-interpreter/)
- [The Mind behind Linux](https://www.ted.com/talks/linus_torvalds_the_mind_behind_linux) :tv:
- [Semantic Versioning 2.0.0](https://semver.org/)
- [Intentionally leaking AWS keys](https://brokenco.de/2021/01/15/leaking-aws-keys.html)
- [Dream Deploys: Atomic, Zero-Downtime Deployments](https://alangrow.com/blog/dream-deploys-atomic-zero-downtime-deployments)
- [Modern Software Over-Engineering Mistakes](https://medium.com/@rdsubhas/10-modern-software-engineering-mistakes-bc67fbef4fc8)
- [Intro to Threads and Processes in Python](https://medium.com/@bfortuner/python-multithreading-vs-multiprocessing-73072ce5600b)
- [Unreliability At Scale](https://blog.dshr.org/2021/06/unreliability-at-scale.html?m=1)
- [Extreme HTTP Performance Tuning: 1.2M API req/s on a 4 vCPU EC2 Instance](https://talawah.io/blog/extreme-http-performance-tuning-one-point-two-million/)
- [Reverse Proxy, HTTP Keep-Alive Timeout, and sporadic HTTP 502s](https://iximiuz.com/en/posts/reverse-proxy-http-keep-alive-and-502s/)
- [A Solution to HTTP 502 Errors with AWS ALB](https://www.tessian.com/blog/how-to-fix-http-502-errors/)
- [DevOps, SRE, and Platform Engineering](https://iximiuz.com/en/posts/devops-sre-and-platform-engineering/)
- [Gunicorn vs Python GIL](https://luis-sena.medium.com/gunicorn-vs-python-gil-221e673d692)
- [Gunicorn Worker Types: How to choose the right one](https://dev.to/lsena/gunicorn-worker-types-how-to-choose-the-right-one-4n2c)
- [A brief description of the architecture of Gunicorn](https://docs.gunicorn.org/en/stable/design.html)
- [DESIGN PATTERNS](https://refactoring.guru/design-patterns)
- [“Don’t Mock What You Don’t Own” in 5 Minutes](https://hynek.me/articles/what-to-mock-in-5-mins/)
- [The History of Pets vs Cattle and How to Use the Analogy Properly](https://cloudscaling.com/blog/cloud-computing/the-history-of-pets-vs-cattle/)

## Fun

- https://turnoff.us
- https://xkcd.com
- https://impurepics.com/
- https://www.commitstrip.com
- [If Programming languages were harry potter characters](http://heeris.id.au/2014/if-programming-languages-were-harry-potter-characters/)
- [Git Koans](https://stevelosh.com/blog/2013/04/git-koans/)
- [Vim Kōans](https://sanctum.geek.nz/arabesque/vim-koans/)
- [The Dharma of Vi](https://blog.samwhited.com/2015/04/the-dharma-of-vi/)
- https://suricrasia.online/iceberg/
- https://goomics.net/

## More Books

### Software Development

- [Coders at Work](https://www.amazon.com/gp/product/1430219483)
- [The Pragmatic Programmer](https://www.amazon.com/Pragmatic-Programmer-Journeyman-Master/dp/020161622X) :sparkles:
- [Hackers: Heroes of the Computer Revolution](https://www.amazon.com/Hackers-Computer-Revolution-Steven-Levy/dp/1449388396)
- [The Mythical Man-Month](http://www.amazon.in/Mythical-Man-Month-Software-Engineering-Anniversary/dp/0201835959)
- [The Joy of Software Development](https://josd.captnemo.in/content/)

### Random

- [A handbook for making programming languages](http://www.craftinginterpreters.com/contents.html)
- [Ask HN: What language-agnostic programming books should I read ?](https://news.ycombinator.com/item?id=14486657)
- [The Phoenix Project: A Novel about IT, DevOps, and Helping Your Business Win](https://www.amazon.com/Phoenix-Project-DevOps-Helping-Business/dp/0988262592)
- [An Illustrated Book of Bad Arguments](https://bookofbadarguments.com/)
- [An illustrated introduction to computational thinking](https://bookofbadchoices.com/index.html#page/3)
- [Atomic Design by Brad Frost](http://atomicdesign.bradfrost.com/)
- https://begriffs.com/posts/2017-04-13-longterm-computing-reading.html
- [What is the single most influential book every programmer should read? [closed]](https://stackoverflow.com/questions/1711/what-is-the-single-most-influential-book-every-programmer-should-read) :books:
- [A Reading List For the Self-Taught Computer Scientist](https://www.reddit.com/r/books/comments/ch0wt/a_reading_list_for_the_selftaught_computer/) :books:
- [SRE Books](https://landing.google.com/sre/books/)
- https://f0.holisticinfosecforwebdevelopers.com/toc.html

## Courses

- [Operating System Engineering](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-828-operating-system-engineering-fall-2012/)
- [Introduction to Algorithms](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-006-introduction-to-algorithms-fall-2011/index.htm)
- [CS 140: Operating Systems](http://web.stanford.edu/~ouster/cgi-bin/cs140-spring14/lectures.php)
- [Awesome Courses](https://github.com/prakhar1989/awesome-courses)

## Papers

- [How Professional Hackers Understand Protected Code while Performing Attack Tasks](https://pdfs.semanticscholar.org/4bd1/2a9823b55d29a0d75c9ea9c8cd08b6fdca3e.pdf)
- [Papers We Love](https://github.com/papers-we-love) :sparkles:
- [Communicating Sequential Processes](https://spinroot.com/courses/summer/Papers/hoare_1978.pdf) :sparkles:
- [Reflections on Trusting Trust](https://users.ece.cmu.edu/~ganger/712.fall02/papers/p761-thompson.pdf)
- [Hints on programming language design](http://flint.cs.yale.edu/cs428/doc/HintsPL.pdf)
- [The Fault Tolerance of Botnets](https://www.dropbox.com/s/rvk6ybbl85zce00/The%20Fault%20Tolerance%20of%20Botnets.pdf?dl=0)
- [Paradigm Shift in Software Development](https://www.dropbox.com/s/db2tbau0jdv9pym/Paradigm%20Exercise.pdf?dl=0)
- [Cloak of Visibility](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45365.pdf)

[![Go Report Card](https://goreportcard.com/badge/github.com/hostinger/fireactions)](https://goreportcard.com/report/github.com/hostinger/fireactions)

![Banner](docs/img/banner_violet.png)

Fireactions is an orchestrator for GitHub runners. BYOM (Bring Your Own Metal) and run self-hosted GitHub runners in ephemeral, fast and secure [Firecracker](https://firecracker-microvm.github.io/) based virtual machines.

> [!IMPORTANT]
> There's been multiple improvements with a lot of breaking changes. The current stable version is **v2.0.0**. Please use this version for production environments.

<!--
https://excalidraw.com/#json=GrJMj6LLYt39mgC0me7Di,C65TV9FhicnxNKgPeRhi3A
sequenceDiagram
    autonumber
    participant Fireactions
    participant Configuration file (YAML)
    participant Pool(s)
    participant Firecracker VM with GitHub runner
    participant GitHub

    Fireactions->>Configuration file (YAML): Load pools
    Fireactions->>Pool(s): Start pool(s)
    loop Ensure min amount of GitHub runners every 1s
        Pool(s)->>GitHub: Create JIT GitHub runner token
        Pool(s)->>Firecracker VM with GitHub runner: Start Firecracker VM
        Firecracker VM with GitHub runner->>GitHub: Run GitHub workflow job
        Firecracker VM with GitHub runner->>Pool(s): Exit (on workflow job finish)
    end
    GitHub->>Fireactions: Scale pool on workflow_job event
-->
![Architecture](docs/img/architecture.png)

Several key features:

- **Scalable**

  Pool based scaling approach. Fireactions always ensures the minimum amount of GitHub runners in the pool.

- **Ephemeral**

  Each virtual machine is created from scratch and destroyed after the job is finished, no state is preserved between jobs, just like with GitHub hosted runners.

- **Customizable**

  Define job labels and customize virtual machine resources to fit Your needs.

## Quickstart
<!doctype html3>

<html3>
<tr><td><th>
<IncomeQ3>Defined By $A$3 Absolute Cell Reference "enter",123".
In Cell May Automatically Change To"$123.00".
Press Tab Or Enter Or Click Outside The Cell.
Active Cell Is Formatted For Data Or A Text.
Text"1/2/3" May Change To "01/02/2003".
Cell A20 May Contain A Formula That Produces The Result Of The Summation Of Cells A1-A25.
Cell 5 May Contain A Formula That Averages All The Numbers In The B Column.
# AAC videos "live" Or "on-the-fly".
Often Use H.264,HEVC,or VP9.
[#page:one#]--StartSwitch("-'1*");
    --End("*,-'1*);
** seqence: "*1*123*"
<=∞=><∞>
[FirebaseApp.AUTH()
[getauth()Firebaseapp][authdomain]measure ID              <ELELi "jcxml">
<icjcxml>
<title> Aeiyen My Little Word </title>
<h1>
 InputString: ("3,3")
   outputString: "3,3",
String First Line: X=F=14.8176
Implys: 1 = 14.8176.
</h1><p>
A*1+n*∅+I*J=4*1+2*∅+3*5=4+∅+15=19novacom -1
uname -a
cat/etc/OS-release
name="
version 7.1
sudo mkdir -p/opt/jdk
sudo cp -rf/home/sivasai/jdk-8u251-linux-x64.tar.gz/opt/jdk/cd/opt/jdk/sudo.tar-ZXFjdk-8u251-linux-x64.tar.gz.1s
update/jdk/jdk1.8.0_251

```bash
$ fireactions --help
BYOM (Bring Your Own Metal) and run self-hosted GitHub runners in ephemeral, fast and secure Firecracker based virtual machines.

Usage:
  fireactions [command]

Main application commands:
  server      Starts the server
  agent       Starts the agent and GitHub Actions runner inside the VM

Pool management commands:
  pools       Manage pools

Machine management commands:
  ps          List all running machines across all pools
  login       SSH into a running VM as root user
  logs        Stream logs from the fireactions-agent service inside a machine

Image management commands:
  image       Manage images

Additional Commands:
  version     Show version information
  help        Help about any command
  completion  Generate the autocompletion script for the specified shell

Flags:
  -h, --help      help for fireactions
  -v, --version   version for fireactions

Use "fireactions [command] --help" for more information about a command.
```

See the [User Guide](https://fireactions.io/latest/) for installation and configuration instructions.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for more information on how to contribute to Fireactions.

## License

See [LICENSE](LICENSE)

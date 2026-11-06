# Setup guide
1. Clone modular repo in your preferred folder on the machine:

```bash
### Linux/MacOS ###

# Using HTTPS (recommended for most users)
git clone https://github.com/TheOpenSI/cosmic-db.git
git clone https://github.com/TheOpenSI/cosmic-core.git
git clone https://github.com/TheOpenSI/cosmic-auth.git
git clone https://github.com/TheOpenSI/cosmic-platform.git
git clone https://github.com/TheOpenSI/cosmic-docker.git

# Using SSH (recommended if you've SSH keys configured)
git clone git@github.com:TheOpenSI/cosmic-db.git
git clone git@github.com:TheOpenSI/cosmic-core.git
git clone git@github.com:TheOpenSI/cosmic-auth.git
git clone git@github.com:TheOpenSI/cosmic-platform.git
git clone git@github.com:TheOpenSI/cosmic-docker.git
```

```ps1
### Windows ###

# Using HTTPS (recommended for most users)
git clone https://github.com/TheOpenSI/cosmic-db.git
git clone https://github.com/TheOpenSI/cosmic-core.git
git clone https://github.com/TheOpenSI/cosmic-auth.git
git clone https://github.com/TheOpenSI/cosmic-platform.git
git clone https://github.com/TheOpenSI/cosmic-docker.git


# Using SSH (recommended if you've SSH keys configured)
git clone git@github.com:TheOpenSI/cosmic-db.git
git clone git@github.com:TheOpenSI/cosmic-core.git
git clone git@github.com:TheOpenSI/cosmic-auth.git
git clone git@github.com:TheOpenSI/cosmic-platform.git
git clone git@github.com:TheOpenSI/cosmic-docker.git
```

2. Follow setup instructions in each repo (except part that build the compose file):

- [`cosmic-db` README.md](https://github.com/TheOpenSI/cosmic-db/blob/main/README.md)
- [`cosmic-core` README.md](https://github.com/TheOpenSI/cosmic-core/blob/main/README.md)
- [`cosmic-auth` README.md](https://github.com/TheOpenSI/cosmic-auth/blob/main/README.md)
- [`cosmic-platform` README.md](https://github.com/TheOpenSI/cosmic-platform/blob/main/README.md)

3. Spin up the unified compose file

> [!NOTE]
> It's possible to run Docker in rootless mode on Linux. However, the way to set
> it up is different on each Linux distros. Please refer to [this](https://docs.docker.com/engine/install) and [this](https://docs.docker.com/engine/security/rootless/)
> (all sourced from Docker documentation) to choose the one that fits for your
> current Linux distro.

```bash
# Linux/MacOS
docker compose up --build -d # Refer to NOTE if running on rootless mode
```

```ps1
# Windows
docker compose up --build -d # Docker run through lightweight Linux VM on Windows so it's rootless by default
```

**The build process will take a while to fully up depending on your internet connection.**

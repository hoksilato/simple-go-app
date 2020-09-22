## Install Go with Homebrew

```
brew install Go
```

## Export paths

Export some paths, and save them in your `.zshrc` or `.bashrc`

```
# Go
export GOPATH=$HOME/src/go
export GOROOT="$(brew --prefix golang)/libexec"
export PATH=$PATH:$GOPATH/bin:$GOROOT/bin
```

Create `go` folder if it doesn't exist

```
test -d "${GOPATH}" || mkdir "${GOPATH}"
```

Create required folders in `GOPATH`

```
mkdir -p $GOPATH $GOPATH/src $GOPATH/pkg $GOPATH/bin
```

## Install go packages

```
go get github.com/go-chi/chi
```

## How to run

Clone this repo

```
cd $GOPATH/src
git clone git@github.com:hoksilato/simple-go-app.git
```

### Option 1:

```
go run main.go
```

Now you can visit `http://localhost:8080/api/jobs`.

### Option 2: 

Build binary file then execute it

```
go build -o jobs
chmod +x jobs
./jobs
```

Now you can visit `http://localhost:8080/api/jobs`.

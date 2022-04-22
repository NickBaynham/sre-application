# Python Microservices - Example 1 (Basic Example)

```
virtualenv dev1
source dev1/bin/activate
pip3 install py-ms[all]
python main.py
```

# Build the Container

```
docker build . -t nbaynhamdevops/example1
```
# Run the application in the container
```
docker run --rm -p 3000:3000 example1
```

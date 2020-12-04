# Mac container

```
docker build -f ./Dockerfile -t jsm174/unityci:2020.2.0b14-mac-mono . --build-arg version=2020.2.0b14 --build-arg changeSet=dc0b50340a64 --build-arg module=mac-mono
docker push jsm174/unityci:2020.2.0b14-mac-mono
```

# Windows container

```
docker build -f ./Dockerfile -t jsm174/unityci:2020.2.0b14-windows-mono . --build-arg version=2020.2.0b14 --build-arg changeSet=dc0b50340a64 --build-arg module=windows-mono
docker push jsm174/unityci:2020.2.0b14-windows-mono
```

# Running locally

```
docker run -it --rm --mount type=bind,source=/Users/jmillard/Documents/vpe,target=/vpe jsm174/unityci:2020.2.0b14-mac
```

# Add license in container

```
mkdir -p /root/.local/share/unity3d/Unity
cp /vpe/Unity_lic.ulf /root/.local/share/unity3d/Unity
```

# Notes

Dockerfiles based on https://github.com/Unity-CI/docker/blob/main/editor/Dockerfile

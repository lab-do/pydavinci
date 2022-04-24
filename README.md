<h1 align='center'>pydavinci</h1>

<p align='center'>A lightly opinionated DaVinci Resolve Python API wrapper</p>

<p align='center'>Provides auto completion, type hints and great API reference documentation.</p>

<p align='center'><sup><i align='center'>I really just wanted auto completion in the IDE and to program transcoding RAW formats</i></sup></p>


---

pydavinci __only works with `Python 3.6.*`__, as that's a requirement on DaVinci Resolve's part. You also need the __Studio__ version.


For the newer DaVinci Resolve v18, currently in beta, newer Python installations are supported.


### Install pydavinci

Install via pip using a __Python 3.6__ environment

```bash
pip install pydavinci

```
Then make sure external scripting is set to `Local` in Settings -> System -> General
<p align='center'>
<img src=https://user-images.githubusercontent.com/4316044/164954498-de350d02-0458-478d-a766-6404b7a8a75b.png />
</p>

Now we just need to import it!

```python
from pydavinci import davinci

resolve = davinci.Resolve()
```

- Check out the usage [examples](https://pedrolabonia.github.io/pydavinci/examples/premiereproxies/)
- Or go deep in the [documentation](https://pedrolabonia.github.io/pydavinci/resolve/)

---

## To-do and contributing

Contributors are always welcome! I currently have a few things I want to change, some of them are:
- [ ] Document all possible values of `get_setting` and `set_setting`
- [ ] Add a better way of interfacing with the whole `get_setting` and `set_setting` methods using a proxy class or something to that effect
- [ ] Create a Marker class to inherit from for the objects that need it
- [ ] Auto launch Resolve when it's not open - I've ran into some issues while trying to connect to the C extension right after launching it, a dirty way to do it is to just implement a `time.sleep` before trying to import the fusionscript module, otherwise we'll need to create another entrypoint to the api for launching the process and then signaling when it's ready 

#### If you want to contribute feel free to open a pull request!
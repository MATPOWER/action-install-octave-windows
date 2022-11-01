Install Octave (Windows)
========================

### GitHub Action to install [GNU Octave][1] on Windows

Installs [GNU Octave][1] on Windows runners and sets the following environment
variables.
- `OCTAVE_VER` set to the version of [Octave][1] installed
- `ML_NAME` set to `Octave`
- `ML_VER` set to same as `OCTAVE_VER`
- `ML_CMD` set to `octave-cli.exe --no-gui --eval`
- `ML_PATHVAR` set to `OCTAVE_PATH`

### Inputs / Outputs

None.

### Example Usage
```
    defaults:
      run:
        shell: bash
    steps:
    - name: Install Octave
      uses: MATPOWER/action-install-octave-windows@v1

    - name: Octave ${{ env.ML_VER }} Installed
      run: $ML_CMD ver
```

[1]: https://octave.org

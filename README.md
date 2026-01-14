# Demosphere

Demosphere is a modification based on Atmosphere, designed to enable Nintendo Switch Demo units to function like retail units. This patch allows Demo units to operate similarly to standard retail consoles by applying specific changes to the Atmosphere custom firmware.

## Usage

To use Demosphere, follow these steps:

1. Clone the original Atmosphere repository:
   ```
   git clone https://github.com/Atmosphere-NX/Atmosphere.git
   cd Atmosphere
   ```

2. Apply the patch provided in this repository:
   ```
   git apply ../demo.diff
   ```

3. Compile the modified Atmosphere project using Docker:
   ```
   docker run --rm -v $(pwd):/data devkitpro/devkita64:20251231 bash -c "cd /data/ && make"
   ```

## Important Notes

After recompiling Atmosphere with this patch, the load patches in commercially available Sigpatches will become ineffective. You will need to create your own Sigpatch configuration to ensure compatibility.

You may occasionally find pre-compiled and packaged versions in the [Releases](https://github.com/tatanakots/Demosphere/releases), but please do not expect me to upload the latest pre-compiled packages promptly.
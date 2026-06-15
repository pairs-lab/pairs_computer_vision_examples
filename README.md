# PAIRS Computer Vision Examples

Worked, runnable examples showing how to do camera and image processing inside the PAIRS UAV stack. Each example is a small ROS package that subscribes to a UAV camera, runs an OpenCV algorithm, and republishes the result, so you can copy it as a starting point for your own vision nodes. Both examples are meant to be flown in the PAIRS Gazebo simulation.

## Contents

- [cpp/edge_detector](./cpp/edge_detector) — `pairs_example_edge_detector`: a C++ nodelet (`pairs_example_edge_detector/EdgeDetector`) demonstrating ImageTransport I/O, OpenCV Canny edge detection, the pinhole camera model, and TF2 point transforms. It is the more comprehensive template, with extensive notes on image-processing coding practices.
- [python/blob_detector](./python/blob_detector) — `pairs_example_blob_detector`: a compact Python node demonstrating OpenCV blob detection on a camera stream.

## Install (ROS 1 Noetic)

```bash
sudo apt install ros-noetic-pairs-example-edge-detector
sudo apt install ros-noetic-pairs-example-blob-detector
```

## Usage

Each example ships its own simulation session. From the example directory:

```bash
# C++ edge detector
cd cpp/edge_detector && ./tmux/start.sh

# Python blob detector
cd python/blob_detector && ./tmux/start.sh
```

You can also launch a single node directly, e.g.:

```bash
roslaunch pairs_example_edge_detector edge_detector.launch
roslaunch pairs_example_blob_detector blob_detector.launch
```

# Disclaimer

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

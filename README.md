# Cap'n Proto vs Flatbuffers

In order for our customers to be happy with performance Advertima's software works we have to ensure, apart other stuff,
that data transmitted between a PoI and a client flows as fast as possible.

To achieve these we have to ensure that each message sent from PoI to a client:
1. has the least size possible
2. requires as few RAM for serialization/deserialization routine as possible
3. requires as few CPU cycles for serialization/deserialization routine as possible

1. RAM used for serialization/deserialization
2. time used to serialize a JSON object
3. time used to deserialize a binary object to JSON
4. binary packet size

## Prerequisites

1. install CMake via your package manager
2. install [pnpm](https://pnpm.js.org/en/installation)

### Build Flatbuffers

1. from the project directory run `./.bin/build-flatbuffers`
2. from the project directory run `./.bin/install-deps`

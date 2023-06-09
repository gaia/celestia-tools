# Celestia Tools

This repo will focus on tooling built for the [Celestia Network](https://github.com/celestiaorg/), but whenever possible, it will be made compatible with any chain based on the [Cosmos SDK](https://github.com/cosmos/cosmos-sdk)

![Celestia network logo](https://avatars.githubusercontent.com/u/54859940?s=200&v=4 'Celestia network') ![FreshSTAKING logo](https://pbs.twimg.com/profile_images/1539316263314370560/syHanQz4_200x200.jpg 'FreshSTAKING')

# Tools

# 1) parse-output.sh

appending `| ./parse-output.sh` to a TX-generating celestia-appd command will **strip out unnecessary output, pick and highlight the relevant messages (errors or results), and streamline checking for a success/fail of the TX after it has been included in the block**. It has three possible outcomes:

a) command wasn't accepted (along with the reason why, stripping out any irrelevant information)

b) command was accepted and broadcasted to the network but not indexed (usually a temporary error, and the scripts gives up after 3 attemtps to find it indexed)

c) command was accepted, broadcasted to the network and indexed, and the result was success or fail (in which case the reason and only the reason why is displayed, stripping out any irrelevant information).

# 2) peer-info.sh

Bash script to show a daemon's peers, in the format ID@IP:port, followed by whether the peer is outbound or inbound, along with the peer's city according to an API query to an IP location service.

# 3) peer-paste.sh

Bash script to parse the output of an RPC's peerlist into a format ready to paste in persistent peers.

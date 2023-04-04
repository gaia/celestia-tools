# Celestia Tools

This repo will focus on tooling built for the [Celestia Network](https://github.com/celestiaorg/), but whenever possible, it will be made compatible with any chain based on the [Cosmos SDK](https://github.com/cosmos/cosmos-sdk)

![Celestia network logo](https://avatars.githubusercontent.com/u/54859940?s=200&v=4 'Celestia network')
# &
![FreshSTAKING logo](https://pbs.twimg.com/profile_images/1539316263314370560/syHanQz4_200x200.jpg 'FreshSTAKING')

# Description

- parse-output.sh: appending

`| ./parse-output.sh`

to a TX-generating celestia-appd command will **strip out unnecessary output, pick and highlight the relevant messages (errors or results), and streamline checking for a success/fail of the TX after it has been included in the block**. It has three possible outcomes:

a) command wasn't accepted (along with the reason why, stripping out any irrelevant information)

b) command was accepted and broadcasted to the network but not indexed (usually a temporary error, and the scripts gives up after 3 attemtps to find it indexed)

c) command was accepted, broadcasted to the network and indexed, and the result was success or fail (in which case the reason and only the reason why is displayed, stripping out any irrelevant information).

# deploy-l2-with-optimism
Learn how to run your own Optimism-based Layer-2 Rollup. This repository provides a detailed, step-by-step guide to setting up, configuring, and operating your own L2 rollup using the Optimism OP Stack. Perfect for builders and researchers who want a deeper understanding of rollup infrastructure.

## Step 1: Clone optimism monorepo

## Step 2: use `make op-node op-batcher op-proposer`

OP Stack system is broken into 2 key components:
1. op-node: which serves as the consensus client
2. then there's another node that serves as the execution client 

Now there are actually multiple implementation of this: 
Right now we have 2 implementations of the consensus client:
- op node 
- Magi

Then we have 2 execution client options:
- op-geth
- op-aragon

Right now, we are going to use op-node and op-geth

Then there is another thing called as Batcher and the Proposer. 

- Batcher is a process that talks to the sequencer node and its all the data from the sequencer and puts it on L1.
- Proposer proposes what the output of the L2 is to the main bridge - which allows usesr to then withdraw funds from the main bridge. 

## Step 3: yarn install in optimism

## Step 4: git clone https://github.com/ethereum-optimism/op-geth.git
then cd op-geth
and run:
> make geth

## Step 5: inside optimism folder
cd packages/contracts-bedrock

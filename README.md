# Efficient Control-Channel Security for the Aeronautical Communications System LDACS

The contribution of this paper is the formal proof of the security of this protocol. Using the symbolic model checker Tamarin, we could build a mathematical, formal model of the LDACS MAKE procedure and following several security objectives that this procedure must fulfill, we derived several provable lemmata for Tamarin. Tamarin finally proved that the LDACS MAKE procedure is secure in the standard model and is proven to have no design flaws in its architecture.
This constitutes an important step for the development of the general LDACS cybersecurity architecture since authentication and key establishment are the most crucial steps in establishing secure wireless communication.

## Authors: 

Nils Mäurer, Thomas Gräupl (Institute of Communications and Navigation, German Aerospace Center)
Corinna Schmitt (Esearch Institute CODE, Universität der Bundeswehr München)

## **Paper**

- Submission to the 2nd Workshop on Secure and Reliable Communication and Navigation in the Aerospace (SRCNAS)
  Co-located with the 24th IEEE International Symposium on a World of Wireless, Mobile and Multimedia Networks (WoWMoM)

## **File structure:**

- `ldacs_iso_3-pass_preq_a_proof.spthy`
  - contains a formal analysis of the proposed LDACS cell-attachment based on elliptic curve diffie-hellman
- `ldacs_iso_3-pass_pqc_a_proof.spthy`
  - contains a formal analysis of the proposed LDACS cell-attachment based on a PQ key transport scheme


## The Tamarin prover repository

For installation and usage instructions of the Tamarin prover see chapter 2 of the manual:

https://tamarin-prover.github.io/manual/book/002_installation.html

## Build environment

Tamarin prover: v1.6.1

OS: Linux based Ubuntu 20.04

Configuration: MD Ryzen 7 3700X 8-Core CPU and 32 GB RAM

Verification time: ~30 s - 1 min


## Output

==============================================================================
summary of summaries:

analyzed: ldacs_iso_3-pass_preq_a_proof.spthy

  exists_session_a (exists-trace): verified (32 steps)
  mutual_authentication_A (all-traces): verified (72 steps)
  mutual_authentication_B (all-traces): verified (72 steps)
  session_uniqueness_A (all-traces): verified (38 steps)
  session_uniqueness_B (all-traces): verified (38 steps)
  secrecy (all-traces): verified (146 steps)
  secrecy_pfs (all-traces): verified (146 steps)
  key_consistency_A (all-traces): verified (1138 steps)
  key_consistency_B (all-traces): verified (1138 steps)
  
  
==============================================================================
summary of summaries:

analyzed: ldacs_iso_3-pass_pqc_a_proof.spthy

  exists_session_a (exists-trace): verified (32 steps)
  mutual_authentication_A (all-traces): verified (84 steps)
  mutual_authentication_B (all-traces): verified (84 steps)
  session_uniqueness_A (all-traces): verified (38 steps)
  session_uniqueness_B (all-traces): verified (38 steps)
  secrecy (all-traces): verified (122 steps)
  secrecy_pfs (all-traces): verified (122 steps)
  key_consistency_A (all-traces): verified (1066 steps)
  key_consistency_B (all-traces): verified (1066 steps)



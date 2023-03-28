# Secure Multi-Party Computation (MPC)

![](https://badgen.net/badge/:update-to/:Mar-2023/red) ![](https://badgen.net/badge/:papers/:28/blue) 

> "The design of scure protocols that implement arbitrarily desired functionalities is a major part of mordern cryptography."
> -- Foundation of Cryptography, Volumn 2, Oded Goldreich. 

MPC has evolved from a theoretical curiosity in the 1980s to a tool for building real systems today. Over the past decade, MPC has been one of the most active research areas in both theoretical and applied cryptography. In the following, we try to show the newest and interesting advances in mpc (both theory & applicaiton), and also the infulential papers in history. 

Note: one paper may be included in several categories (e.g. a paper may introduce a new protocol for both OT and VOLE, we decide to include it in both categories).

## Table of Contents

- [offline-techniques](#offline-techniques)
  * [ot](#oblivious-transfer) : oblivious transfer
  * [vole](#vector-oblivious-linear-evaluation): (subfield) (vector) oblivious linear evaluation
  * [oprf](#oblivious-pseudo-random-function): oblivious pseudorandom function
  * [pcg](#pseudorandom-correlation-generator): pseudorandom correlation generator
- [online-techniques](#online-techniques)
  * [secret sharing](#secret-sharing)
  * [garbled-circuit](#garbled-circuit)

## Offline Techniques

### Oblivious transfer

- SoftSpokenOT: Quieter OT Extension from Small-Field Silent VOLE in the Minicrypt Model  
  *Lawrence Roy*  
  Crypto 2022, [publisher](https://www.iacr.org/cryptodb//data/paper.php?pubkey=32258), Roy22

- Silver: Silent VOLE and Oblivious Transfer from Hardness of Decoding Structured LDPC Codes  
  *Geoffroy Couteau, Peter Rindal, Srinivasan Raghuraman*  
  Crypto 2021, [eprint](https://eprint.iacr.org/2021/1150), CRR21

- The Rise of Paillier: Homomorphic Secret Sharing and Public-Key Silent OT  
  *Claudio Orlandi, Peter Scholl, Sophia Yakoubov*  
  EuroCrypt 2021, [eprint](https://eprint.iacr.org/2021/262), OSY21

- Batching Base Oblivious Transfers  
  *Ian McQuoid, Mike Rosulek, Lawrence Roy*  
  AsiaCrypt 2021, [eprint](https://eprint.iacr.org/2021/682), MRR21

- Efficient Two-Round OT Extension and Silent Non-Interactive Secure Computation  
  *Elette Boyle, Geoffroy Couteau, Niv Gilboa, Yuval Ishai, Lisa Kohl, Peter Rindal, Peter Scholl*  
  CCS 2019, [eprint](https://eprint.iacr.org/2019/1159), BCGI+19 (with Peter Rindal)
  
- Endemic Oblivious Transfer  
  *Daniel Masny, Peter Rindal*  
  CCS 2019, [eprint](https://eprint.iacr.org/2019/706), MR19 
  
- Efficient Pseudorandom Correlation Generators: Silent OT Extension and More  
  *Elette Boyle, Geoffroy Couteau, Niv Gilboa, Yuval Ishai, Lisa Kohl, Peter Scholl*  
  Crypto 2019, [eprint](https://eprint.iacr.org/2019/448), BCGI+19 (without Peter Rindal)

- Actively Secure 1-out-of-N OT Extension with Application to Private Set Intersection  
  *Michele Orrù, Emmanuela Orsini, Peter Scholl*  
  CT-RSA 2017, [eprint](https://eprint.iacr.org/2016/933), OOS17

- Actively Secure OT Extension with Optimal Overhead  
  *Marcel Keller, Emmanuela Orsini, Peter Scholl*  
  Crypto 2015, [eprint](https://eprint.iacr.org/2015/546), KOS15
  
- The Simplest Protocol for Oblivious Transfer  
  *Tung Chou, Claudio Orlandi*  
  LatinCrypt 2015, [eprint](https://eprint.iacr.org/2015/267), CO15
  
- More Efficient Oblivious Transfer and Extensions for Faster Secure Computation  
  *Gilad Asharov, Yehuda Lindell, Thomas Schneider, Michael Zohner*  
  CCS 2013, [eprint](https://eprint.iacr.org/2013/552), ALSZ13
  
- Extending Oblivious Transfers Efficiently  
  *Yuval Ishai, Joe Kilian, Kobbi Nissim, Erez Petrank*  
  Crypto 2003, [eprint](https://www.iacr.org/archive/crypto2003/27290145/27290145.pdf), IKNP03

- Oblivious Transfer and Polynomial Evaluation  
  *Moni Naor, Benny Pinkas*  
  STOC 1999, [eprint](https://dl.acm.org/doi/pdf/10.1145/301250.301312), NP99

### vector Oblivious Linear Evaluation

- Two-Round Oblivious Linear Evaluation from Learning with Errors  
	*Pedro Branco, Nico Do ̈ttling, Paulo Mateus*  
	PKC 2022, [eprint](https://eprint.iacr.org/2020/635), BDM22

- Correlated Pseudorandomness from Expand-Accumulate Codes  
	*Elette Boyle, Geoffroy Couteau, Niv Gilboa, Yuval Ishai, Lisa Kohl, Nicolas Resch, Peter Scholl*  
	Crypto 2022, [eprint](https://eprint.iacr.org/2022/1014), BCG+22
	
- Silver: Silent VOLE and Oblivious Transfer from Hardness of Decoding Structured LDPC Codes  
  *Geoffroy Couteau, Peter Rindal, Srinivasan Raghuraman*  
  Crypto 2021, [eprint](https://eprint.iacr.org/2021/1150), CRR21
  
- Two-Round Oblivious Linear Evaluation from Learning with Errors  
  *Pedro Branco, Nico Döttling, Paulo Mateus*  
  PKC 2022, [eprint](https://eprint.iacr.org/2020/635), BDM20
  
- Efficient Protocols for Oblivious Linear Function Evaluation from Ring-LWE  
  *Carsten Baum, Daniel Escudero, Alberto Pedrouzo-Ulloa, Peter Scholl, Juan Ramón Troncoso-Pastoriza*  
  SCN 2020, [eprint](https://eprint.iacr.org/2020/970), BEPS+20
  
- Distributed vector-OLE: Improved constructions and implementation  
  *Phillipp Schoppmann, Adrià Gascón, Leonie Reichert, Mariana Raykova*  
  CCS 2019, [eprint](https://eprint.iacr.org/2019/1084), SGRR19
  
- Compressing vector OLE  
  *Elette Boyle, Geoffroy Couteau, Niv Gilboa, Yuval Ishai*  
  CCS 2018, [eprint](https://eprint.iacr.org/2019/273), BCGI18
  
- Maliciously secure oblivious linear function evaluation with constant overhead  
  *Satrajit Ghosh, Jesper Buus Nielsen, Tobias Nilges*  
  AsiaCrypt 2017, [eprint](https://eprint.iacr.org/2017/409), GNN17
  
- TinyOLE: Efficient actively secure two-party computation from oblivious linear function evaluation, 2017,   
  *Nico Döttling, Satrajit Ghosh, Jesper Buus Nielsen, Tobias Nilges, Roberto Trifiletti*  
  CCS 2017, [eprint](https://eprint.iacr.org/2017/790), DGNN+17
  
- Oblivious Transfer and Polynomial Evaluation  
  *Moni Naor, Benny Pinkas*  
  STOC 1999, [eprint](https://dl.acm.org/doi/pdf/10.1145/301250.301312), NP99
  
### Oblivious Pseudo-Random Function

### Pseudorandom-Correlation Generator

- Correlated Pseudorandomness from Expand-Accumulate Codes  
  *Elette Boyle, Geoffroy Couteau, Niv Gilboa, Yuval Ishai, Lisa Kohl, Nicolas Resch, Peter Scholl*  
  Crypto 2022, [eprint](https://eprint.iacr.org/2022/1014), BCG+22

## Online Techniques

### Secret Sharing

- The Round Complexity of Secure Protocols  
  *Donald Beaver, Silvio Micali, Phillip Rogaway*  
  STOC 1990, [eprint](http://web.cs.ucdavis.edu/~rogaway/papers/bmr90), BMR90
  
- Completeness Theorems for Non-Cryptographic Fault Tolerant Distributed Computation  
  *Michael Ben-Or, Shafi Goldwasser, Avi Wigderson*  
  STOC 1988, [eprint](https://dl.acm.org/doi/10.1145/62212.62213), BGW88

- How to play any mental game?  
  *Oded Goldreich, Silvio Micali, Avi Wigderson*  
  STOC 1987, [eprint](https://dl.acm.org/doi/10.1145/28395.28420), GMW87
  
- How to generate and exchange secrets?  
  *Andrew Chi-Chih Yao*  
  FOCS 1986, [eprint](https://ieeexplore.ieee.org/document/4568207), Yao86

### Garbled Circuit



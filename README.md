ML-MessagePack
==============

MessagePack implementation for Standard ML (SML)

Features
--------

- Portable: Depends only on the required components of the SML Basis Library specification.
- Composable: Encoder and decoder are composable by combinators.

Usage
-----

#### MLton and MLKit

Include mlmsgpack.mlb in your MLB file.

#### Poly/ML

From the interactive shell, use .sml files in the following order.

- mlmsgpack-aux.sml
- realprinter-default.sml
- mlmsgpack.sml

#### SML/NJ

Use mlmsgpack.cm.

#### Moscow ML

First, you need LargeInt and LargeWord structures. The definition below will do.

    structure LargeInt = Int
    structure LargeWord = Word

Then, use .sml files in the following order.

- mlmsgpack-aux.sml
- realprinter-fail.sml
- mlmsgpack.sml

#### Alice ML

From the interactive shell, use .sml files in the following order.

- mlmsgpack-aux.sml
- realprinter-fail.sml
- mlmsgpack.sml

#### SML#

.smi files are provided. Require mlmsgpack.smi from your .smi file.

Known Problems
--------------

Our recommendation is MLton, MLKit and Poly/ML. Moscow ML is also fine if you don't use real values.

#### SML/NJ

Packing real values produces imprecise results in some situations.

#### Moscow ML

Packing real values is not supported, since some components of the SML Basis Library are not provided.

#### Alice ML

Packing real values is not supported, since some components of the SML Basis Library are not provided.
Also, some unit tests fail.

#### SML#

Several functions do not work properly because of bugs of SML#.

Status
------

Not complete.

See Also
--------

There already exists another MessagePack implemenatation for SML, 
called MsgPack-SML, which is targeted for Mlton.

https://msgpacksml.codeplex.com/

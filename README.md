# Orogen-Plugin for serialization

## Description
This package installs an Orogen-Plugin which allows to automatically generate opaque types for complex class objects. With this it is possible to serialize them to send and receive via ports of Orogen-Tasks.

## Details
Generates an opaque conversion for the given type. It registers a wrapper type based on the selected serialization method and generates the conversion between the opaque type and its wrapper type.

The following options are available: 
* +:include+ and +:includes+ are used to include the headers of the opaque type.
* +:type+ selects the serialization type, default is +:boost_serialization+

Serialization types:
* +:boost_serialization+ the opaque type must support boost serialization. It is used to store the internal data of the opaque in binary form.

## Example
    opaque_autogen '/gridmaps/Grid2D',
                   :includes => "gridmaps/Grid2D.hpp",
                   :type => :boost_serialization


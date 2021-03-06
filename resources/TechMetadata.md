# Technical Metadata
  * I'm working for the definitions put forth in the Understanding Metadata, by Jenn Riley (NISO, 2017)
  * There are a lot of definitions out there and the lines can blur between types.
  * I'm considering Administrative Data to be a sort of umbrella
    * Technical Metadata  - Decoding and rendering files
    * Preservation Metadata - Long-term management of files
    * Rights Metadata - Intellectual property rights attached to content.
  * Technical Metadata
    * Characteristics
      * Often embedded in the file
      * Tends to be information for the computer to "understand" the file(s)
      * May be used by repo managers to evaluate digital objects (creation date, file formats, hardware/software)
      * Important for interoperability, digital object management, and preservation
    * Example properties
      * File type
      * File size
      * Creation date/time
      * Compression scheme
      * Hardware and software used to acquire the digital object
      * Resolution
      * Color profiles
    * Tools
      * Tools like JHOVE, EXIF, DROID, etc can identify, extract, and/or validate Tech Metadata
      * FITS (File Information Tool Set) is a tool that wraps a lot of these tools together.
      * FITS can also transform the data from these tools into existing
    * Common standards/Schema
      * FITS XML (wrapper XML file that also contains core technical metadata fields)
        * Identification (file format in one or more identity blocks)
        * File Information (basic technical metadata that isn't specific to any format)
        * File Status (validity information)
        * Metadata (each tool's native output that has been normalized and consolidated by FITS)
        * Tool Output (configurable - this section contains the output from each tool that ran against the file)
        * Statistics (records how much time each wrapped tool spent processing the file)
      * MIX (NISO Metadata for images in XML)
      * TextMD
      * AES Audio Object
      * DocumentMD
      * EBUCore
      * ContainerMD

# BBTools - OFFICIAL REPOSITORY

**⚠️ THIS IS THE OFFICIAL BBTools REPOSITORY maintained by Brian Bushnell ⚠️**

**Not to be confused with unofficial/outdated mirrors. This is the authoritative source.**

**BBTools** is a suite of fast, multithreaded bioinformatics tools designed for analysis of DNA and RNA sequence data. BBTools can handle common sequencing file formats such as fastq, fasta, sam, scarf, fasta+qual, compressed files, and text files containing one sequence per line.

## 🚀 Features

- **High Performance**: Multithreaded, efficient memory usage, and optimized algorithms
- **Comprehensive Suite**: Over 90 tools for various bioinformatics tasks
- **Format Flexibility**: Handles multiple file formats and automatic format detection
- **Platform Independent**: Pure Java implementation runs on any system with Java 8+
- **Production Ready**: Battle-tested at JGI and used in thousands of publications

## 📦 Main Components

### Core Tools (Most Popular)
- **BBMap**: Short read aligner for DNA and RNA-seq data
- **BBDuk**: Adapter trimming, quality filtering, and contaminant removal  
- **BBMerge**: Paired read merging with error correction
- **BBNorm**: Error correction and normalization
- **Tadpole**: Fast assembler for small genomes or metagenomes
- **Clumpify**: Reorder reads to maximize compression and speed up analysis
- **CallVariants**: Variant calling from aligned reads
- **BBCMS**: Error correction via conditional median filtering

### Quality Control
- **BBDuk**: Quality trimming and adapter removal
- **BBSplit**: Binning reads by mapping to multiple references
- **Clumpify**: Reorder reads to maximize compression

### Assembly Tools
- **Tadpole**: Extremely fast micro-assembler
- **BBTools Assembly Pipeline**: Complete assembly workflow

### Sketch Tools
- **SendSketch**: Identify contaminants and organisms
- **CompareSketch**: Compare sketches for similarity

## 🔧 Installation

### Quick Start
```bash
# Download the latest version
wget https://sourceforge.net/projects/bbmap/files/latest/download -O BBTools.tar.gz
tar -xzf BBTools.tar.gz
cd bbmap

# Test installation
./bbduk.sh --version
```

### Requirements
- Java 8 or higher (Java 14+ recommended)
- 4GB RAM minimum (more for large datasets)

## 📖 Documentation

Comprehensive documentation is available in the `/docs` directory:
- `readme.txt` - General information
- `UsageGuide.txt` - Detailed usage instructions
- `ToolDescriptions.txt` - Description of all tools

## 💻 Usage Examples

### Adapter Trimming
```bash
bbduk.sh in=reads.fq out=clean.fq ref=adapters.fa ktrim=r k=23 mink=11 hdist=1 tpe tbo
```

### Read Mapping
```bash
bbmap.sh ref=reference.fasta in=reads.fq out=mapped.sam
```

### Error Correction
```bash
tadpole.sh in=reads.fq out=corrected.fq mode=correct
```

## 🤝 Contributing

We welcome contributions! Please see our contributing guidelines (coming soon).

## 📄 License

BBTools is free for academic and non-profit use. See `license.txt` for details.

## 📚 Citation

If you use BBTools in your research, please cite:
```
BBTools: a suite of fast, multithreaded bioinformatics tools designed for 
analysis of DNA and RNA sequence data. Brian Bushnell.
Official Repository: https://github.com/bbushnell/BBTools
SourceForge: https://sourceforge.net/projects/bbmap/
```

**Note:** Please use this official repository, not outdated third-party mirrors.

## 🔗 Links

- **Official Website**: [bbtools.org](https://bbtools.org) (coming soon)
- **SourceForge**: [sourceforge.net/projects/bbmap](https://sourceforge.net/projects/bbmap/)
- **Support Forum**: [JGI BBTools Forum](https://jgi.doe.gov/data-and-tools/software-tools/bbtools/)

## 👥 Authors

- **Brian Bushnell** - Primary Developer
- **Jon Rood** - Contributor
- **Shijie Yao** - Contributor

## 📊 Version

Current Version: **39.34**

---

*BBTools is developed at the Joint Genome Institute (JGI) and Lawrence Berkeley National Laboratory (LBNL)*

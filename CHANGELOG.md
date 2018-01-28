## [2.5.2] - 2018-01-29
### Added
- Rewritten rf-fold engine to make it faster (and to make code maintenance easier)
- Fixed an issue in rf-fold causing a crash when no reactivity data was available for a given pseudoknotted helix
- Fixed a bug in rf-fold causing the software to report unfolded structures for RNAs with length < than the allowed minimum window length (50 nt) in windowed folding mode
- Introduced in rf-fold the generation of SVG graphical summaries (reactivity data, Shannon entropy, base-pairing probabilities and MEA structure)

### API changes
- Data::IO::XML has been replaced by a Data::XML class for XML construction, that is then passed to a generic Data::IO object for writing
- Introduced Graphics libraries for SVG graphics generation (currently supports bar plots, paths, and RNA arc plots)

## [2.5.1] - 2018-01-07
### Added
- Introduced CHANGELOG
- Added back support for Siegfried *et al*., 2014 normalzation method (now the method allows also the analysis of experiments lacking a denatured sample)

## [2.5.0] - 2018-01-05
### Added
- Introduced support for pseudoknots
- Introduced rf-jackknife for slope/intercept grid search
- Changed RC format (from now on backward compatibility is supported, but RC files created before this release are no longer supported)
- rf-peakcall now supports the analysis of experiments lacking control/input sample

### Removed
- Temporarily removed Siegfried *et al*., 2014 normalzation method support
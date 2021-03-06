A command-line composers tool for exploring diatonic music via musical set theory.

By defining groups of notes by their 'prime form' (see: http://composertools.com/Theory/PCSets/PCSets3.htm), we can efficiently classify them and list related musical objects.

## Usage:
    python -i sample.py
    >>> pcs = PitchClassSet.from_pitches([0,4,7])
    >>> pcs.name
    'Major Chord'
    >>> print pcs.similar_sets
    >>> print pcs.supersets
    >>> print pcs.subsets
    >>> jazz_minor = pcs.supersets[133]
    >>> jazz_minor = Scale.from_pitches(jazz_minor)
    >>> print jazz_minor.relative_mode(2)
    >>> print jazz_minor.parallel_mode(3)
    >>> chord = jazz_minor.triad(1)
    >>> chord.add(7).no(5)
    >>> chord.name
    'Incomplete Minor-seventh Chord.1'
  

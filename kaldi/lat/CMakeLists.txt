add_pyclif_library("_arctic_weight" arctic-weight.clif
  CLIF_DEPS _float_weight
  RPATH $ORIGIN/../fstext
  BASETYPES __float__weight_clifwrap::pyFloatWeight
)

add_pyclif_library("_kaldi_lattice" kaldi-lattice.clif
  CLIF_DEPS _iostream _vector_fst
  LIBRARIES kaldi-lat
  RPATH $ORIGIN/../base:$ORIGIN/../fstext
)

add_pyclif_library("_confidence" confidence.clif
  CLIF_DEPS _vector_fst
  LIBRARIES kaldi-lat
  RPATH $ORIGIN/../fstext
)

add_pyclif_library("_sausages" sausages.clif
  CLIF_DEPS _options_itf _vector_fst
  LIBRARIES kaldi-lat
  RPATH $ORIGIN/../fstext:$ORIGIN/../itf
)

add_pyclif_library("_determinize_lattice_pruned" determinize-lattice-pruned.clif
  NAMESPACES fst
  CLIF_DEPS _options_itf _mutable_fst _transition_model
  LIBRARIES kaldi-lat
  RPATH $ORIGIN/../fstext:$ORIGIN/../itf:$ORIGIN/../hmm
)

add_pyclif_library("_minimize_lattice" minimize-lattice.clif
  CLIF_DEPS _mutable_fst
  LIBRARIES kaldi-lat
  RPATH $ORIGIN/../fstext
)
add_pyclif_library("_push_lattice" push-lattice.clif
  CLIF_DEPS _mutable_fst
  LIBRARIES kaldi-lat
  RPATH $ORIGIN/../fstext
)

add_pyclif_library("_phone_align_lattice" phone-align-lattice.clif
  CLIF_DEPS _options_itf _vector_fst _transition_model
  LIBRARIES kaldi-lat
  RPATH $ORIGIN/../fstext:$ORIGIN/../itf:$ORIGIN/../hmm
)

add_pyclif_library("_word_align_lattice" word-align-lattice.clif
  CLIF_DEPS _iostream _options_itf _vector_fst _transition_model
  LIBRARIES kaldi-lat
  RPATH $ORIGIN/../base:$ORIGIN/../fstext:$ORIGIN/../itf:$ORIGIN/../hmm
)

add_pyclif_library("_word_align_lattice_lexicon" word-align-lattice-lexicon.clif
  CLIF_DEPS _iostream _options_itf _vector_fst _transition_model
  LIBRARIES kaldi-lat
  RPATH $ORIGIN/../base:$ORIGIN/../fstext:$ORIGIN/../itf:$ORIGIN/../hmm
)

add_pyclif_library("_lattice_functions" lattice-functions.clif
  CLIF_DEPS _iostream _options_itf _decodable_itf _vector_fst _deterministic_fst _transition_model _kaldi_vector
  LIBRARIES kaldi-lat
  RPATH $ORIGIN/../base:$ORIGIN/../fstext:$ORIGIN/../itf:$ORIGIN/../hmm:$ORIGIN/../matrix
)
.. _1000_genomes:

1000_genomes
============

*  **Versions:** phase3
*  **Reference genome builds:** GRCh37, GRCh38
*  **Type:** :class:`MatrixTable`

Schema (phase3, GRCh37)
~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: text

    ----------------------------------------
    Global fields:
        'metadata': struct {
            name: str, 
            version: str, 
            reference_genome: str, 
            n_rows: int32, 
            n_cols: int32, 
            n_partitions: int32
        } 
    ----------------------------------------
    Column fields:
        's': str 
        'sex': str 
        'super_population': str 
        'population': str 
        'sample_qc': struct {
            call_rate: float64, 
            n_called: int64, 
            n_not_called: int64, 
            n_hom_ref: int64, 
            n_het: int64, 
            n_hom_var: int64, 
            n_non_ref: int64, 
            n_singleton: int64, 
            n_snp: int64, 
            n_insertion: int64, 
            n_deletion: int64, 
            n_transition: int64, 
            n_transversion: int64, 
            n_star: int64, 
            r_ti_tv: float64, 
            r_het_hom_var: float64, 
            r_insertion_deletion: float64
        } 
    ----------------------------------------
    Row fields:
        'locus': locus<GRCh37> 
        'alleles': array<str> 
        'rsid': str 
        'qual': float64 
        'filters': set<str> 
        'info': struct {
            CIEND: int32, 
            CIPOS: int32, 
            CS: str, 
            END: int32, 
            IMPRECISE: bool, 
            MC: array<str>, 
            MEINFO: array<str>, 
            MEND: int32, 
            MLEN: int32, 
            MSTART: int32, 
            SVLEN: array<int32>, 
            SVTYPE: str, 
            TSD: str, 
            AC: int32, 
            AF: float64, 
            NS: int32, 
            AN: int32, 
            EAS_AF: float64, 
            EUR_AF: float64, 
            AFR_AF: float64, 
            AMR_AF: float64, 
            SAS_AF: float64, 
            DP: int32, 
            AA: str, 
            OLD_VARIANT: array<str>, 
            VT: str, 
            EX_TARGET: bool, 
            MULTI_ALLELIC: bool
        } 
        'was_split': bool 
        'cm_position': float64 
        'recombination_rate_cm_per_mb': float64 
        'variant_qc': struct {
            AC: array<int32>, 
            AF: array<float64>, 
            AN: int32, 
            homozygote_count: array<int32>, 
            n_called: int64, 
            n_not_called: int64, 
            call_rate: float32, 
            n_het: int64, 
            n_non_ref: int64, 
            het_freq_hwe: float64, 
            p_value_hwe: float64
        } 
    ----------------------------------------
    Entry fields:
        'GT': call 
    ----------------------------------------
    Column key: ['s']
    Row key: ['locus', 'alleles']
    ----------------------------------------
    

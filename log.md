# Log

## 2023-04-05
- create conda env with current `torch` and `transformers`, but with `fitlog==0.9.13` and `fastnlp==0.7.0` @DFKI 
- adjust `model/modeling_bart.py`, commit: a857e4650ee2b516c7ff9812448bc0738d1b57e3
- create log directory: `logs/essay`
- install `numpy==1.21.6`
- further adjustments to the code (until commit: 159e9ae84004660b497da45d31052e57937f2bf4)
- start training @DFKI (in screen `GMAM`): `python train.py`
- final output:
    ```
    Evaluate data in 6.75 seconds!
    Evaluate data in 11.75 seconds!
    FitlogCallback evaluation on data-test:
    Seq2SeqSpanMetric_essay: triple_f=46.35, triple_rec=45.15, triple_pre=47.620000000000005, am_component_f=74.13, am_component_rec=74.19, am_component_pre=74.07000000000001, em=0.3148, invalid=0.0, entity_info={'<<P>>': {'acc': 80.0, 'recall': 77.1323, 'f1': 78.54}, '<<C>>': {'acc': 59.8784, 'recall': 65.4485, 'f1': 62.5397}, '<<MC>>': {'acc': 74.359, 'recall': 75.817, 'f1': 75.0809}}, entity_overall={'acc': 74.0711462450593, 'recall': 74.18844022169438, 'f1': 74.12974683544304}, invalid_len=0.0, invalid_order=0.0, invalid_cross=0.0, invalid_cover=0.0
    Evaluation on dev at Epoch 75/75. Step:2850/2850:
    Seq2SeqSpanMetric_essay: triple_f=38.769999999999996, triple_rec=39.050000000000004, triple_pre=38.49, am_component_f=67.5, am_component_rec=69.28999999999999, am_component_pre=65.81, em=0.3238, invalid=0.0, entity_info={'<<C>>': {'acc': 53.9216, 'recall': 62.5, 'f1': 57.8947}, '<<P>>': {'acc': 70.9091, 'recall': 71.0706, 'f1': 70.9898}, '<<MC>>': {'acc': 67.7419, 'recall': 74.1176, 'f1': 70.7865}}, entity_overall={'acc': 65.80732700135685, 'recall': 69.28571428571428, 'f1': 67.5017397355602}, invalid_len=0.0, invalid_order=0.0, invalid_cross=0.0, invalid_cover=0.0

    In Epoch:59/Step:2242, got best dev performance:
    Seq2SeqSpanMetric_essay: triple_f=41.15, triple_rec=41.53, triple_pre=40.77, am_component_f=67.86999999999999, am_component_rec=69.71000000000001, am_component_pre=66.12, em=0.3333, invalid=0.0, entity_info={'<<C>>': {'acc': 55.8376, 'recall': 62.5, 'f1': 58.9812}, '<<P>>': {'acc': 70.4444, 'recall': 72.2096, 'f1': 71.3161}, '<<MC>>': {'acc': 67.033, 'recall': 71.7647, 'f1': 69.3182}}, entity_overall={'acc': 66.12466124661248, 'recall': 69.71428571428572, 'f1': 67.8720445062587}, invalid_len=0.0, invalid_order=0.0, invalid_cross=0.0, invalid_cover=0.0
    ```

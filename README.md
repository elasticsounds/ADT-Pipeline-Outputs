# ADT-Pipeline-Outputs
Demo for all pipeline outputs

# TEST COMMANDS

## Cuaderno 5 Full Book

python main.py --textbook accessible_digital_textbooks/few_shot/adt_examples/textbooks/cuaderno5.pdf --output_dir c5_10_30_extraction_outputs --translation_targets en --base_language es --start 10 --end 30
### RESULT FAILED --> See Logfile.

## Cuaderno 5 page 10 - 30
python main.py --textbook accessible_digital_textbooks/few_shot/adt_examples/textbooks/cuaderno5.pdf --output_dir c5_10_30_extraction_outputs --translation_targets en --base_language es --start 10 --end 30

python tts.py --input_dir extraction_outputs --output_dir tts_output --languages es --overwrite

python tts.py --input_dir extraction_outputs --output_dir tts_output --languages en --overwrite

python adt.py --pdf_path accessible_digital_textbooks/few_shot/adt_examples/textbooks/cuaderno5.pdf --input_dir c5_10_30_extraction_outputs --output_dir c5_10_30_web_assets_result --base_language es --languages en --overwrite --start 10 --end 30 --tts_input_dir c5_10_30_tts_output

## Cuaderno 3 page 10 - 30
python main.py --textbook accessible_digital_textbooks/few_shot/adt_examples/textbooks/cuaderno3.pdf --output_dir c3_10_30_extraction_outputs --translation_targets en --base_language es --start 10 --end 30

### Many elements were still enqueued - so ran with --retry_errored_and_enqueued
python main.py --textbook accessible_digital_textbooks/few_shot/adt_examples/textbooks/LivingUruguay1.pdf --output_dir lu_1_extraction_outputs --translation_targets en --base_language es --start 10 --end 30 --retry_errored_and_enqueued

mkdir c3_10_30_tts_output

python adt.py --pdf_path accessible_digital_textbooks/few_shot/adt_examples/textbooks/cuaderno3.pdf --input_dir c3_10_30_extraction_outputs --output_dir c3_10_30_web_assets_result --base_language es --languages en --overwrite --start 10 --end 30 --tts_input_dir c3_10_30_tts_output

## Living Uruguay 1 page 10 - 30
python main.py --textbook accessible_digital_textbooks/few_shot/adt_examples/textbooks/LivingUruguay1.pdf --output_dir lu_1_extraction_outputs --translation_targets es --base_language en --start 10 --end 30

mkdir lu_1_tts_output

python adt.py --pdf_path accessible_digital_textbooks/few_shot/adt_examples/textbooks/LivingUruguay1.pdf --input_dir lu_1_extraction_outputs --output_dir lu_1_web_assets_result --base_language en --languages es --overwrite --start 10 --end 30 --tts_input_dir lu_1_tts_output

## Science 5th grade page 10 - 30
python main.py --textbook accessible_digital_textbooks/few_shot/adt_examples/textbooks/science5thgrade.pdf --output_dir science5thgrade_extraction_outputs --translation_targets es --base_language en --start 10 --end 30

mkdir science5thgrade_tts_output

python adt.py --pdf_path accessible_digital_textbooks/few_shot/adt_examples/textbooks/science5thgrade.pdf --input_dir science5thgrade_extraction_outputs --output_dir science5thgrade_web_assets_result --base_language en --languages es --overwrite --tts_input_dir science5thgrade_tts_output

## Math 2nd Grade whole book
python main.py --textbook accessible_digital_textbooks/few_shot/adt_examples/textbooks/math2ndgrade.pdf --output_dir math2ndgrade_extraction_outputs --translation_targets es --base_language en --start 10 --end 30

mkdir math2ndgrade_tts_output

python adt.py --pdf_path accessible_digital_textbooks/few_shot/adt_examples/textbooks/math2ndgrade.pdf --input_dir math2ndgrade_extraction_outputs --output_dir math2ndgrade_web_assets_result --base_language en --languages es --overwrite --tts_input_dir math2ndgrade_tts_output

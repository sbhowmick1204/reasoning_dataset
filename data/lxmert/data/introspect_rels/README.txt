This is the version of VQA-Introspect that has relation annotations for the binary QA pairs. Relations have been predicted using a fine-tuned BERT, which was pre-trained for NLI and fine-tuned on a sub-set of VQA-Introspect.

In general, entries have the following fields:
img_id: This is the image name without extension (images come from COCO)
question_id: Question identifier as int
sent: String version of the question
question_type: Type of question (how it starts)
answer_type: Type of answer
label: Answers using soft scores (as required by LXMERT)
role: Question role (main, sub or unk)
Questions with role='sub' also have a field named parent, which indicates the ID of the QA pair it is related to, and a field named rel, which contains the relation to the parent.

Total samples:
Train: 215862 (sub: 160085, main: 55777)
Val: 69668 (sub: 49882, main: 19786)


3.0 Classes
====================================

Message Elements:
================
Following are the classes that should be used while creating messages in Golambda 3.0

KeyValueDict
^^^^^^^^^^^^

MessageText
^^^^^^^^^^^
* message_obj = MessageText("This is the sample message")

MessageTemplate
^^^^^^^^^^^^^^^
* template = MessageTemplate(template=TextWithEndWithResult)

MessageNextIntent
^^^^^^^^^^^^^^^^^
* next_intents = MessageNextIntent(next_intents=self.common_next_intents)

BookingCardList
^^^^^^^^^^^^^^^
* booking_card_list = BookingCardList(booking_cards=booking_cards)

AltInfo
^^^^^^^
DefaultIntents
^^^^^^^^^^^^^^
Form
^^^^
* form = Form(form_label, title, form_identifier, mandatory=True)
* Available Methods:
    add_textinput_form_field(self, name, label)
    add_checkbox_form_field(self, name, label)
    add_drop_down_form_field(self, name, label, options)
    add_slider_form_field(self, name, label, rangeVal=10, initialValue=0)
    
CustomEventList
^^^^^^^^^^^^^^^

Response Elements:
^^^^^^^^^^^^^^^^^
* MessageDoc
* AnalyticDoc
* GolambdaContextDoc
* ConversationContextDoc
* DialogueContextDoc

Notes on GoLambda Framework
===========================

* Whenever a lambda requires information specific to a booking, goLambda can fetch it for you from middleware and provide
you a EJDB object which can be used to retrieve information with out parsing the JSON structure of the middleware response.

Usage:
-----
   booking_obj = self.instance
This statement will query the middleware for the booking of pid taken from self.paymentid and return you a object with
the following keys


`
"aa", "airline_phone_no", "alnm", "amount", "an", "auto_cin", "bid", "booking_type", "bref", "bst", "checkint",
"checkout", "checkoutt", "cid", "client_flavour", "color", "cp", "created", "db_status", "departure", "dest", "destcode",
"destterm", "destvid", "fd_product", "flt_duration", "fno", "gcpamount", "hn", "hotel_id", "hoteladdr", "hpn", "hvid",
"id", "installment_link", "irctc_error", "isHotline", "is_hotelier_chat_enabled", "is_ppe", "is_refundable", "lat",
"lid", "long", "mid", "on", "package_name", "pax_email", "pax_list", "pax_mobile", "pay_mode", "pid", "print", "rt",
"src", "srccode", "srcterm", "srcvid", "title", "ugc", "vendor", "vertical", "vouchers"
`


* Whenever you create a class extending GoibiboAction class and call init of the super class, goLambda framework add the
a lot fields in the instance of the object. Some of them are :

self.paymentid, self.mobile, self.entity_vertical, self.vertical
self.intent_name, self.channel, self.lid, self.email, self.user_id

* Whenever you create an Intent Class, Framework adds some of the common attributes by default. If you have any attribute
other than these, only then you need to add the attribute in the intent class. The attributes that are default are:

`
'pid': Attribute(value_type=unicode, IsMandatory=False, path='paymentid'),
'lid': Attribute(value_type=unicode, IsMandatory=False, path='lid'),
'email': Attribute(value_type=unicode, IsMandatory=False, path='email'),
'mobile': Attribute(value_type=unicode, IsMandatory=False, path='mobile'),
'user_id': Attribute(value_type=int, IsMandatory=False, path='user_id'),
'sessionid': Attribute(value_type=unicode, IsMandatory=False, path='sessionid'),
'channel': Attribute(value_type=unicode, IsMandatory=False, path='channel'),
'attachMeta': Attribute(value_type=bool, IsMandatory=False, path='attachMeta', default_value=False),
'inhouse_entities': Attribute(value_type=dict, IsMandatory=False, path='inhouse_entities', default_value={}),
'golambda_context': Attribute(value_type=dict, IsMandatory=False, path='golambda_context', default_value={}),
'bid': Attribute(value_type=unicode, IsMandatory=False, path='bookingid'),
'intent_name': Attribute(value_type=unicode, IsMandatory=False, path='intent_name'),
'lang': Attribute(value_type=unicode, IsMandatory=False, default_value=u'', path='lang'),
'user_key': Attribute(value_type=unicode, IsMandatory=False, default_value=u'', path='user_key'),
'flavour': Attribute(value_type=unicode, IsMandatory=False, default_value=u'', path='flavour'),
'app_version': Attribute(value_type=int, IsMandatory=False, path='app_version'),
'conversation_id': Attribute(value_type=unicode, IsMandatory=False, default_value=u'', path='conversation_id'),
'gi_trace_id': Attribute(value_type=unicode, IsMandatory=False, default_value=u'', path='gi_trace_id'),
'message': Attribute(value_type=unicode, IsMandatory=False, default_value=u'', path='message'),
'tta_enabled': Attribute(value_type=bool, IsMandatory=False, default_value=False, path='tta_enabled'),
'user_type': Attribute(value_type=int, IsMandatory=False, default_value=0, path='user_type'),
'vertical': Attribute(value_type=unicode, IsMandatory=False, default_value=u'', path='e.vertical'),
'first_time': Attribute(value_type=bool, IsMandatory=False, default_value=False, path='first_time')
`

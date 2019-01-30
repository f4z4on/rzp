# RŽP

[RŽP](http://www.rzp.cz) means “*Registr živnostenského podnikání*” (translated to English as the *Trade Licensing Register*). It is a partially public database of business subjects in the Czech Republic operated by the [Ministry of Industry and Trade](http://www.mpo.cz). The system was originally developed by [ICZ a.s.](http://www.i.cz) for the government.

Fun fact is that an official name of the system is actually “*Živnostenský rejstřík*” which is one of those bizarre moments when you just don’t get what the hell are doing those people paid by you. Not to mention there are four major systems operated by different branches of the Czech government providing public information about business subjects in the country.

There is a [documentation](http://www.rzp.cz/napoveda.html) describing public API to RŽP. But it is only in Czech and there are more than 30 pages of XML Schema code in PDF which can’t be just copied and pasted elsewhere. So, here we are, fixing government’s and major vendor’s incompetency.

There’s a [simple HTML form](index.html) which serves as a way to submit XML requests (yeah, this is the API). There are example XML requests for [general query](req-query.xml) and [subject’s details info](req-detail.xml). Finally, there are XML Schema sources which can help you validate [your requests](request.xsd) and [responses from the system](response.xsd).

Your request can be validated with `xmllint` or similar tool, for example:

```bash
xmllint --schema request.xsd YOUR_XML_REQ
```

The schemas are copied as-is from the official documentation. I will provide English comments later (hopefully). The API is versioned and this repo covers only the version 2.6.

## License

There is no license mentioned in the documentation created by ICZ so it falls back to the Czech IP laws which means I am relatively sure you and I can copy as we like for our own purposes. If anything, it is my fault for publishing these files here without asking ICZ first—you are safe unless you are publishing them too. I will clear this issue later (hopefully).

You can use this code for whatever you like, I don’t care.

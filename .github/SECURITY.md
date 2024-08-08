PyObject *item;
int err;
while (item = PyIter_NextItem(iterator, &err)) {
    /* do something with item */
    ...
    /* release reference when done */
    Py_DECREF(item);
}
Py_DECREF(iterator);
if (err < 0) {
    /* error */
}
else {
    /* no error */
}# Security Policy

## Supported Versions

The Python team applies security fixes according to the table
in [the devguide](
https://devguide.python.org/versions/#supported-versions
).

## Reporting a Vulnerability

Please read the guidelines on reporting security issues [on the
official website](https://www.python.org/dev/security/) for
instructions on how to report a security-related problem to
the Python team responsibly.

To reach the response team, email `security at python dot org`.

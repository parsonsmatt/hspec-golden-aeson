# hspec-golden-aeson

GoldenSpecs functions write golden files if they do not exist. When they do
exist they use a seed from the golden file to create an arbitrary value of a
type and check if the serialization matches the file. If it fails it means
that there has been a change in the Aeson serialization or a change in the
data type.

RoundtripSpecs make sure that a type is able to be encoded to JSON, decoded
from JSON back to the original type, and equal the same value. If it fails
then there may be an issue with the ToJSON and FromJSON instances.
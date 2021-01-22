# flag-struct
func (f *FlagSet) String(name string, value string, usage string) *string
//String defines a string flag with specified name, default value, and usage string. 
//The return value is the address of a string variable that stores the value of the flag.

func (f *FlagSet) StringVar(p *string, name string, value string, usage string)
//StringVar defines a string flag with specified name, default value, and usage string. 
//The argument p points to a string variable in which to store the value of the flag.

func (f *FlagSet) Args() []string 
// Args returns the non-flag arguments

func (f *FlagSet) Bool(name string, value bool, usage string) *bool
//Bool defines a bool flag with specified name, default value, and usage string. 
//The return value is the address of a bool variable that stores the value of the flag.

func (f *FlagSet) Int(name string, value int, usage string) *int
//Int64 defines an int64 flag with specified name, default value, and usage string.
//The return value is the address of an int64 variable that stores the value of the flag.

func (f *FlagSet) Parse(arguments []string) error
//Parse parses flag definitions from the argument list, which should not include the command name.
//Must be called after all flags in the FlagSet are defined and before flags are accessed by the program. 
//The return value will be ErrHelp if -help or -h were set but not defined.


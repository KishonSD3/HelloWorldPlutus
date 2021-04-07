import qualified Data.Text                 as T -- #Import Declarations see https://www.haskell.org/onlinereport/haskell2010/haskellch5.html#x11-1010005.3
import           Language.Plutus.Contract  hiding (when)
import           Language.PlutusTx.Prelude -- #Modules see https://www.haskell.org/onlinereport/haskell2010/haskellch5.html#x11-980005
import           Playground.Contract

-- | A 'Contract' that logs a message.  #comments see https://www.haskell.org/onlinereport/haskell2010/haskellch2.html#x7-170002.3
hello :: Contract BlockchainActions T.Text () -- #Variables,Constructors,Type Signatures see https://www.haskell.org/onlinereport/haskell2010/haskellch3.html#x8-240003.2.
hello = logInfo @String "Hello, world" -- #Declaration and Bindings see https://www.haskell.org/onlinereport/haskell2010/haskellch4.html#x10-620004

endpoints :: Contract BlockchainActions T.Text () -- #Variables,Constructors,Type Signatures see https://www.haskell.org/onlinereport/haskell2010/haskellch3.html#x8-240003.2.
endpoints = hello -- #Declaration and Bindings see https://www.haskell.org/onlinereport/haskell2010/haskellch4.html#x10-620004

mkSchemaDefinitions ''BlockchainActions
-- mkSchemaDefinitions :: Name -> Q [Dec]
-- https://playground.plutus.iohkdev.io/tutorial/haddock/playground-common/html/src/Playground.TH.html#mkSchemaDefinitions
-- https://playground.plutus.iohkdev.io/tutorial/haddock/playground-common/html/Playground-Contract.html
-- credit https://gist.github.com/denisonluz/c71de55be66541b8f26ce79810d904aa

$(mkKnownCurrencies [])
-- mkFunction :: Name -> Q [Dec]
-- https://playground.plutus.iohkdev.io/tutorial/haddock/playground-common/html/src/Playground.TH.html#mkFunctions
-- https://playground.plutus.iohkdev.io/tutorial/haddock/playground-common/html/Playground-Contract.html
-- credit https://gist.github.com/denisonluz/c71de55be66541b8f26ce79810d904aa

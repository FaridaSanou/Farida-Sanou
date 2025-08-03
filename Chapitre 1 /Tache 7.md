HC1T7 - Tâche 7 : Conversion Fahrenheit/Celsius
-- Fonction de conversion Fahrenheit → Celsius
fToC :: Floating a => a -> a
fToC f = (5 / 9) * (f - 32)

-- Fonction principale
main :: IO ()
main = do
  let fahrenheit = 98.6
  let celsius = fToC fahrenheit
  putStrLn ("La température " ++ show fahrenheit ++ "°F équivaut à " ++ show celsius ++ "°C")

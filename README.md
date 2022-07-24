# Santander-Bootcamp-Mobile-Developer
Repositório dedicado às entregas de exercícios, desafios, entre outros necessários na condução dos estudos deste Bootcamp.

## Páginas do Santander Bolsas e da Digital Innovation One - DIO

[Bolsas Santander Tecnologia | Santander Bootcamp 2022](https://app.becas-santander.com/pt-BR/program/bolsas-santander-tecnologia-santander-bootcamp-2022)

[Digital Innovation One](https://web.dio.me/home)

## Introdução ao Kotlin

### Tipos de dado e os parse's (quando houver)

- Int => toInt()
- Long => toLong()
- Float => toFloat()
- Double => toDouble()
- Array => toList() ???
- Boolean
- Char => toChar()
- Byte => toByte()
- Short => toShort()
- Null!

### Declaração de variáveis

- var (valor mutável e é camelCase)
- val (valor imutável e é camelCase)
- const val (valor imutável e é SNAKE_CASE)

### Principais tópicos dessa matéria

[Kotlin Playground contendo os principais tópicos dessa matéria](https://pl.kotl.in/3_RbmJigU)

fun main() {
    // Professora Ana Luísa Dias (DIO)

    // Exemplo de declaração de variável do tipo var

    // Valor definido e alterado durante a execução

    // var currentAge = 22
    // var currentAge:Int?

	// --- x --- x --- x ---

    // Exemplo de declaração de variável do tipo val

    // Valor definido durante a execução

    // val currentAge = 22
    // val currentAge:Int?

    // --- x --- x --- x ---

    // Exemplo de declaração de variável do tipo const val

    // Valor definido durante a compilação

    // const val MIN_AGE = 16
    // const val MAX_AGE = 69

    // --- x --- x --- x ---

    val bingo = listOf(3,6,9,8,6,34,2,17,19,21,22,33,29)
    val number = (1..34).random()
    
    println(number)
    println(number in bingo)
    
    val name = "Marcio Alessandro"
    val s = "Olá"
            
    println(name[0])
    println(name.first())
    
    println(name[name.length-1])
    println(name.last())
    
    println(s + name)
    println("${s}, ${name}")
    println("Bem vindo(a), $name!")
    
    println("--- x --- x --- x ---")
    println("")
    
    // Início da aula => Empty x Blank
    println("Início da aula => Empty x Blank")
    
    val s1 = ""
    println(s1.isEmpty())
    println(s1.isBlank())
    println(s1.isNullOrBlank() || s.isNullOrEmpty())
    
    val s2 = "   "
    println(s2.isEmpty())
    println(s2.isBlank())
    
    // Fim da aula => Empty x Blank
    println("Fim da aula => Empty x Blank")
    println("--- x --- x --- x ---")
    println("")
    
    // Início da aula => Funções
    println("Início da aula => Funções")
    
    // private fun getFullName(parâmetros:Tipo):TipoRetorno{
    	// val fullName = "$name $lastName"
    	// return fullName
	// }
    
    println(getFullNameExempleOne("Marcio","Alessandro"))
    
    // Exemplo de função single-line
    println(getFullNameExempleTwo("Marcio","Xavier"))
    
    // Exemplo de função inline
    println(getFullNameExempleThre("Marcio","Neto"))
    
    // Fim da aula => Funções
    println("Fim da aula => Funções")
    println("--- x --- x --- x ---")
    println("")
    
    // Início da aula => Funções de ordem superior
    println("Início da aula => Funções de ordem superior")
    
    // Recebem outra função ou lambda por parâmetro
    
    // Exemplo de função recebendo outra fução
    // val x = calculate(12,4,::sum)
    
    // Exemplo de função recebendo lambda
    // val y = calculate(12,4){ a,b -> a*b }
    
    val z1:Int
    val z2:Int
    val z3:Int
    
    z1 = calculate(34, 90, ::sum)
    z2 = calculate(34, 90){a,b -> a*b}
    z3 = calculate(34, 90){a,b -> 
        println("Vou calcular!")
        a+b+3}
    
    println(z1)
    println(z2)
    println(z3)
    
    // Fim da aula => Funções de ordem superior
    println("Fim da aula => Funções de ordem superior")
    println("--- x --- x --- x ---")
    println("")
    
    // Início da aula => Funções single e funções/extensões
    println("Início da aula => Funções single e funções/extensões")
    
    // Função com o prefixo, exemplo fun String.nomeDaFuncao()
    // Você pode criar uma função que só pode ser chamada por um
    // tipo específico, cujo o valor pode ser referenciado dentro
    // d função através da palavra this
    
    // fun String.randomCapitalizedLetter() = this[(0..this.length-1).random()].toUpperCase()
    
    // Fim da aula => Funções single e funções/extensões
    println("Fim da aula => Funções single e funções/extensões")
    println("--- x --- x --- x ---")
    println("")
    
    // Início da aula => Estruturas de controle
    println("Início da aula => Estruturas de controle")
    
    // Exemplo de IF
    val num:Int = 3
    
    if(num > 6){
        // bloco de código
    } else if (num > 9){
        // bloco de código
    } else{
        // bloco de código
    }
    
    // Exemplo de WHEN, conhecido como switch em algumas linguagens conhecidas
    
    when {
       num > 6 -> {}
       num > 9 -> {} 
       else -> {} 
    }
       
    // Exemplo de "Elvis operator"
    
    val a:Int? = null
    var number1 = a ?: 0
    
    // Fim da aula => Estruturas de controle
    println("Fim da aula => Estruturas de controle")
    println("--- x --- x --- x ---")
    println("")
    
}

private fun getFullNameExempleOne(name:String, lastName:String):String{
    val fullName = "$name $lastName"
    return fullName
}

private fun getFullNameExempleTwo(name:String, lastName:String):String{
    return "$name $lastName"
}

private fun getFullNameExempleThre(name:String, lastName:String) = "$name $lastName"

fun sum(a1:Int,a2:Int) = a1.plus(a2)

fun calculate(n1:Int,n2:Int,operation:(Int,Int)->Int):Int{
    val result = operation(n1,n2)
    return result
}

// fun String.randomCapitalizedLetter() = this[(0..this.length-1).random()].toUpperCase()


## Fundamentos de Orientação a Objetos com Kotlin

- Professor Jether Rodrigues


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

fun main() {
   val personOne = Person()
   
   println(personOne.nome)
   println(personOne.cpf)
   
   println(personOne.personInTo())
}

data class Banco(
    val nome:String,
    val numero:String
)

class Conta {
    
    var agencia:String
    privte set
    
    val numero:String
    val saldo:Double
    
    fun deposito(valor:Double) {
        
    }
    
    fun saque(valor:Double) {
        
    }
}

class Person {
    var nome:String = "Teste"
    var cpf:String = "000.000.000-00"
    
    // Construtor secundário
    constructor()
    
    fun personInTo() = "$nome e $cpf"
    
}

fun main() {
    
    val bankOne = Banco(nome = "Banco teste um", numero = 9)
    
    println(bankOne.nome)
    
}

data class Banco(
    val nome:String,
    val numero:Int
)

// enum class

fun main() {
   ClienteTipo.values().forEach { elemento ->
       println("${elemento.name} - ${elemento.descricao}")
   }
   
   val pf = ClienteTipo.PF
   println("${pf.name} - ${pf.descricao}")
}

enum class ClienteTipo(val descricao:String){
    PF("Pessoa Física"),
    PJ("Pessoa Jurídica");
}

// abstract class

Solutions
Docs
Community
Teach
Play
1.7.10
JVM
Program arguments
Copy link
Share code
Run
fun main() {
   val funcionarioUm = Analista("Nome do funcionário Analista", "000.000.000-00", 3333.21)
   
   ImprimeRelatorioFuncionario.imprime(funcionarioUm)
}

class Analista(nome:String, cpf:String, salario:Double) : Funcionario(nome, cpf, salario) {
    
    override fun calculoAuxilio() = salario * 0.1
    
}

abstract class Funcionario(
    nome:String,
    cpf:String,
    val salario:Double
) : PersonAbstract(nome, cpf) {
    
    // Exemplo da classe Funcionario herdando da classe PersonAbstract
    
    protected abstract fun calculoAuxilio():Double
    
    override fun toString(): String = """
        Nome: $nome
        CPF: $cpf
        Salário: $salario
        Auxílio: ${calculoAuxilio()}
    """.trimIndent()
    
}

class ImprimeRelatorioFuncionario {
    companion object {
        fun imprime(funcionario: Funcionario) {
            println(
                funcionario.toString()
            )
        } 
    }
}

open class Person (
    open val nome:String,
    open val cpf:String
) {
    
}

abstract class PersonAbstract (
    val nome:String,
    val cpf:String
) {
    
}


## Aplicando Conceitos de Coloções, Arrays e Listas

- Professor Jether Rodrigues


fun main() {
   // Início da parte do IntArray
   
    val valuesIntArray = IntArray(11)
    
    valuesIntArray[0] = 0
    valuesIntArray[1] = 1
    valuesIntArray[2] = 2
    valuesIntArray[3] = 2
    valuesIntArray[4] = 1
    valuesIntArray[5] = 0
    valuesIntArray[6] = 9
    valuesIntArray[7] = 9
    valuesIntArray[8] = 9
    valuesIntArray[9] = 0
    valuesIntArray[10] = 0
    
    // Exemplo com o for
    println("Exemplo com o for")
    for(valor in valuesIntArray) {
        
        // valor é a variável que receberá os elementos do array a cada passagem pelo loop for
        
        println(valor)
        
    }
    
    println(" ")
    println("// --- x --- x --- x ---")
    println(" ")
    
    // Exemplo com o forEach
    println("Exemplo com o forEach")
    
    valuesIntArray.forEach{
        println("forEach $it")
    }
    
    println(" ")
    println("// --- x --- x --- x ---")
    println(" ")
    
    // Exemplo com o for por maio do index
    println("Exemplo com o for por maio do index")
    
    for(index in valuesIntArray.indices) {
        
        println("for + index => " + valuesIntArray[index])
        
    }
    
    // Fim da parte do IntArray
    
    println(" ")
    println("// --- x --- x --- x ---")
    println(" ")
    
    // Início da parte do IntArrayOf
    println("Início da parte do IntArrayOf")
    
    val valuesIntArrayOf = intArrayOf(2, 1, 0, 0, 1, 2, 3, 3, 3, 9, 9)
    
    valuesIntArrayOf.forEach {
        println(it)
    }
    
    // Fim da parte do IntArrayOf
    
    println(" ")
    println("// --- x --- x --- x ---")
    println(" ")
    
    // Início da parte do arrayOf
    println("Início da parte do arrayOf")
    
    val valuesArrayOf = arrayOf("Nome a","Nome b","Nome c")
    
    valuesArrayOf.sort()
    valuesArrayOf.forEach {
        println(it)
    }
    
    // Fim da parte do arrayOf
    
    println(" ")
    println("// --- x --- x --- x ---")
    println(" ")
    
    // Início da parte do doubleArray
    println("Início da parte do doubleArray")
    
    val valuesDoubleArray = DoubleArray(3)
    
    valuesDoubleArray[0] = 0.21
    valuesDoubleArray[1] = 0.07
    valuesDoubleArray[2] = 0.33
    
    valuesDoubleArray.sort()
    
    valuesDoubleArray.forEach {
        println(it)
    }
    
    valuesDoubleArray.forEachIndexed { index, valor ->
        
        valuesDoubleArray[index] = valor * 1.1
        
    }
    
    valuesDoubleArray.forEach {
         println("Valor com aumento de 10% => ${it}")
    }
    
    // Fim da parte do doubleArray
    
    println(" ")
    println("// --- x --- x --- x ---")
    println(" ")
    
    // Início da parte de operações
    println("Início da parte de operações")
    
    val valuesDoubleArrayOf = doubleArrayOf(1021.03, 1033.06, 1075.09)
    
    for(valueDoubleArrayOf in valuesDoubleArrayOf) {
        
        println(valueDoubleArrayOf)
        
    }
    
    println(" ")
    println("Maior valor é ${valuesDoubleArrayOf.maxOrNull()}")
    println(" ")
    println("Menor valor é ${valuesDoubleArrayOf.minOrNull()}")
    println(" ")
    println("Valor médio dos valores é ${valuesDoubleArrayOf.average()}")
    println(" ")
    
    println("Início do exemplo de filtro do valor maior e igual a 1030")
    println(" ")
    
    val valueFilter = valuesDoubleArrayOf.filter{it >= 1030}
    
    valueFilter.forEach{
        println(it)
    }
    
    println(" ")
    println("Início do exemplo de contar elementos num range")
    println(valuesDoubleArrayOf.count {it in 1030.0..2000.0}.toString() + " elemento(s)")
    println(" ")
    
    println("Início do exemplo de procurar pelo método find")
    println(valuesDoubleArrayOf.find {it == 1033.06})
    println(" ")
    
    println("Início do exemplo de procurar qualquer elemento pelo método any, com o retorno em Bolean")
    println(valuesDoubleArrayOf.any {it == 1033.06})
    println(" ")
    
    println("Início do exemplo lista utilizando listOf")
    
    val funcionarioUm = Funcionario("Nome A", 1000.3, "CLT")
    val funcionarioDois = Funcionario("Nome B", 1000.6, "PJ")
    val funcionarioTres = Funcionario("Nome C", 1000.9, "CLT")
    
    val funcionarios = listOf(funcionarioUm, funcionarioDois, funcionarioTres)
    
    funcionarios.forEach{
        println(it)
    }
    
    println(" ")
    
    println("Início de exemplo de procura em uma lista por meio do find")
    
    println(funcionarios.find{it.nome == "Nome A"})
    
    println(" ")
    
    println("Início de exemplo de ordenar por um item da lista")
    
    funcionarios.sortedBy{it.salario}.forEach{println(it)}
    
    println(" ")
    
    println("Início de exemplo de agrupar o retorno por meio de um item da lista")
    
    funcionarios.groupBy{it.tipoContratacao}.forEach{println(it)}
    
    println(" ")
    
    println("Início de exemplo de unir set's separados")
    
    val grupoFuncionariosCLT = setOf(funcionarioUm, funcionarioTres)
    val grupoFuncionariosPj = setOf(funcionarioDois)
    
    val gruposFuncionarios = grupoFuncionariosCLT.union(grupoFuncionariosPj)
    
    gruposFuncionarios.forEach{println(it)}
    
    println(" ")
    
    println("Tem a operação subtract, para extrair elementos iguais em set's diferentes, e tem a operação intersect para retornar somente o elemento igual             que existe entre os grupos")
    
    println(" ")
    
    println("Início da parte do mutableListOf")
    
    val funcionariosMutableListOf = mutableListOf(funcionarioUm, funcionarioDois)
    
    funcionariosMutableListOf.forEach{
        println(it)
    }
    
    println(" ")
    println("// --- x --- x --- x ---")
    println(" ")
    
    // Exemplo de adicionar item na lista
    println("Exemplo de adicionar item na lista")
    
    funcionariosMutableListOf.add(funcionarioTres)
    
    funcionariosMutableListOf.forEach{
        println(it)
    }
    
    println(" ")
    println("// --- x --- x --- x ---")
    println(" ")
    
    // Exemplo de remover item na lista
    println("Exemplo de remover item na lista")
    
    funcionariosMutableListOf.remove(funcionarioTres)
    
    funcionariosMutableListOf.forEach{
        println(it)
    }
    
    println(" ")
    println("// --- x --- x --- x ---")
    println(" ")
    
    println("Início da parte do mutableMap com o exemplo de uma classe para um CRUD de um map")
    
    val repositorio = Repositorio<Funcionario>()
    
    repositorio.create(funcionarioUm.nome, funcionarioUm)
    repositorio.create(funcionarioDois.nome, funcionarioDois)
    repositorio.create(funcionarioTres.nome, funcionarioTres)
    
    println(repositorio.findById(funcionarioUm.nome))
    
    println(" ")
    println("// --- x --- x --- x ---")
    println(" ")
    
    repositorio.findAll().forEach{
        println(it)
    }
    
    println("Fim da parte do mutableMap com o exemplo de uma classe para um CRUD de um map")
    
    println(" ")
    
    // Fim da parte de operações
    
    println(" ")
    println("// --- x --- x --- x ---")
    println(" ")
    
}

class Repositorio<T> {
    private val map = mutableMapOf<String, T>()
    
    // Criar um elemento no map
    fun create(id: String, value: T) {
        map[id] = value
    }
    
    // Excluir um item no map
    fun remove(id: String) = map.remove(id)
    
    // Pegar um elemento no map por meio do id
    fun findById(id: String) = map.get(id)
    
    // Pegar todos os elementos do map
    fun findAll() = map.values
    
    
}

data class Funcionario(
    val nome: String,
    val salario: Double,
    val tipoContratacao: String
) {
    
    override fun toString(): String = 
    
    """
    
    Nome:           $nome
    Salário:        $salario
    Tp Contratação:     $tipoContratacao
    --- x --- x --- x ---
    
    """.trimIndent()
}






# Agenda de Pagamentos Refatorado

Implementado o padrão **command** na classe principal *Main*, sendo adicionado as classes [Command](https://github.com/JhonathanMilk/PayrollRefatorado/blob/main/Command) e [MenuControl](https://github.com/JhonathanMilk/PayrollRefatorado/blob/main/MenuControl). além de várias tranformações de metódos em classes.

>[Main antiga](https://github.com/JhonathanMilk/Payroll/blob/main/Main)

>[Main Refatorada](https://github.com/JhonathanMilk/PayrollRefatorado/blob/main/Main)

Após a implementação do Command e separação de métodos em classes, ficou evidente outro smell. Então foi alterado duplicação de código, implementando o **Extract Method** em [RemoveEmployee](https://github.com/JhonathanMilk/PayrollRefatorado/blob/main/RemoveEmployee) e [PrintEmployee](https://github.com/JhonathanMilk/PayrollRefatorado/blob/main/RemoveEmployee), sendo implementado apenas um único método *testIsEmpty* na classe [PaymentSchedule](https://github.com/JhonathanMilk/PayrollRefatorado/blob/main/PaymentSchedule)

Aplicado também **Extract Method** nos métodos *AddServiceRate* e *showServiceRate* pertencentes a classe [ProgramControl](https://github.com/JhonathanMilk/Payroll/blob/main/ProgramControl). Importante ressaltar que essa clase não existe mais no projeto refatorado. o código duplicado dessas classes foi movido para  classe [Syndicate](https://github.com/JhonathanMilk/PayrollRefatorado/blob/main/Syndicate), método *scanIdSyndicate*.

Implementado o padrão **Introducer Parameter Object** no método *addEmployees* na classe [ProgramControl](https://github.com/JhonathanMilk/Payroll/blob/main/ProgramControl) e *changeTypeEmployee* na classe [ChangeRegistration](https://github.com/JhonathanMilk/Payroll/blob/main/ChangeRegistration). Os parâmetros foram encapsulados todos no objeto *dateEmployees*.

>[AddEmployees refatorada](https://github.com/JhonathanMilk/PayrollRefatorado/blob/main/AddEmployee) 

>[ChangeRegistration refatorada](https://github.com/JhonathanMilk/PayrollRefatorado/blob/main/ChangeRegistration) 

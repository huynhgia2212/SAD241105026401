### Phân tích các ca sử dụng còn lại trong Payroll System
**Use Cases**

**1. BankSystem**

- Primary Actor: Payroll System
  
- Preconditions: Employee has selected direct deposit as their payment method.
  
- Basic Flow:
  
Payroll System receives employee's bank account information.

Payroll System generates paycheck information.

Payroll System sends paycheck information to BankSystem.

BankSystem processes the paycheck information and deposits the funds into the employee's account.

- Alternative Flows:
  
If the BankSystem is unavailable, the Payroll System may need to hold the paycheck information until the BankSystem is back online.

If there are errors in the paycheck information, the Payroll System may need to notify the Payroll Administrator for correction.

**2. Employee**

- Primary Actor: Employee
  
- Preconditions: Employee has an account in the Payroll System.
  
- Basic Flow:
  
Employee logs into the Payroll System.

Employee enters timecard information or purchase orders.

Employee views their pay history and remaining vacation time.

Employee updates their personal information (address, payment method, etc.).

- Alternative Flows:
  
If the employee encounters errors while entering data, they may need to contact the Payroll Administrator for assistance.

If the employee forgets their password, they may need to initiate a password reset process.

**3. PayrollAdministrator**

- Primary Actor: Payroll Administrator
  
- Preconditions: Payroll Administrator has access to the Payroll System.

- Basic Flow:

Payroll Administrator adds new employees to the system.

Payroll Administrator deletes employees from the system.

Payroll Administrator updates employee information (name, address, payment classification, etc.).

Payroll Administrator runs administrative reports.

- Alternative Flows:

If the Payroll Administrator needs to make changes to the payroll schedule, they may need to update the System Clock.

If there are errors in the payroll calculations, the Payroll Administrator may need to investigate and correct them.

**4. Project Management Database**

- Primary Actor: Payroll System

- Preconditions: Project Management Database is accessible.

- Basic Flow:

Payroll System queries the Project Management Database for project information (charge numbers, project names, etc.).

Payroll System uses the retrieved project information to calculate employee pay.

- Alternative Flows:

If the Project Management Database is unavailable, the Payroll System may need to delay payroll processing or use cached data.

If there are errors in the project information, the Payroll System may need to notify the Payroll Administrator for correction.

**5. System Clock**

- Primary Actor: Payroll System

- Preconditions: System Clock is accurate.

- Basic Flow:

Payroll System queries the System Clock to determine the current date and time.

Payroll System uses the current date and time to calculate pay periods and generate paychecks.

- Alternative Flows:

If the System Clock is inaccurate, the Payroll System may generate incorrect paychecks.

**6. Pay Period**

- Primary Actor: Payroll System

- Preconditions: Pay Period start and end dates are defined.

- Basic Flow:

Payroll System calculates employee pay for the current pay period.

Payroll System generates paychecks for the current pay period.

- Alternative Flows:

If the pay period is changed, the Payroll System may need to adjust payroll calculations accordingly.

**7. Paycheck**

- Primary Actor: Payroll System
  
- Preconditions: Employee information and pay calculations are accurate.
  
- Basic Flow:
  
Payroll System generates a paycheck for each employee.

Payroll System sends paychecks to employees via their chosen payment method (mail, direct deposit, or pickup).

- Alternative Flows:
  
If there are errors in the paycheck information, the Payroll System may need to generate a corrected paycheck.

**8. Purchase Order**

- Primary Actor: Employee

- Preconditions: Employee is a commissioned employee.

- Basic Flow:

Employee enters a purchase order into the Payroll System.

Payroll System calculates the employee's commission based on the purchase order amount.

- Alternative Flows:

If the purchase order information is incorrect, the Payroll System may need to reject the purchase order.

**9. Salaried Employee**

- Primary Actor: Payroll System

- Preconditions: Employee is classified as salaried.

- Basic Flow:

Payroll System calculates the employee's salary based on their pay rate.

Payroll System generates a paycheck for the employee.

- Alternative Flows:

If the employee's salary rate changes, the Payroll System may need to update their pay calculations.

### Viết code Java mô phỏng ca sử dụng Maintain Timecard.

**Lớp Employee**

    public class Employee {
    private int id;
    private String name;
    private List<Timecard> timecards;

    public void addTimecard(Timecard timecard) {
        timecards.add(timecard);
    }
    }

    public class Timecard {
    private Date date;
    private Time startTime;
    private Time endTime;
    private String projectCode;

    

    public double getTotalHours() {
      
    }

    public double getOvertimeHours() {
       
    }
    }

**Lớp TimecardSystem**

        import java.util.*;

        public class TimecardSystem {
        public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        Employee employee = new Employee();
        employee.setId(1); 1 
        employee.setName("John Doe");

        while (true) {
            System.out.println("1. Nhập thông tin chấm công");
            System.out.println("2. Xem lại thông tin chấm công");
            System.out.println("3. Thoát");

            int choice = scanner.nextInt();

            switch (choice) {
                case 1:
                    Timecard timecard = new Timecard();
                    System.out.print("Ngày: ");
                    timecard.setDate(new Date(scanner.nextLong()));
                    employee.addTimecard(timecard);
                    break;
                case 2:
                   
                    break;
                case 3:
                    System.exit(0);
            }
        }
    }
}

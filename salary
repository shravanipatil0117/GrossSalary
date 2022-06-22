import java.awt.FlowLayout;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import javax.swing.JButton;
import javax.swing.JComboBox;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JPasswordField;
import javax.swing.JTextArea;
import javax.swing.JTextField;
import javax.swing.SwingUtilities;

public class SwingBasic extends JFrame {

  private String[] department = {
    "IT",
    "Product design",
    "Product managment",
    "HR",
    "Sales",
  };
  private String[] gender = { "Male", "Female" };
  private String[] project = {
    "frontend",
    "backend",
    "blockchain",
    "machine learning",
  };
  JLabel label;
  JLabel label2;
  JLabel label3;
  JLabel label4;
  JLabel label5;
  JLabel label6;
  JLabel label7;

  public void start() {
    //employee
    label = new JLabel();
    label.setText(" Employee Name :");
    JTextField txt = new JTextField();
    txt.setText("Enter employee details");

    //dep
    label2 = new JLabel();
    label2.setText(" Department :");
    JComboBox comboBox = new JComboBox();
    int count = 0;
    for (int i = 0; i < department.length; i++) comboBox.addItem(
      department[count++]
    );

    //basic salary
    label3 = new JLabel();
    label3.setText(" Basic salary :");
    JTextField salary = new JTextField();
    salary.setText("Enter basic salary details");

    //gender
    label4 = new JLabel();
    label4.setText(" Gender :");
    JComboBox comboBox2 = new JComboBox();
    int count2 = 0;
    for (int j = 0; j < gender.length; j++) comboBox2.addItem(gender[count2++]);

    //address
    label5 = new JLabel();
    label5.setText(" Address :");
    JTextField address = new JTextField();
    address.setText("Enter address");

    //projects
    label6 = new JLabel();
    label6.setText("Projects Topics :");
    JComboBox comboBox3 = new JComboBox();
    int count3 = 0;
    for (int k = 0; k < project.length; k++) comboBox3.addItem(
      project[count3++]
    );

    //Answer
    label7 = new JLabel();
    //submit
    JButton but = new JButton();
    JButton reset = new JButton();
    but.setText("Submit");
    reset.setText("Reset");
    add(label);
    add(txt);
    add(label2);
    add(comboBox);
    add(label3);
    add(salary);
    add(label4);
    add(comboBox2);
    add(label5);
    add(address);
    add(label6);
    add(comboBox3);
    add(but);
    add(reset);
    add(label7);
    //event listners
    but.addActionListener(
      new ActionListener() {
        public void actionPerformed(ActionEvent e) {
          try {
            String employee = txt.getText();
            Object department = comboBox.getSelectedItem();
            String emSalary = salary.getText();
            Object emGender = comboBox2.getSelectedItem();
            String emAddress = address.getText();
            Object proj = comboBox3.getSelectedItem();
            if (Integer.parseInt(emSalary) <= 0) {
              throw new Exception("cannot be 0");
            }
            if (employee.isEmpty()) {
              throw new Exception("NameCannotBeBlank");
            }
            double hra = 0.05 * Integer.parseInt(emSalary);
            double da = 0.6;
            if (Integer.parseInt(emSalary) >= 25000) {
              da = 0.7 * Integer.parseInt(emSalary);
            } else if (Integer.parseInt(emSalary) >= 30000) {
              da = 0.8 * Integer.parseInt(emSalary);
            } else if (Integer.parseInt(emSalary) >= 40000) {
              da = 0.85 * Integer.parseInt(emSalary);
            }
            double grossSalary = Integer.parseInt(emSalary) + da + hra;
            System.out.println(
              employee +
              " " +
              department +
              " " +
              emGender +
              " " +
              emAddress +
              " " +
              emSalary +
              " " +
              proj
            );
            System.out.println(grossSalary);
            label7.setText("Gross salary is :" + String.valueOf(grossSalary));
          } catch (Exception exc) {
            System.out.println("Error: " + exc.getMessage());
          }
        }
      }
    );
    reset.addActionListener(
      new ActionListener() {
        public void actionPerformed(ActionEvent e) {
          txt.setText("");
          comboBox.setSelectedIndex(0);
          salary.setText("");
          comboBox2.setSelectedIndex(0);
          address.setText("");
          comboBox3.setSelectedIndex(0);
        }
      }
    );
    setLayout(new FlowLayout());
    setBounds(400, 150, 150, 150);
    setSize(400, 400);
    setVisible(true);
    setDefaultCloseOperation(EXIT_ON_CLOSE);
  }

  public static void main(String args[]) {
    new SwingBasic().start();
  }
}

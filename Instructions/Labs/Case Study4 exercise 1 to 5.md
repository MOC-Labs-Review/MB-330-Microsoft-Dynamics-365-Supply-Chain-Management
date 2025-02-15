---
lab:
    title: 'Case study 4 Quality control and quality management'
    module: 'Module 5: Configure and manage quality control and quality management '
---
Case study 4 Quality control and quality management
===================================================

Objectives
----------

1.  *Enable quality management; create tests, item sampling, definitions and
    process of the quality management process.*

2.  *Create a manual quality order with a specification.*

3.  *Work with non-conformance issues like faulty items by defining several
    required specifications. *

4.  *Create and process a non-conformance order to have an item repaired and to
    adjust a faulty machine.*

5.  *Run a non-conformance report, a non-conformance tag report, and a
    corrections report*

Exercise \#1 Enable quality management process that specifies items to be inspected at the time of picking
----------------------------------------------------------------------------------------------------------

*Objective: Enable quality management; create tests, item sampling, definitions
and process of the quality management process.*

The quality manager in USMF wants to know how to enable a quality management
process requiring that incoming inventory for all TV products be inspected
immediately at the time of picking.

When she create a sales order for item T0002 and during the picking step, a
quality order will be automatically created.

To be able to proceed with picking and packing the sales order she will have to
process the quality order.

**Can you assess her to do the following?**

-   Enable quality management in Inventory management parameters.

-   Create tests.

-   Create test variables to define the test results are recorded.

-   Set up item sampling.

-   Create quality and item groups.

-   Create a test group.

-   Define when quality orders will be created.

-   Process quality orders.

### Enable quality management

1.  Go to **Inventory management** \> **Setup** \> **Inventory and warehouse
    management parameters**.

2.  Click the **Quality management** tab.

3.  Set the **Use quality management** option to **Yes**.

4.  Click **Report setup**. In USMF, the report setup for quality management is
    already defined. If this wasn’t done, you’d add new lines here for the
    different report types, and select the type of document to be used for each
    report.

5.  Close all pages.

### Create a test

1.  Go to **Inventory management** \> **Setup** \> **Quality control** \>
    **Tests**.

2.  Click **New**.

3.  In the **Test** field, type **eBookTest**.

4.  In the **Description** field, type **Test eBook**.

5.  In the **Type** field, select **Option** to assign the test results based on
    pre-defined values.

6.  Click **Save**.

7.  Close all pages.

### Create Test variables to define the way test results are recorded

1.  Go to **Inventory management** \> **Setup** \> **Quality control** \> **Test
    variables**.

2.  Click **New**.

3.  In the **Variable** field, type **Power**.

4.  In the **Description** field, type **Power up**.

5.  Click **Save**.

6.  Click **Outcomes**.

7.  Click **New**.

8.  In the **Outcome** field, type **ON**.

9.  In the **Description** field, type **Device starts normally**.

10. In the **Outcome** status field, select **Pass**.

11. Click **Save**.

12. Click **New**.

13. In the **Outcome** field, type **OFF**.

14. In the **Description** field, type **Device does not power up**.

15. In the **Outcome** status field, select **Fail**.

16. Click **Save**.

17. Close all pages.

### Set up item sampling

1.  Go to **Inventory management** \> **Setup** \> **Quality control** \> **Item
    sampling**.

2.  Click **New**.

3.  In the **Item sampling** field, type **One**.

4.  In the **Description** field, type one sample.

5.  In the **Quantity** specification field select **Fixed quantity**.

6.  In the **Value** field, enter **1**. This value relates to the Quantity
    specification that’s selected in the adjacent field.

7.  Expand or collapse the **Process** section.

8.  Select or clear the **Full blocking** option. If you select this option, the
    whole lot or order line quantity is blocked if a test is failed. If you
    don't select it, only the items in the quality order are blocked.

9.  Click **Save**.

10. Close all pages.

### Create a quality and item group

1.  Go to **Inventory management** \> **Setup** \> **Quality control** \>
    **Quality groups**.

2.  Click **New**.

3.  In the **Quality group** field, type **eBookQG**. Use a descriptive name to
    help you identify which kind of items the group will contain (your sampling
    criteria).

4.  In the **Description** field, type **Quality group for TVs**.

5.  Click **Save**.

6.  Click **Add items**.

7.  Select the **Item number** row. In this example the filtering will be run
    based on the item number.

8.  In the **Criteria** field, type **T\*** to filter on the item numbers that
    start with T.

9.  Click **OK**.

10. Click **OK**.

11. Close all pages.

### Create a test group

1.  Go to **Inventory management** \> **Setup** \> **Quality control** \> **Test
    groups**.

2.  Click **New**.

3.  In the **Test group** field, type **eBookTG**. Give the test group a name
    that will help you remember what kind of tests are being run, and which
    quality group it should be associated with.

4.  In the **Description** field, type **Test group for TVs**.

5.  In the **Item sampling** field, select **One**.

6.  Under the **Overview** tab, click **Add**.

7.  In the **Sequence** number field, enter **1**.

8.  In the **Test** field, select **eBookTest**.

9.  Click the **Test** tab.

10. In the **Variable** field, select **Power**.

11. In the **Default outcome** field, click the drop-down button to open the
    lookup.

12. Select **ON**.

13. Click **Save**.

14. Close all pages.

### Define when quality orders will be created

1.  Go to **Inventory management** \> **Setup** \> **Quality control** \>
    **Quality associations**.

2.  Click **New**.

3.  In the **Reference** type field, select **Sales**.

4.  In the Item code field, select **Group**.

5.  In the Item field, enter or select **eBookQG**.

6.  Expand the **Process** section.

7.  In the **Event** type field, select **Picking process is scheduled**.

8.  Expand the **Quality order process** section.

9.  In the **Event blocking** field, enter or select **Picking process**.

10. Expand the **Specifications** section.

11. In the **Test group** field, enter or select **eBookTG**.

12. Click **Save**.

13. Close all pages.

### Process quality orders

1.  Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.

2.  Click **New**.

3.  In the **Customer account** field, select **US-013**.

4.  Click **OK**.

5.  In the **Item number** field, enter or select **T0002**.

6.  On the Action Pane, click **Pick and pack**.

7.  Click **Quality orders**. Note that currently there is no quality order.

8.  Close the page.

9.  Click **Generate picking list**.

10. Click **OK**.

11. Click **OK**.

12. Read the error message generated preventing you from continuing the process
    of picking and packing because you have now a quality order .

13. Click **Quality orders**. Note the quality order automatically is generated.

14. Review the tests.

15. Click **Results**.

16. Set Result quantity to **1**.

17. Set **Test result** to **ON**.

18. Click **Validate**.

19. Close the page.

20. Click **Validate**.

21. Click **OK**.

22. Close the quality order page.

23. Click **Generate picking list**.

24. Click **OK**.

25. Click **OK**.

26. Once back on the **Sales order** page, clear the messages via the X.

27. Note that there is no error because you have passed the quality order test.

28. Click **Picking list registration**.

29. Click **Updates**.

30. Click **Update all**.

31. Close the form.

32. Click **Post packing slip**.

33. Click **OK**.

34. Click **OK**.

35. Close all pages.

Exercise \#2 Create a manual quality order with a specification
---------------------------------------------------------------

*Objective: Create a manual quality order with a specification.*

The quality manager must deal with non conformance and quality issues and track
the cause of any problems.

He wants make sure that the shipped products have a quality expected by USMF so
he asked an employee in sales, to make an additional selection for the HDMI
cable item A0002 for impedance by creating a manual quality order with a
specification.

The sales employee is new and not sure what to do. You were called to help the
sales employee. What features you will be using to perform the above tasks?

You will need to do the following:

### Create a manual quality order.

1.  Open **Inventory management \> Periodic tasks \> Quality management \>
    Quality orders**.

2.  Click **New**.

3.  Select **Inventory** as the **Reference type**.

4.  Select **Item number A0002.**

5.  Select **eBookTG** as the **Test group.**

6.  Type "1.00" in the **Quantity** field.

7.  Select **2** in the **Site** field.

8.  Select **24** in the **Warehouse** field.

9.  Select **Available** in the **Inventory status** field.

10. Click **OK**.

11. In the bottom pane, select the line where Sequence is 10 (Length), and then
    click **Results**.

12. In the **Result quantity** field, type "1.00".

13. In the **Test result** field, type "100.00".

14. Click **Validate** and close the form.

15. Select the line where Sequence is 20 (Rub and Scratch), and then click
    **Results**.

16. In the **Result quantity** field, type "1.00".

17. Click **Validate** and close the form.

Exercise \#3 Define conditions to work with non-conformance issues
------------------------------------------------------------------

*Objective: Work with non-conformance issues like faulty items by defining
several required specifications. *

Due to recent issues with customers returning faulty computers, you want to
setup some processes to deal with faulty items in the system.

You will need to define several conditions to work with non-conformance:
problems and diagnostic types, operations, quality charges, and quarantine
zones.

You will need to do the following:

Add diagnostic types.

Add a quarantine zone.

### Work with nonconformance

1.  Open **Inventory management \> Setup \> Quality management \> Problem
    types.**

2.  Click **New**.

3.  Enter **Temperature** in both **Problem type** and **Description** fields.

4.  Click **Save**.

### Add diagnostic types

1.  Open **Inventory management \> Setup \> Quality management \> Diagnostic
    types.**

2.  Click **New**.

3.  Enter **Machine temperature** in both **Diagnostic** and **Description**
    fields.

4.  Click **Save**.

5.  Open **Inventory management \> Setup \> Quality management \> Operations.**

6.  Click **New**.

7.  Enter **Adjustment temp** in both **Operation** and **Description** fields.

8.  Select **Purchase order** in the **type** field.

9.  Click **Save**.

10. Open **Inventory management \> Setup \> Quality management \> Quality
    charges.**

11. Click **New**.

12. Enter **Repair** in both **Problem type** and **Description** fields.

13. Click **Save**.

### Add a quarantine zone

1.  Open **Inventory management \> Setup \> Quality management \> Quarantine
    zones.**

2.  Click **New**.

3.  Enter **Repair** in both **Quarantine zone** and **Description** fields.

4.  Click **Save**.

Exercise \#4 Use non-conformance order to repair an item and a faulty machine (Bonus)
-------------------------------------------------------------------------------------

*Objective: Create and process a non-conformance order to have an item repaired
and to adjust a faulty machine.*

The company discovered a faulty computer in the inventory, and you will need to
raise a non-conformance order to get it fixed.

The item you found will need to be to be taken out of stock and repaired.

A machine has caused this fault and will need to be adjusted to prevent more
items to be faulty.

You will need to do the following:

### Create and process a non-conformance order.

1.  Open **Inventory management \> Periodic tasks \> Quality management \> Non
    Conformances**.

2.  Click **New**.

3.  Select **Internal** in **Non conformance** field.

4.  Enter **1000** in the **Item number** field.

5.  Enter **Enclosure** as the problem type.

6.  Enter **5.00** in the **Defective quantity** field.

7.  Enter **1** in the **Site** field.

8.  Enter **13** in the **Warehouse** field.

9.  Click **OK.**

10. Click the **Function** button (you may need to click the ellipsis toward the
    top right of the screen) and select **Approve non conformance.**

11. Click **Yes.**

12. Click the **Related operations** button.

13. Click **New.**

14. Select **Enclosure** in the **Operation** field.

15. Enter **Damaged** in the **Reason** field.

16. Click **Save**.

17. Click the **Items** button.

18. Click **New.**

19. Select **A0001** as the item number.

20. Enter **1.00** in the **Quantity** field.

21. Click **Save** and close form.

22. Click **Quality Charges** button.

23. Click **New.**

24. Select **Rework** in the **Charges code** field.

25. Enter **Rework** in the **Description** field.

26. Enter **100.00** in the **Charges value** field.

27. Click **Save** and exit form.

28. Click **Timesheet** button.

29. Click **New.**

30. Enter **5.0** in the **Operation hours** field.

31. Click **Save** and exit form.

32. Close the **Related operations** form.

33. Click the **Corrections** button.

34. Click **New.**

35. Select **Machine adjustment** in the **Diagnostic** field.

36. Select **000002 (Charlie Carson)** in the **Worker** field. Press
    **Select**.

37. Select **High** in the **Correction priority** field.

38. Click the **Save** button.

39. Click the **Mark Complete** button.

40. Click **OK** and close the form.

41. Click the **Functions** button and select **Close non conformance**.

42. Click **Yes.**

Exercise \#5 Run non-conformance reports
----------------------------------------

*Objective: Run a non-conformance report, a non-conformance tag report, and a
corrections report.*

The quality manager must review conformance items created during the month as
well as any corrections made that are related to conformance.

At the end of each month, he will need to run the reports and validate the
output.

The quality manager is not sure where or how to do so. You were called to help.

You will need to do the following:

-   Run a non-conformance report.

-   Run a non-conformance tag report.

-   Run a correction report.

### Run a non-conformance report

1.  Open **Inventory management \> Inquiries and reports \> Quality management
    \> Non Conformance**.

2.  Click **OK**.

### Run a non-conformance tag report

1.  Open **Inventory management \> Inquiries and reports \> Quality management
    \> Non Conformance tag**.

2.  Click **OK**.

### Run a correction report

1.  Open **Inventory management \> Inquiries and reports \> Quality management
    \> Corrections**.

2.  Click **OK**.

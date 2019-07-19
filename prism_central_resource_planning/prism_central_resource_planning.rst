.. _prism_central_resource_planning:

--------------------------------
Prism Central: Resource Planning
--------------------------------

Overview
++++++++

This lab will introduce Prism Central’s resource planning features that help you stay on top of cluster utilization and more accurately predict cluster expansions.

Prism Central Resource Planning
+++++++++++++++++++++++++++++++

Nutanix utilizes our X-Fit machine learning and data analytics as part of Prism Pro. We utilize that machine learning and data analytics to provide Cluster Runway and just in time forecasting (What If Planning).

Capacity Runway
...............

Use Prism Central’s Capacity Runway feature to learn about cluster resource planning and recommendations.

.. -----------------------Begin---------------------------------------------
.. Put this in if running on version 5.11

.. #. In **Prism Central >** :fa:`align-justify` **> Operations > Planning > Capacity Runway**

.. -----------------------End---------------------------------------------

.. -----------------------Begin---------------------------------------------
.. Remove the following line

#. In **Prism Central > Planning > Capacity Runway**.

.. -----------------------End---------------------------------------------
- Note the runway summaries showing the days left for each cluster.
- How long does the current cluster has before it runs out of memory, CPU, and storage?

#. Click one of the clusters.

.. note::

  The most constrained resource is highlighted on the left side.

.. note::

  Clicking Storage, CPU, or Memory Runway displays the chart for that resource.

#. Click **Optimize Resources** to see a list of recommended management tasks for reallocating resources, such as optimizing over-provisioned VMs, deleting inactive VMs, or adding resources to constrained VMs.

#. Close the Capacity Runway view.

What If Planning
................

#. Push the initial guess of the capacity planning task to add hypothetical workloads and see how the prediction changes.

.. -----------------------Begin---------------------------------------------
.. Put this in if running on version 5.11

.. #. In **Prism Central >** :fa:`align-justify` **> Operations > Planning > Scenarios**, then click **New Scenario**

.. -----------------------End---------------------------------------------

.. -----------------------Begin---------------------------------------------
.. Remove the following line

#. In **Prism Central > Planning > Scenarios**, then click **New Scenario**.

.. -----------------------End---------------------------------------------

#. Next, fill out the following fields:

.. -----------------------Begin---------------------------------------------
.. Change the following line
- **Cluster** - Select a Cluster Model
.. into - **CLUSTER** - Select a cluster of your choice
.. -----------------------End---------------------------------------------
- **Target** - 6 months

.. -----------------------Begin---------------------------------------------
.. Remove the following line
- **Vendor Type** - Nutanix
.. -----------------------End---------------------------------------------

#. Now lets add a 150 seat Citrix XenDesktop workload..

.. -----------------------Begin---------------------------------------------
.. Change the following line

#. Click **+ Add Workload**.

.. into
.. #. Click **Workload Add/Adjust**
.. -----------------------End---------------------------------------------

#. Next, fill out the following fields and click **Add Workload**:

- **Workload** - VDI
- **Vendor** - XenDesktop
- **User Type** - Power Users
- **Provision Type** - Machine Creation Services (MCS)
- **Number of Users** - 150
- **On** - One Month from now

#. Repeat this process, adding workloads until the runway falls short of the six-month target.

#. **Save** this scenario.

#. Note the **Resources** section, which shows the existing hardware.

#. Click **Recommend** to see a suggested NX configuration to extend the runway.

#. Now lets experiment with changing the target and workloads and generating recommendations:

- Additional 150 seats in three months.
- Change in demand every three months.

#. Generate a PDF report to see detailed capacity planning information.

Takeaways
+++++++++

- The Capacity Runway view in the Planning dashboard allows you to view summary resource runway information for the registered clusters and access detailed runway information about each cluster.
- The Scenarios view in the Planning dashboard allows you to create "what if" scenarios to assess the future resource requirements for potential work loads that you specify.
- You must have a Prism Pro license to use the resource planning tools.

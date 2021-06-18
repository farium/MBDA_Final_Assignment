# EPA-simmodel
The folder contains 8 notebooks, which are named and ordered based on the analysis steps that are taken.
The first step is Problem Formulation, which is not a notebook but a python file named "problem_formulation.py".
In the python file, a problem formulation was added using id 6. 
This problem formulation is used throughout the notebooks to generate scenarios and outcomes.

The next step taken was exploration, marked by the first letter "E".
This is then split into three notebooks;
E.1 is the generation of scenarios with all policies set to 0, therefore called Zero Policy
    This notebook creates the files 'results_exploration.tar.gz' with 1000 scenarios,
    and 'full_results_exploration.tar.gz' with 10000 scenarios that is later used.
E.2 contains several visualizations of the results from E.1
E.3 generates scenarios for each policy individually active. The results are also visualized in this notebook.
    This notebook creates the files 'iso_rfr.tar.gz' that contains the data for isolated rfr policies,
    'iso_dikes.tar.gz' that contains the data for isolated dike policies,
    and 'iso_ews.tar.gz' that contains the data for isolated ews policies.

The next step was generation of policies until a satisficing set of outcomes was found, marked by the letters "PG".
This is split into four notebooks;
PG.1 creates scenarios where all Room for the River policies are active.
   The file created are called 'full_rfr_policy.tar.gz' for the one with all rfr policies, 
   and 'ews_rfr_policies.tar.gz' for the data with a combination of all rfr and differing ews
PG.2 creates scenarios where dikes are heightened to different values at all locations simultaneously.
    The file created is called 'full_dike_policies.tar.gz'
PG.3 combines RfR projects with dikes into new policies, where in the final step values were iterated until the result was satisficing.
    The first file created is called 'efficient_rfr.tar.gz', which contains data of 3 different combinations of rfr policies
    The next file 'rfr_dikes.tar.gz' combines rfr policies with dikes
    The file 'best_policy.tar.gz' has the data in which a combination is chosen with good results
    The last file 'best_policy_ews.tar.gz' combines the above policy with 4 ews day options
PG.4 uses the final policy from PG.3, and runs it with 10000 scenarios to check for robustness. The various outcomes are visualized.
    The file 'final_policy.tar.gz' is saved which takes the policy from best_policy_ews with 2 days ews, and is run for 10000 scenarios

The last step was scenario discovery, marked by the letters "SD".
SD.1 contains the scenario discovery step by applying Prim analysis to data from PG.4 and visualizes this.

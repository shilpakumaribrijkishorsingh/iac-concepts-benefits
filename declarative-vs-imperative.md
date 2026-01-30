# Declarative vs. Imperative Approaches in IaC

## Declarative Approach
The **Declarative** approach focuses on **what** the eventual target configuration should look like. You define the desired end state, and the tool figures out how to achieve it.
* **Example:** Terraform, AWS CloudFormation, Kubernetes manifests.
* **Pros:** * Easier to manage at scale.
    * **Idempotent:** Running the same code multiple times results in the same state without unintended side effects.
    * Less complex for the user to write.

## Imperative Approach
The **Imperative** approach focuses on **how** the infrastructure should be changed. It involves writing step-by-step scripts or commands that must be executed in a specific order.
* **Example:** Bash scripts, AWS CLI, Python scripts using Boto3.
* **Pros:** * Offers precise control over the exact sequence of events.
    * Can be more intuitive for those with a traditional programming background.
* **Cons:** * Harder to maintain as infrastructure grows.
    * Not naturally idempotent (running the script twice might cause errors or duplicate resources).

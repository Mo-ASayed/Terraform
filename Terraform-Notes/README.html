<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Terraform Notes</title>
</head>
<body>
    <h1>Terraform Notes</h1>

    <p>Terraform is all about <strong>infrastructure as code</strong>. It helps you define your infrastructure with code so you can version, track, and deploy it easily. Here's a quick walk-through of the basics to advanced bits.</p>

    <h2>1. Getting Started</h2>

    <p>Start with the basic commands that you'll always use.</p>

    <h3><code>terraform init</code></h3>
    <ul>
        <li><strong>Purpose:</strong> Prepares the working directory with the necessary plugins.</li>
        <li><strong>Run it:</strong> First thing you do when you set up a new Terraform project.</li>
    </ul>
    <pre><code>terraform init</code></pre>

    <h3><code>terraform plan</code></h3>
    <ul>
        <li><strong>Purpose:</strong> Checks what Terraform will do before actually doing it.</li>
        <li>Shows you what resources will be created, modified, or destroyed.</li>
        <li><strong>Pro Tip:</strong> Run this often, especially before <code>apply</code>.</li>
    </ul>
    <pre><code>terraform plan</code></pre>

    <h3><code>terraform apply</code></h3>
    <ul>
        <li><strong>Purpose:</strong> Actually applies your changes to the infrastructure.</li>
        <li>Runs the plan and then does the work.</li>
    </ul>
    <pre><code>terraform apply</code></pre>

    <h3>Table of Basic Commands:</h3>

    <table border="1">
        <tr>
            <th>Command</th>
            <th>Purpose</th>
        </tr>
        <tr>
            <td><code>terraform init</code></td>
            <td>Sets up the environment with plugins</td>
        </tr>
        <tr>
            <td><code>terraform plan</code></td>
            <td>Shows the execution plan</td>
        </tr>
        <tr>
            <td><code>terraform apply</code></td>
            <td>Executes the plan and applies changes</td>
        </tr>
        <tr>
            <td><code>terraform destroy</code></td>
            <td>Tears down the infrastructure</td>
        </tr>
    </table>

    <h2>2. Getting into Resource Blocks</h2>

    <p>Resource blocks are where you define <em>what</em> you want Terraform to manage.</p>
    <pre><code>resource "aws_instance" "example" {
    ami           = "ami-12345678"
    instance_type = "t2.micro"
}</code></pre>

    <ul>
        <li><strong>Resource Type:</strong> First part, <code>aws_instance</code>.</li>
        <li><strong>Name:</strong> The second part, <code>"example"</code>, is your reference name.</li>
        <li><strong>Arguments:</strong> Define the attributes like <code>ami</code> and <code>instance_type</code>.</li>
    </ul>

    <p>The cool part? This block is declarative, so Terraform will always aim to make your infra match it.</p>

    <h3>Variables</h3>
    <ul>
        <li>You can use variables to make your configuration more flexible.</li>
        <li>Defined like this:</li>
    </ul>
    <pre><code>variable "instance_type" {
    default = "t2.micro"
}</code></pre>

    <p>And used in your resource block like this:</p>
    <pre><code>instance_type = var.instance_type</code></pre>

    <h2>3. Moving on to Imports</h2>

    <p>Sometimes you want Terraform to manage something <strong>already created</strong>. Instead of recreating it, you can import it.</p>

    <h3><code>terraform import</code></h3>
    <ul>
        <li><strong>Purpose:</strong> Bring existing resources under Terraform management.</li>
        <li><strong>Usage:</strong></li>
    </ul>
    <pre><code>terraform import aws_instance.example i-0123456789abcdef0</code></pre>

    <p>This will import the <code>i-0123456789abcdef0</code> instance into your <code>aws_instance.example</code> resource block.</p>

    <h2>4. Replacing Resources</h2>

    <p>Every now and then, you might want to replace a resource entirely, for instance, when upgrading.</p>

    <h3><code>terraform taint</code> (old command)</h3>
    <p>Marks a resource for replacement on the next apply.</p>
    <pre><code>terraform taint aws_instance.example</code></pre>

    <h3><code>terraform apply -replace</code></h3>
    <p>Modern, cleaner way to force a resource to be replaced without marking it tainted.</p>
    <pre><code>terraform apply -replace="aws_instance.example"</code></pre>

    <h2>5. Modules: Keeping It DRY</h2>

    <p>As your infrastructure grows, you'll want to <strong>reuse configurations</strong>. That's where <strong>modules</strong> come in.</p>

    <h3>Why Use Modules?</h3>
    <ul>
        <li>Makes your Terraform code modular and easy to manage.</li>
        <li>Can reuse common patterns, like VPC creation, across multiple environments.</li>
    </ul>

    <h3>Example:</h3>
    <p>Here’s how a basic module setup works:</p>
    <pre><code>module "vpc" {
    source = "./modules/vpc"
    cidr_block = "10.0.0.0/16"
}</code></pre>

    <ul>
        <li><strong>source:</strong> Path to the module (could be local or remote).</li>
        <li><strong>cidr_block:</strong> A variable you're passing to the module.</li>
    </ul>

    <p>Modules keep your infrastructure configuration neat and repeatable.</p>

    <h2>6. Advanced Command - Graph</h2>

    <p>For visual learners, Terraform has a <strong>graph</strong> command that shows the dependency graph of your infrastructure.</p>
    <pre><code>terraform graph | dot -Tpng > graph.png</code></pre>

    <p>This can give you an actual image of how your resources relate to each other.</p>

    <h2>7. Wrapping Up</h2>

    <p>Terraform is all about defining your infrastructure, but it’s also about making sure it’s reproducible and easy to manage. Whether you're just getting started with <code>plan</code> and <code>apply</code>, or using advanced tricks like <code>import</code>, <strong>understanding the basics</strong> will make your life easier.</p>

    <ul>
        <li><strong>Modules</strong> help you stay DRY.</li>
        <li><strong>Plan often</strong>, and always check what you’re about to apply.</li>
        <li><strong>Import</strong> lets you bring in existing resources without hassle.</li>
        <li>Use <strong>replace</strong> and <strong>taint</strong> carefully when you want to recreate resources.</li>
    </ul>

    <p>Feel free to add on top of this or tweak it for your own workflow. Happy Terraforming!</p>
</body>
</html>

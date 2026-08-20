# srsg-processes
Please note that this document is a work in progress.

## How to Build the SRSG Processes Jupyter Book Locally

1. Open a terminal and clone the repository `git clone git@github.com:Southampton-RSG/srsg-processes.git`
2. Change into the srsg-processes directory `cd srsg-processes`
3. Create a virtual environment `python -m venv venv`, activate it `source venv/bin/activate` (`source venv/Scripts/activate` for Windows) and install the requirements into it `pip install -r requirements.txt`
4. Run the command `jupyter-book build srsg-processes/` this will create the html files in the _build subdirectory.
5. Open the html file srsg-processes/_build/html/index.html using whichever method you would usually use to open html files e.g. VSCode Live Server 

For more information about Jupyter Book, the 'get started', 'author content' and 'build and publish' sections of the documentation are very helpful: [https://jupyterbook.org/stable](https://jupyterbook.org/stable)

## How to Edit using the GitHub Interface

To make changes follow these steps:

1. Navigate to the `srsg-processes` folder.
2. Open the specific section you want to edit, such as `section_1.md`.
3. Click the pencil icon in the upper-right corner (hovering over it will display "Edit this file").
4. Modify the content as needed, ensuring you use proper Markdown formatting. For a Markdown guide, refer to [Markdown Guide](https://www.markdownguide.org/).
5. Click on **Commit changes**.
6. Enter a brief commit message summarizing your update, such as "Update organizational chart with new staff member." If needed, provide additional details in the 'Extended description' box.
7. Verify that the option **Commit directly to the main branch** is selected.
8. Click **Commit changes**. Your updates will appear in the handbook within a few minutes.

All proposed and actual changes must follow the [Terms of Reference for the Process Working Group](./srsg-processes/context_of_the_organisation/tor_process_working_group.md).
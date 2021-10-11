The `GITHUB_TOKEN` secret is set to an access token for the repository each time a job in a workflow begins. {% ifversion fpt or ghes > 3.1 or ghae-next %}You should set the permissions for this access token in the workflow file to grant read access for the `contents` scope and write access for the `packages` scope. {% else %}It has read and write permissions for packages in the repository where the workflow runs. {% endif %}For more information, see "[Authenticating with the GITHUB_TOKEN](/actions/configuring-and-managing-workflows/authenticating-with-the-github_token)."
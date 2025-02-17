---
title: Changing your GitHub username
intro: 'You can change the username for your account on {% ifversion fpt or ghec %}{% data variables.product.prodname_dotcom_the_website %}{% elsif ghes %}{% data variables.location.product_location %} if your instance uses built-in authentication{% endif %}.'
redirect_from:
  - /articles/how-to-change-your-username
  - /articles/changing-your-github-user-name
  - /articles/renaming-a-user
  - /articles/what-happens-when-i-change-my-username
  - /articles/changing-your-github-username
  - /github/setting-up-and-managing-your-github-user-account/changing-your-github-username
  - /github/setting-up-and-managing-your-github-user-account/managing-user-account-settings/changing-your-github-username
  - /account-and-profile/setting-up-and-managing-your-github-user-account/managing-user-account-settings/changing-your-github-username
versions:
  fpt: '*'
  ghes: '*'
  ghec: '*'
topics:
  - Accounts
shortTitle: Change your username
---

{% ifversion ghec or ghes %}

{% note %}

{% ifversion ghec %}

**Note**: Members of an {% data variables.enterprise.prodname_emu_enterprise %} cannot change usernames. Your enterprise's IdP administrator controls your username for {% data variables.product.product_name %}. For more information, see "[AUTOTITLE](/admin/identity-and-access-management/using-enterprise-managed-users-for-iam/about-enterprise-managed-users)."

{% elsif ghes %}

**Note**: If you sign into {% data variables.location.product_location %} with LDAP credentials or single sign-on (SSO), only your local administrator can change your username. For more information about authentication methods for {% data variables.product.product_name %}, see "[AUTOTITLE](/admin/identity-and-access-management/managing-iam-for-your-enterprise)."

{% endif %}

{% endnote %}

{% endif %}

## About username changes

You can change your username to another username that is not currently in use.{% ifversion fpt or ghec %} If the username you want is not available, consider other names or unique variations. Using a number, hyphen, or an alternative spelling might help you find a similar username that's still available.

If you hold a trademark for the username, you can find more information about making a trademark complaint on our [Trademark Policy](/free-pro-team@latest/site-policy/content-removal-policies/github-trademark-policy) page.

If you do not hold a trademark for the name, you can choose another username or keep your current username. {% data variables.contact.github_support %} cannot release the unavailable username for you. For more information, see "[Changing your username](#changing-your-username)."{% endif %}

After changing your username, your old username becomes available for anyone else to claim. Most references to your repositories under the old username automatically change to the new username. However, some links to your profile won't automatically redirect.

{% data variables.product.product_name %} cannot set up redirects for:
- [@mentions](/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#mentioning-people-and-teams) using your old username
- Links to [gists](/get-started/writing-on-github/editing-and-sharing-content-with-gists/creating-gists) that include your old username

{% ifversion fpt or ghec %}

If you're a member of an {% data variables.enterprise.prodname_emu_enterprise %}, you cannot make changes to your username. {% data reusables.enterprise-accounts.emu-more-info-account %}

{% endif %}

{% ifversion fpt or ghec %}

{% data reusables.accounts.rename-account-repo-namespace-retirement %} If you try to create a repository using a retired owner name and repository name combination, you will see the error: "The repository `<REPOSITORY_NAME>` has been retired and cannot be reused."

{% endif %}

{% data reusables.package_registry.rename-account-namespace-retirement %}

## Repository references

After you change your username, {% data variables.product.product_name %} will automatically redirect references to your repositories.
- Web links to your existing repositories will continue to work. This can take a few minutes to complete after you make the change.
- Command line pushes from your local repository clones to the old remote tracking URLs will continue to work.

If the new owner of your old username creates a repository with the same name as your repository, that will override the redirect entry and your redirect will stop working. Because of this possibility, we recommend you update all existing remote repository URLs after changing your username. For more information, see "[AUTOTITLE](/get-started/getting-started-with-git/managing-remote-repositories)."

## Links to your previous profile page

After changing your username, links to your previous profile page, such as `https://{% data variables.command_line.backticks %}/previoususername`, will return a 404 error. We recommend updating any links to your account on {% data variables.location.product_location %} from elsewhere{% ifversion fpt or ghec %}, such as your LinkedIn or Twitter profile{% endif %}.

## Your Git commits

{% ifversion fpt or ghec %}Git commits that were associated with your {% data variables.product.product_name %}-provided `noreply` email address won't be attributed to your new username and won't appear in your contributions graph.{% endif %} If your Git commits are associated with another email address you've [added to your GitHub account](/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/adding-an-email-address-to-your-github-account), {% ifversion fpt or ghec %}including the ID-based {% data variables.product.product_name %}-provided `noreply` email address, {% endif %}they'll continue to be attributed to you and appear in your contributions graph after you've changed your username. For more information on setting your email address, see "[AUTOTITLE](/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/setting-your-commit-email-address)."

## Your gists

After changing your username, the URLs to any public or secret gists will also change and previous links to these will return a 404 error. We recommend updating the links to these gists anywhere you may have shared them.

## CODEOWNERS files

After changing your username, CODEOWNERS files that include your old username will need to be manually updated. When you view the CODEOWNERS files on {% data variables.product.prodname_dotcom_the_website %}, an error message is displayed if the file contains any unknown users, or users without write access. We recommend updating all relevant CODEOWNERS files with your new username. For more information, see "[AUTOTITLE](/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners)."

## Changing your username

{% data reusables.user-settings.access_settings %}
{% data reusables.user-settings.account_settings %}
3. In the "Change username" section, click **Change username**.{% ifversion fpt or ghec %}
4. Read the warnings about changing your username. If you still want to change your username, click **I understand, let's change my username**.
5. Type a new username.
6. If the username you've chosen is available, click **Change my username**. If the username you've chosen is unavailable, you can try a different username or one of the suggestions you see.
{% endif %}

## Further reading

- "[AUTOTITLE](/pull-requests/committing-changes-to-your-project/troubleshooting-commits/why-are-my-commits-linked-to-the-wrong-user)"{% ifversion fpt or ghec %}
- "[AUTOTITLE](/free-pro-team@latest/site-policy/other-site-policies/github-username-policy)"{% endif %}

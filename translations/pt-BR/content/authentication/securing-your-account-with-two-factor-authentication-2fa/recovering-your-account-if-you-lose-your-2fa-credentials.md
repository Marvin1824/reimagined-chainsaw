---
title: Recuperar sua conta ao perder as credenciais 2FA
intro: 'Se você perder acesso às suas credenciais de autenticação de dois fatores, você poderá usar seus códigos de recuperação ou outra opção de recuperação, para recuperar o acesso à sua conta.'
redirect_from:
  - /articles/recovering-your-account-if-you-lost-your-2fa-credentials/
  - /articles/authenticating-with-an-account-recovery-token/
  - /articles/recovering-your-account-if-you-lose-your-2fa-credentials
  - /github/authenticating-to-github/recovering-your-account-if-you-lose-your-2fa-credentials
  - /github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa/recovering-your-account-if-you-lose-your-2fa-credentials
versions:
  fpt: '*'
  ghes: '*'
  ghec: '*'
topics:
  - 2FA
shortTitle: Recuperar uma conta com 2FA
---

{% ifversion fpt or ghec %}

{% warning %}

**Aviso**: {% data reusables.two_fa.support-may-not-help %}

{% endwarning %}

{% endif %}

## Usar um código de recuperação da autenticação de dois fatores

Use um dos códigos de recuperação para obter acesso automaticamente à sua conta. Seus códigos de recuperação podem estar salvos em um gerenciador de senhas ou na pasta de downloads do seu computador. O nome padrão do arquivo de códigos de recuperação é `github-recovery-codes.txt`. Para obter mais informações sobre códigos de recuperação, consulte "[Configurar métodos de recuperação da autenticação de dois fatores](/articles/configuring-two-factor-authentication-recovery-methods#downloading-your-two-factor-authentication-recovery-codes)".

{% data reusables.two_fa.username-password %}{% ifversion fpt or ghec %}
2. Em "Encontrou algum problema?", clique em **Insira um código de recuperação de dois fatores**. ![Link to use a recovery code](/assets/images/help/2fa/2fa-recovery-code-link.png){% else %}
2. Na página da 2FA, em "Don't have your phone?" (Não está com seu telefone?), clique em **Enter a two-factor recovery code** (Digite um código de recuperação de dois fatores). ![Link to use a recovery code](/assets/images/help/2fa/2fa_recovery_dialog_box.png){% endif %}
3. Digite um dos seus códigos de recuperação e clique em **Verify** (Verificar). ![Campo para digitar um código de recuperação e botão Verify (Verificar)](/assets/images/help/2fa/2fa-type-verify-recovery-code.png)

{% ifversion fpt or ghec %}
## Autenticar com um número de telefone alternativo

Se você perder o acesso ao seu aplicativo TOTP principal ou número de telefone, é possível fornecer um código de autenticação de dois fatores enviado para seu número de telefone alternativo e conseguir acessar automaticamente sua conta.
{% endif %}

## Autenticar com uma chave de segurança

Se você configurou a autenticação de dois fatores com uma chave de segurança, você pode usar a chave de segurança como método de autenticação secundário para reaver automaticamente o acesso à sua conta. Para obter mais informações, consulte "[Configurar autenticação de dois fatores](/articles/configuring-two-factor-authentication#configuring-two-factor-authentication-using-a-security-key)".

{% ifversion fpt or ghec %}
## Efetuar a autenticação com um dispositivo verificado, token SSH ou token de acesso pessoal

Se você sabe sua senha do {% data variables.product.product_name %} mas não tem credenciais de autenticação de dois fatores ou seus códigos de recuperação de autenticação de dois fatores, você pode ter uma senha única enviada para o seu endereço de e-mail verificado para começar o processo de verificação e recuperar o acesso à sua conta.

{% note %}

**Observação**: Por razões de segurança, recuperar o acesso à sua conta efetuando a autenticação com uma senha única pode levar de 3 a 5 dias úteis. Os pedidos adicionais enviados durante este período não serão revisados.

{% endnote %}

Você pode usar as suas credenciais de autenticação de dois fatores ou os códigos de recuperação de dois fatores para recuperar o acesso à sua conta a qualquer momento no período de espera de 3 a 5 dias.

1. Digite seu nome de usuário e senha para solicitar autenticação. Se você não sabe sua senha de {% data variables.product.product_name %}, você não poderá gerar uma senha única.
2. Em "Encontrou algum problema?", clique em **Não consegue acessar seu dispositivo de dois fatores ou códigos de recuperação válidos?** ![Faça o link, se você não tiver seu dispositivo de 2FA ou códigos de recuperação](/assets/images/help/2fa/no-access-link.png)
3. Clique em **Eu entendo, começar** para solicitar uma redefinição das suas configurações de autenticação. ![Botão de redefinição da configuração de autenticação](/assets/images/help/2fa/reset-auth-settings.png)
4. Clique em **Enviar senha de uso único** para enviar uma senha de uso único para todos os endereços de e-mail associados à sua conta. ![Botão para enviar a senha de uso único](/assets/images/help/2fa/send-one-time-password.png)
5. Em "Única senha", digite a senha temporária do endereço e-mail de recuperação {% data variables.product.prodname_dotcom %} enviada. ![Campo para a senha de uso único](/assets/images/help/2fa/one-time-password-field.png)
6. Clique **Verificar endereço de e-mail**.
7. Escolha um fator de verificação alternativo.
    - Se você usou seu dispositivo atual para acessar essa conta antes e gostaria de usar o dispositivo para verificação, clique em **Verificar com este dispositivo**.
    - Se você já configurou uma chave SSH nesta conta e gostaria de usar a chave SSH para verificação, clique na **chave SSH**.
    - Se você já configurou um token de acesso pessoal anteriormente e gostaria de usar o token de acesso pessoal para verificação, clique em **Token de acesso pessoal**. ![Botões de verificação alternativa](/assets/images/help/2fa/alt-verifications.png)
8. Um integrante do {% data variables.contact.github_support %} irá rever a sua solicitação e o seu endereço de e-mail de 3 a 5 dias úteis. Se a sua solicitação for aprovada, você receberá um link para concluir o processo de recuperação de conta. Se sua solicitação for negada, o e-mail incluirá uma forma de entrar em contato com o suporte para esclarecer outras dúvidas.

## Autenticar com um token de recuperação de conta

{% warning %}

**Aviso:** Os tokens de recuperação de conta estão obsoletos e serão desabilitados em **de 1 de dezembro de 2021 de**. Certifique-se de ter configurado outros métodos de recuperação de dois fatores. Para obter mais informações, consulte "[Configurando métodos de recuperação de autenticação de dois fatores](/articles/configuring-two-factor-authentication-recovery-methods)".

{% endwarning %}

Se você perder o acesso aos métodos de autenticação de dois fatores para sua conta em {% data variables.product.product_location %}, você poderá recuperar seu token de recuperação de conta de um provedor de recuperação de parceiro e pedir para o suporte de {% data variables.product.prodname_dotcom %} revisá-lo.

Se você não tiver acesso aos seus métodos de autenticação de dois fatores ou códigos de recuperação e tiver armazenado um token de recuperação de conta no Facebook usando a recuperação de contas em outro lugar, pode ser que você consiga usar seu token para recuperar o acesso à sua conta.

Se você não conseguir recuperar o acesso à sua conta, gere uma de uso único para recuperar o acesso. Para obter mais informações, consulte "[Efetuar a autenticação com um dispositivo verificado, token SSH ou token de acesso pessoal](#authenticating-with-a-verified-device-ssh-token-or-personal-access-token)".

{% warning %}

**Avisos:**
- Antes de acessar um token de recuperação de conta, tente usar seus [códigos de autenticação de dois fatores](/articles/accessing-github-using-two-factor-authentication) ou seus códigos de recuperação da autenticação de dois fatores para reaver o acesso à sua conta. Para obter mais informações, consulte "[Recuperar sua conta se você perder as credenciais da 2FA](/articles/recovering-your-account-if-you-lose-your-2fa-credentials)".

{% endwarning %}

1. No Facebook, acesse [Security Settings](https://www.facebook.com/settings?tab=security) (Configurações de segurança) e clique em **Recover Accounts Elsewhere** (Recuperação de contas em outro lugar). ![Página de configurações de segurança do Facebook com link Recuperação de contas em outro lugar](/assets/images/help/settings/security-facebook-security-settings-page.png)
2. Clique no token de recuperação associado à sua conta em {% data variables.product.product_location %}. ![Lista de tokens de recuperação armazenados no Facebook](/assets/images/help/settings/security-github-rae-token-on-facebook.png)
3. Para acessar seu token de recuperação de conta, clique em **Recover This Account** (Recuperar esta conta). Uma nova janela abrirá, retornando ao {% data variables.product.product_name %}. ![Caixa modal com informações sobre seu token de recuperação e botão Recover This Account (Recuperar esta conta)](/assets/images/help/settings/security-recover-account-facebook.png)
4. Entre em contato com o {% data variables.contact.contact_support %} para informá-los que seu token de recuperação de conta está pronto para ser verificado.
{% endif %}

## Leia mais

- [Sobre a autenticação de dois fatores](/articles/about-two-factor-authentication)"
- "[Configurar a autenticação de dois fatores](/articles/configuring-two-factor-authentication)"
- "[Configurar métodos de recuperação de autenticação de dois fatores](/articles/configuring-two-factor-authentication-recovery-methods)"
- "[Acessar o {% data variables.product.prodname_dotcom %} usando a autenticação de dois fatores](/articles/accessing-github-using-two-factor-authentication)"
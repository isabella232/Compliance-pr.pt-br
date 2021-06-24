---
title: RGPD
description: Orientação técnica da Microsoft — CONJUNTO DE FERRAMENTAS DE MIGRAÇÕES FASTTRACK PARA ENVIAR SOLICITAÇÃO DE EXCLUSÃO
keywords: Migração FastTrack, Microsoft 365 Education, documentação do Microsoft 365, RGPD
localization_priority: Priority
Robots: NOFOLLOW,NOINDEX
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: mohitku
author: MohitKumar
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft GDPR
hideEdit: true
ms.openlocfilehash: d3429d3fb35317146e32fddc71bae2f12c40269d
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089504"
---
# <a name="fasttrack-migration-toolset-for-submitting-delete-request"></a><span data-ttu-id="34ce1-104">Conjunto de ferramentas de migração FastTrack para envio de solicitação de exclusão</span><span class="sxs-lookup"><span data-stu-id="34ce1-104">FastTrack Migration Toolset for Submitting Delete Request</span></span>

## <a name="toolset-purpose"></a><span data-ttu-id="34ce1-105">Finalidade do conjunto de ferramentas</span><span class="sxs-lookup"><span data-stu-id="34ce1-105">Toolset purpose</span></span>

<span data-ttu-id="34ce1-p101">Se você for um cliente envolvido atualmente com migrações FastTrack, a exclusão da conta de usuário não excluirá a cópia dos dados em posse da equipe do Microsoft FastTrack, mantida apenas para a conclusão da migração. Se, durante a migração, você quiser que a equipe do Microsoft FastTrack também exclua a cópia dos dados, envie uma solicitação por esse conjunto de ferramentas. No curso normal dos negócios, o Microsoft FastTrack excluirá todas as cópias dos dados após a conclusão da migração.</span><span class="sxs-lookup"><span data-stu-id="34ce1-p101">In the event that you are a customer currently engaged in FastTrack migrations, deleting the user account will not delete the data copy held by the Microsoft FastTrack team, which is held for the sole purpose of completing the migration. If during the migration you would like the Microsoft FastTrack team to also delete the data copy, submit a request via this tool set. In the ordinary course of business, Microsoft FastTrack will delete all data copies once the migration is complete.</span></span>

### <a name="supported-platforms"></a><span data-ttu-id="34ce1-109">Plataformas compatíveis</span><span class="sxs-lookup"><span data-stu-id="34ce1-109">Supported platforms</span></span>

<span data-ttu-id="34ce1-p102">A Microsoft oferece suporte à versão inicial deste conjunto de ferramentas na plataforma do Windows e no console do PowerShell. Este conjunto de ferramentas oferece suporte às plataformas conhecidas a seguir:</span><span class="sxs-lookup"><span data-stu-id="34ce1-p102">Microsoft supports the initial release of this  toolset in the Windows platform and PowerShell console. The following known platforms are supported by this toolset:</span></span>

<span data-ttu-id="34ce1-112">\***Tabela 1 - Plataformas compatíveis com este conjunto de ferramentas** _</span><span class="sxs-lookup"><span data-stu-id="34ce1-112">\***Table 1 — Platforms supported by this toolset** _</span></span>

<span data-ttu-id="34ce1-113">_\*\*\*</span><span class="sxs-lookup"><span data-stu-id="34ce1-113">_\*\*\*</span></span>

|<span data-ttu-id="34ce1-114">Versão do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="34ce1-114">PowerShell version</span></span>|<span data-ttu-id="34ce1-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="34ce1-115">Windows 7</span></span>|<span data-ttu-id="34ce1-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="34ce1-116">Windows 8</span></span>|<span data-ttu-id="34ce1-117">Windows 10</span><span class="sxs-lookup"><span data-stu-id="34ce1-117">Windows 10</span></span>|<span data-ttu-id="34ce1-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="34ce1-118">Windows Server 2012</span></span>|<span data-ttu-id="34ce1-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="34ce1-119">Windows Server 2016</span></span>|
|:---:|:---:|:---:|:---:|:---:|:---:|
|<span data-ttu-id="34ce1-120">5.0</span><span class="sxs-lookup"><span data-stu-id="34ce1-120">5.0</span></span>|<span data-ttu-id="34ce1-121">Não suportado</span><span class="sxs-lookup"><span data-stu-id="34ce1-121">Not Supported</span></span>|<span data-ttu-id="34ce1-122">Com suporte</span><span class="sxs-lookup"><span data-stu-id="34ce1-122">Supported</span></span>|<span data-ttu-id="34ce1-123">Com suporte</span><span class="sxs-lookup"><span data-stu-id="34ce1-123">Supported</span></span>|<span data-ttu-id="34ce1-124">Com suporte</span><span class="sxs-lookup"><span data-stu-id="34ce1-124">Supported</span></span>|<span data-ttu-id="34ce1-125">Com suporte</span><span class="sxs-lookup"><span data-stu-id="34ce1-125">Supported</span></span>|
|<span data-ttu-id="34ce1-126">5.1</span><span class="sxs-lookup"><span data-stu-id="34ce1-126">5.1</span></span>|<span data-ttu-id="34ce1-127">Não suportado</span><span class="sxs-lookup"><span data-stu-id="34ce1-127">Not Supported</span></span>|<span data-ttu-id="34ce1-128">Com suporte</span><span class="sxs-lookup"><span data-stu-id="34ce1-128">Supported</span></span>|<span data-ttu-id="34ce1-129">Com suporte</span><span class="sxs-lookup"><span data-stu-id="34ce1-129">Supported</span></span>|<span data-ttu-id="34ce1-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="34ce1-130">Supported</span></span>|<span data-ttu-id="34ce1-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="34ce1-131">Supported</span></span>|
|

### <a name="obtaining-the-toolset"></a><span data-ttu-id="34ce1-132">Como obter o conjunto de ferramentas</span><span class="sxs-lookup"><span data-stu-id="34ce1-132">Obtaining the toolset</span></span>

<span data-ttu-id="34ce1-p103">Este conjunto de ferramentas está disponível na Galeria do PowerShell no aplicativo de console do PowerShell. Para localizar e carregar este módulo de cmdlet, primeiro abra o PowerShell no modo de administrador para que ele tenha as permissões apropriadas para instalar o módulo. Se você não usou o PowerShell anteriormente, vá para a Barra de Tarefas do Windows e na caixa de pesquisa digite 'PowerShell ”. Selecione o aplicativo de console usando o botão direito do mouse e escolha **Executar como administrador** e clique em **Sim** para executar o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="34ce1-p103">This toolset is available in the PowerShell Gallery on the PowerShell console application.  To locate and load this cmdlet module, first open PowerShell in administrator mode so it has the appropriate permissions to install the module. If you have not used PowerShell previously go to your Windows Task Bar and in the search box type 'PowerShell”. Select the console app using right-click and choose **Run as administrator**, then click **Yes** to run Windows PowerShell.</span></span>

![PowerShell - Executar como administrador](../media/fasttrack-powershell_image.png)

![PowerShell - Permitir que o aplicativo faça alterações](../media/fasttrack-run-powershell_image.png)

<span data-ttu-id="34ce1-p104">Agora que o console está aberto, você precisa definir as permissões para a execução do script. Digite o seguinte comando para permitir que os scripts sejam executados:</span><span class="sxs-lookup"><span data-stu-id="34ce1-p104">Now that the console is open, you need to set permissions for script execution. Type the following command to allow the scripts to run:</span></span>

```powershell
Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process
```

<span data-ttu-id="34ce1-141">Você receberá uma solicitação para confirmar essa ação, pois o administrador pode alterar o escopo de acordo com seu critério.</span><span class="sxs-lookup"><span data-stu-id="34ce1-141">You will be prompted to confirm this action, as the administrator can change the scope at their discretion.</span></span>

<span data-ttu-id="34ce1-142">\**_Definir a Política de Execução_* _</span><span class="sxs-lookup"><span data-stu-id="34ce1-142">\**_Set Execution Policy_* _</span></span>

![Definir alteração de política de execução no PowerShell](../media/powershell-set-execution-policy_image.png)

<span data-ttu-id="34ce1-144">Agora que o console está configurado para permitir o script, execute o próximo comando para instalar o módulo:</span><span class="sxs-lookup"><span data-stu-id="34ce1-144">Now that the console is set to allow the script, run this next command to install the module:</span></span>

```powershell
Install-Module -Name Microsoft.FastTrack -Repository PSGallery -WarningAction SilentlyContinue -Force
```

### <a name="prerequisites-for-module"></a><span data-ttu-id="34ce1-145">Pré-requisitos para o módulo</span><span class="sxs-lookup"><span data-stu-id="34ce1-145">Prerequisites for module</span></span>

<span data-ttu-id="34ce1-p105">Para executar com êxito este módulo, você precisará instalar módulos dependentes para uso, caso eles ainda não estejam instalados. Talvez seja necessário reiniciar o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="34ce1-p105">To successfully execute this module, you may need to install dependent modules for use if they are not already installed. You may need to restart PowerShell.</span></span>

<span data-ttu-id="34ce1-p106">Para enviar um DSR, você deve primeiro fazer logon usando suas credenciais do Office 365. Inserir as credenciais adequadas validará seu status de administrador global e coletará informações do locatário.</span><span class="sxs-lookup"><span data-stu-id="34ce1-p106">In order to submit a DSR, you must first log in using your Office 365 credentials. Entering the proper credentials will validate your global administrator status and collect tenant information.</span></span>

```powershell
Login-FastTrackAccount -ApiKey <API Key provided by FastTrack MVM>
```

<span data-ttu-id="34ce1-150">Após o logon bem-sucedido, as credenciais e a chave serão armazenadas para uso com os módulos do FastTrack durante o restante da sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="34ce1-150">Once successfully logged in, the credentials and key will be stored for use with FastTrack modules for the remainder of the current PowerShell session.</span></span>

<span data-ttu-id="34ce1-151">Se você precisar se conectar a um ambiente de nuvem que não seja comercial, será necessário adicionar  _-Environment\* ao comando de *Logon* com um dos seguintes ambientes válidos:</span><span class="sxs-lookup"><span data-stu-id="34ce1-151">If you need to connect to a cloud environment, other than commercial, _-Environment\* will need to be added to *Log in* command with one of the following valid environments:</span></span>

- <span data-ttu-id="34ce1-152">AzureCloud</span><span class="sxs-lookup"><span data-stu-id="34ce1-152">AzureCloud</span></span>
- <span data-ttu-id="34ce1-153">AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="34ce1-153">AzureChinaCloud</span></span>
- <span data-ttu-id="34ce1-154">AzureGermanCloud</span><span class="sxs-lookup"><span data-stu-id="34ce1-154">AzureGermanCloud</span></span>
- <span data-ttu-id="34ce1-155">AzureUSGovernmentCloud</span><span class="sxs-lookup"><span data-stu-id="34ce1-155">AzureUSGovernmentCloud</span></span>

```powershell
Login-FastTrackAccount -ApiKey <API Key provided by FastTrack MVM> -Environment <cloud environment>
```

<span data-ttu-id="34ce1-156">Para enviar uma solicitação de DSR, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="34ce1-156">To submit a DSR request, run the following command:</span></span>

```powershell
Submit-FastTrackGdprDsrRequest -DsrRequestUserEmail SubjectUserEmail@mycompany.com
```

<span data-ttu-id="34ce1-p107">Em caso de sucesso, o cmdlet retornará um objeto de ID de transação. Guarde o ID da Transação.</span><span class="sxs-lookup"><span data-stu-id="34ce1-p107">On success, the cmdlet will return a Transaction ID object. Please retain the Transaction ID.</span></span>

#### <a name="checking-the-status-of-a-request-transaction"></a><span data-ttu-id="34ce1-159">Verificar o status da transação de uma solicitação</span><span class="sxs-lookup"><span data-stu-id="34ce1-159">Checking the status of a request transaction</span></span>

<span data-ttu-id="34ce1-160">Execute a seguinte função usando a ID da Transação obtida anteriormente:</span><span class="sxs-lookup"><span data-stu-id="34ce1-160">Run the following function using the previously obtained Transaction ID:</span></span>

```powershell
Get-FastTrackGdprDsrRequest -TransactionID "YourTransactionID"
```

#### <a name="transaction-status-codes"></a><span data-ttu-id="34ce1-161">Códigos de Status da Transação</span><span class="sxs-lookup"><span data-stu-id="34ce1-161">Transaction Status Codes</span></span>

|<span data-ttu-id="34ce1-162">Transação</span><span class="sxs-lookup"><span data-stu-id="34ce1-162">Transaction</span></span>|<span data-ttu-id="34ce1-163">Status</span><span class="sxs-lookup"><span data-stu-id="34ce1-163">Status</span></span>|
|---|---|
|<span data-ttu-id="34ce1-164">**Criado**</span><span class="sxs-lookup"><span data-stu-id="34ce1-164">**Created**</span></span>|<span data-ttu-id="34ce1-165">A solicitação foi criada.</span><span class="sxs-lookup"><span data-stu-id="34ce1-165">Request has been created.</span></span>|
|<span data-ttu-id="34ce1-166">**Falhou**</span><span class="sxs-lookup"><span data-stu-id="34ce1-166">**Failed**</span></span>|<span data-ttu-id="34ce1-167">Falha na criação da solicitação. Envie novamente ou contate o suporte.</span><span class="sxs-lookup"><span data-stu-id="34ce1-167">Request failed to create, please resubmit, or contact support.</span></span>|
|<span data-ttu-id="34ce1-168">**Concluída**</span><span class="sxs-lookup"><span data-stu-id="34ce1-168">**Completed**</span></span>|<span data-ttu-id="34ce1-169">A solicitação foi concluída e corrigida.</span><span class="sxs-lookup"><span data-stu-id="34ce1-169">Request has been completed and sanitized.</span></span>|
|

<!-- original version: **Created**  Request has been created<br/>**Failed** Request failed to create, please resubmit, or contact support<br/>**Completed** Request has been completed and sanitized -->

## <a name="learn-more"></a><span data-ttu-id="34ce1-170">Saiba mais</span><span class="sxs-lookup"><span data-stu-id="34ce1-170">Learn more</span></span>

[<span data-ttu-id="34ce1-171">Central de Confiabilidade da Microsoft</span><span class="sxs-lookup"><span data-stu-id="34ce1-171">Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/privacy/gdpr-overview)

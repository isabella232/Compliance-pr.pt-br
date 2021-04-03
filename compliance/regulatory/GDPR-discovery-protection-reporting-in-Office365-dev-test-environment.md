---
title: Descoberta de RGPD, proteção e relatórios no ambiente de desenvolvimento/teste do Microsoft 365
description: Saiba como configurar e demonstrar informações de identificação pessoal (PII) para GDPR em um ambiente de desenvolvimento/teste do Microsoft 365.
f1.keywords:
- NOCSH
ms.author: bcarter
author: brendacarter
manager: laurawi
audience: ITPro
ms.topic: article
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- M365-security-compliance
- MS-Compliance
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: c2112ce8-1c4b-424f-b200-59e161db2d21
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: a12e8e735df05004e63080f22c3c9b4de5749506
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496656"
---
# <a name="gdpr-discovery-protection-and-reporting-in-the-devtest-environment"></a><span data-ttu-id="e41eb-103">Descoberta de RGPD, proteção e relatórios no ambiente de desenvolvimento/teste</span><span class="sxs-lookup"><span data-stu-id="e41eb-103">GDPR discovery, protection, and reporting in the dev/test environment</span></span>

 <span data-ttu-id="e41eb-104">**Resumo:** demonstre recursos de RGPD no Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e41eb-104">**Summary:** Demonstrate GDPR capabilities in Microsoft 365.</span></span>

<span data-ttu-id="e41eb-105">Este artigo descreve como configurar e demonstrar a descoberta, a proteção e o relatório de informações de identificação pessoal (PII), para a Regulamentação Geral sobre a Proteção de Dados (RGPD) em um ambiente de desenvolvimento/teste do Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e41eb-105">This article describes how you configure and demonstrate personally identifiable information (PII) discovery, protection, and reporting for the General Data Protection Regulation (GDPR) in a Microsoft 365 dev/test environment.</span></span>

## <a name="phase-1-create-and-configure-your-trial-microsoft-365-subscription"></a><span data-ttu-id="e41eb-106">Fase 1: Criar e configurar a sua assinatura de avaliação do Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="e41eb-106">Phase 1: Create and configure your trial Microsoft 365 subscription</span></span>

<span data-ttu-id="e41eb-107">Primeiro, siga as etapas no artigo em [Fase 2 do ambiente de desenvolvimento/teste do Microsoft 365](/Office365/Enterprise/office-365-dev-test-environment#phase-2-create-an-office-365-trial-subscription).</span><span class="sxs-lookup"><span data-stu-id="e41eb-107">First, follow the steps in [Phase 2 of the Microsoft 365 dev/test environment](/Office365/Enterprise/office-365-dev-test-environment#phase-2-create-an-office-365-trial-subscription) article.</span></span>

<span data-ttu-id="e41eb-108">Em seguida, use estas etapas para configurar o gerente de Descoberta Eletrônica:</span><span class="sxs-lookup"><span data-stu-id="e41eb-108">Next, use these steps to configure the eDiscovery manager:</span></span>

1. <span data-ttu-id="e41eb-109">Entre no locatário de avaliação do Microsoft 365 com sua conta de administrador global.</span><span class="sxs-lookup"><span data-stu-id="e41eb-109">Sign in to your Microsoft 365 trial tenant with your global administrator account.</span></span>
2. <span data-ttu-id="e41eb-110">Na home page do Microsoft 365, clique em **segurança e conformidade**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-110">From the Microsoft 365 home page, click **Security & Compliance**.</span></span>
3. <span data-ttu-id="e41eb-111">Na nova guia Segurança e Conformidade, clique em **Permissões** > **Gerenciador de Descoberta Eletrônica**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-111">From the new Security & Compliance tab, click **Permissions** > **eDiscovery Manager**.</span></span>
4. <span data-ttu-id="e41eb-112">Clique em **Editar** para o Gerenciador de Descoberta Eletrônica e clique em **Escolher o Gerenciador de Descoberta Eletrônica**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-112">Click **Edit** for eDiscovery Manager, and then click **Choose eDiscovery Manager**.</span></span>
5. <span data-ttu-id="e41eb-113">Clique em **+ Adicionar**, procure o nome da sua conta do administrador global e adicione sua conta de administrador global como um Gerente de Descoberta Eletrônica.</span><span class="sxs-lookup"><span data-stu-id="e41eb-113">Click **+ Add**, search for your global administrator account name and add your global administrator account as an eDiscovery Manager.</span></span>
6. <span data-ttu-id="e41eb-114">Clique em **Concluir** > **Salvar** > **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-114">Click **Done** > **Save** > **Close**.</span></span>

## <a name="phase-2-add-personally-identifiable-information-to-your-tenant"></a><span data-ttu-id="e41eb-115">Fase 2: Adicionar as informações de identificação pessoal ao seu locatário</span><span class="sxs-lookup"><span data-stu-id="e41eb-115">Phase 2: Add personally identifiable information to your tenant</span></span>

<span data-ttu-id="e41eb-116">Nesta fase, crie um documento com PII para um conjunto de exemplo de números de contas bancárias internacionais (IBANs) e armazene-o em um site do SharePoint Online no ambiente de desenvolvimento/teste do Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e41eb-116">In this phase, you create a document with PII for a set of example International Banking Account Numbers (IBANs) and store it on a SharePoint Online site in your Microsoft 365 dev/test environment.</span></span>

1. <span data-ttu-id="e41eb-117">Abra o Microsoft Word no computador.</span><span class="sxs-lookup"><span data-stu-id="e41eb-117">On your local computer, open Microsoft Word.</span></span>
2. <span data-ttu-id="e41eb-118">Cole a tabela a seguir no arquivo do Word e salve-a como ‘IBANs.docx’ no computador local.</span><span class="sxs-lookup"><span data-stu-id="e41eb-118">Paste the following table in the Word file and save it as 'IBANs.docx' on your local computer.</span></span>

   |<span data-ttu-id="e41eb-119">Número</span><span class="sxs-lookup"><span data-stu-id="e41eb-119">Number</span></span>|<span data-ttu-id="e41eb-120">País</span><span class="sxs-lookup"><span data-stu-id="e41eb-120">Country</span></span>|<span data-ttu-id="e41eb-121">Código</span><span class="sxs-lookup"><span data-stu-id="e41eb-121">Code</span></span>|<span data-ttu-id="e41eb-122">IBAN</span><span class="sxs-lookup"><span data-stu-id="e41eb-122">IBAN</span></span>|
   |---|---|---|---|
   |<span data-ttu-id="e41eb-123">1</span><span class="sxs-lookup"><span data-stu-id="e41eb-123">1</span></span>|<span data-ttu-id="e41eb-124">SEPA Áustria</span><span class="sxs-lookup"><span data-stu-id="e41eb-124">Austria SEPA</span></span>|<span data-ttu-id="e41eb-125">AT</span><span class="sxs-lookup"><span data-stu-id="e41eb-125">AT</span></span>|<span data-ttu-id="e41eb-126">AT611904300234573201</span><span class="sxs-lookup"><span data-stu-id="e41eb-126">AT611904300234573201</span></span>|
   |<span data-ttu-id="e41eb-127">2</span><span class="sxs-lookup"><span data-stu-id="e41eb-127">2</span></span>|<span data-ttu-id="e41eb-128">SEPA Bulgária</span><span class="sxs-lookup"><span data-stu-id="e41eb-128">Bulgaria SEPA</span></span>|<span data-ttu-id="e41eb-129">BG</span><span class="sxs-lookup"><span data-stu-id="e41eb-129">BG</span></span>|<span data-ttu-id="e41eb-130">BG80BNBG96611020345678</span><span class="sxs-lookup"><span data-stu-id="e41eb-130">BG80BNBG96611020345678</span></span>|
   |<span data-ttu-id="e41eb-131">3</span><span class="sxs-lookup"><span data-stu-id="e41eb-131">3</span></span>|<span data-ttu-id="e41eb-132">SEPA Dinamarca</span><span class="sxs-lookup"><span data-stu-id="e41eb-132">Denmark SEPA</span></span>|<span data-ttu-id="e41eb-133">DK</span><span class="sxs-lookup"><span data-stu-id="e41eb-133">DK</span></span>|<span data-ttu-id="e41eb-134">DK5000400440116243</span><span class="sxs-lookup"><span data-stu-id="e41eb-134">DK5000400440116243</span></span>|
   |<span data-ttu-id="e41eb-135">4</span><span class="sxs-lookup"><span data-stu-id="e41eb-135">4</span></span>|<span data-ttu-id="e41eb-136">SEPA Finlândia</span><span class="sxs-lookup"><span data-stu-id="e41eb-136">Finland SEPA</span></span>|<span data-ttu-id="e41eb-137">FI</span><span class="sxs-lookup"><span data-stu-id="e41eb-137">FI</span></span>|<span data-ttu-id="e41eb-138">FI2112345600000785</span><span class="sxs-lookup"><span data-stu-id="e41eb-138">FI2112345600000785</span></span>|
   |<span data-ttu-id="e41eb-139">5</span><span class="sxs-lookup"><span data-stu-id="e41eb-139">5</span></span>|<span data-ttu-id="e41eb-140">SEPA França</span><span class="sxs-lookup"><span data-stu-id="e41eb-140">France SEPA</span></span>|<span data-ttu-id="e41eb-141">FR</span><span class="sxs-lookup"><span data-stu-id="e41eb-141">FR</span></span>|<span data-ttu-id="e41eb-142">FR1420041010050500013M02606</span><span class="sxs-lookup"><span data-stu-id="e41eb-142">FR1420041010050500013M02606</span></span>|
   |<span data-ttu-id="e41eb-143">6</span><span class="sxs-lookup"><span data-stu-id="e41eb-143">6</span></span>|<span data-ttu-id="e41eb-144">SEPA Alemanha</span><span class="sxs-lookup"><span data-stu-id="e41eb-144">Germany SEPA</span></span>|<span data-ttu-id="e41eb-145">DE</span><span class="sxs-lookup"><span data-stu-id="e41eb-145">DE</span></span>|<span data-ttu-id="e41eb-146">DE89370400440532013000</span><span class="sxs-lookup"><span data-stu-id="e41eb-146">DE89370400440532013000</span></span>|
   |<span data-ttu-id="e41eb-147">7</span><span class="sxs-lookup"><span data-stu-id="e41eb-147">7</span></span>|<span data-ttu-id="e41eb-148">SEPA Grécia</span><span class="sxs-lookup"><span data-stu-id="e41eb-148">Greece SEPA</span></span>|<span data-ttu-id="e41eb-149">GA</span><span class="sxs-lookup"><span data-stu-id="e41eb-149">GR</span></span>|<span data-ttu-id="e41eb-150">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="e41eb-150">GR1601101250000000012300695</span></span>|
   |<span data-ttu-id="e41eb-151">8</span><span class="sxs-lookup"><span data-stu-id="e41eb-151">8</span></span>|<span data-ttu-id="e41eb-152">SEPA Itália</span><span class="sxs-lookup"><span data-stu-id="e41eb-152">Italy SEPA</span></span>|<span data-ttu-id="e41eb-153">IT</span><span class="sxs-lookup"><span data-stu-id="e41eb-153">IT</span></span>|<span data-ttu-id="e41eb-154">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="e41eb-154">GR1601101250000000012300695</span></span>|
   |<span data-ttu-id="e41eb-155">9</span><span class="sxs-lookup"><span data-stu-id="e41eb-155">9</span></span>|<span data-ttu-id="e41eb-156">SEPA Países Baixos</span><span class="sxs-lookup"><span data-stu-id="e41eb-156">Netherlands SEPA</span></span>|<span data-ttu-id="e41eb-157">NL</span><span class="sxs-lookup"><span data-stu-id="e41eb-157">NL</span></span>|<span data-ttu-id="e41eb-158">NL91ABNA0417164300</span><span class="sxs-lookup"><span data-stu-id="e41eb-158">NL91ABNA0417164300</span></span>|
   |<span data-ttu-id="e41eb-159">10</span><span class="sxs-lookup"><span data-stu-id="e41eb-159">10</span></span>|<span data-ttu-id="e41eb-160">SEPA Polônia</span><span class="sxs-lookup"><span data-stu-id="e41eb-160">Poland SEPA</span></span>|<span data-ttu-id="e41eb-161">PL</span><span class="sxs-lookup"><span data-stu-id="e41eb-161">PL</span></span>|<span data-ttu-id="e41eb-162">PL27114020040000300201355387</span><span class="sxs-lookup"><span data-stu-id="e41eb-162">PL27114020040000300201355387</span></span>|

   <span data-ttu-id="e41eb-163">Observação:- este conjunto de dados de amostra é derivado de informações publicamente disponíveis e destina-se a ser usado somente para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="e41eb-163">Note:- This sample data set is derived from publicly available information and is intended to be used for test purposes only.</span></span>

3. <span data-ttu-id="e41eb-164">Em uma nova guia do navegador, digite: **https://**\<YourTenantName\>**.sharepoint.com**</span><span class="sxs-lookup"><span data-stu-id="e41eb-164">In a new tab of your browser, type:  **https://**\<YourTenantName\>**.sharepoint.com**</span></span>
4. <span data-ttu-id="e41eb-p101">Clique em **documentos** para abrir a biblioteca de documentos para esse site. Se você for solicitado a realizar um novo tour de experiência de lista, clique em **avançar** até terminar.</span><span class="sxs-lookup"><span data-stu-id="e41eb-p101">Click **Documents** to open the document library for this site. If you're prompted for a new list experience tour, click **Next** until it's finished.</span></span>
5. <span data-ttu-id="e41eb-167">Clique em **Carregar** > **Arquivos** e selecione o IBANs.docx criado na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="e41eb-167">Click **Upload** > **Files** and select the IBANs.docx you created in step 2.</span></span>

## <a name="phase-3-demonstrate-data-discovery"></a><span data-ttu-id="e41eb-168">Fase 3: Demonstrar a descoberta de dados</span><span class="sxs-lookup"><span data-stu-id="e41eb-168">Phase 3: Demonstrate data discovery</span></span>

<span data-ttu-id="e41eb-169">Nesta fase, você demonstra a pesquisa para localizar o documento criado e armazenado na Fase 2, com base em seu conteúdo com IBANs.</span><span class="sxs-lookup"><span data-stu-id="e41eb-169">In this phase, you demonstrate search to find the document created and stored in Phase 2, based on its content containing IBANs.</span></span>

1. <span data-ttu-id="e41eb-170">Na guia Segurança e Conformidade, clique em **Página Inicial**, em seguida, clique em **Pesquisa e Investigação** > **Pesquisa de Conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-170">From the Security & Compliance tab, click **Home**, and then click **Search & investigation** > **Content search**.</span></span>
2. <span data-ttu-id="e41eb-171">Crie um novo item de pesquisa clicando em **+**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-171">Create a new search item by clicking on **+**.</span></span>
3. <span data-ttu-id="e41eb-172">Em uma nova janela, forneça as informações a seguir: a.</span><span class="sxs-lookup"><span data-stu-id="e41eb-172">In a new window, provide the following information: a.</span></span> <span data-ttu-id="e41eb-173">Nome: Pesquisa de IBAN b.</span><span class="sxs-lookup"><span data-stu-id="e41eb-173">Name: IBAN Search b.</span></span> <span data-ttu-id="e41eb-174">Onde deseja que seja feita a pesquisa?: **Escolha sites específicos para procurar** (clique em **+**) e insira a URL do site: **https://**\<YourTenantName\>**.sharepoint.com/** c.</span><span class="sxs-lookup"><span data-stu-id="e41eb-174">Where do you want us to look?: **Choose specific sites to search** (click **+**), and then enter the site's URL: **https://**\<YourTenantName\>**.sharepoint.com/** c.</span></span> <span data-ttu-id="e41eb-175">Clique em **Adicionar** e então clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-175">Click **Add**, and then click **OK**.</span></span> <span data-ttu-id="e41eb-176">Se você ver um Aviso, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-176">If you see a Warning, click **OK**.</span></span>
    <span data-ttu-id="e41eb-177">d.</span><span class="sxs-lookup"><span data-stu-id="e41eb-177">d.</span></span> <span data-ttu-id="e41eb-178">Clique em **Avançar** em uma janela **Nova pesquisa**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-178">Click **Next** on a **New search** window.</span></span>
    <span data-ttu-id="e41eb-179">e.</span><span class="sxs-lookup"><span data-stu-id="e41eb-179">e.</span></span> <span data-ttu-id="e41eb-180">Para **O que você deseja que procuremos?**: **SensitiveType: "Número internacional de conta bancária (IBAN)"**, em seguida, clique em **Pesquisar**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-180">For **What do you want us to look for?**: **SensitiveType:"International Banking Account Number (IBAN)"**, and then click **Search**.</span></span>

4. <span data-ttu-id="e41eb-181">Você deverá ver pelo menos um item listado nos resultados da **Pesquisa de IBAN**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-181">Make sure you see at least one item listed in the **IBAN Search** results.</span></span>

## <a name="phase-4-create-a-custom-sensitive-information-type-via-powershell"></a><span data-ttu-id="e41eb-182">Fase 4: Criar um tipo de informação confidencial personalizado via PowerShell</span><span class="sxs-lookup"><span data-stu-id="e41eb-182">Phase 4: Create a custom sensitive information type via PowerShell</span></span>

<span data-ttu-id="e41eb-p103">Nesta fase, você pode criar um tipo personalizado de informações confidenciais para a fictícia Contoso Corporation usando o Microsoft PowerShell. A Contoso usa um número de clientes (CCN) para identificar cada cliente em seu banco de dados. Um CCN tem a seguinte estrutura:</span><span class="sxs-lookup"><span data-stu-id="e41eb-p103">In this phase, you create a custom sensitive information type for the fictional Contoso Corporation using Microsoft PowerShell.  Contoso uses a Contoso Customer Number (CCN) to identify each customer in their customer database. A CCN consists of the following structure:</span></span>

- <span data-ttu-id="e41eb-186">Dois dígitos para representar o ano em que o registro foi criado.</span><span class="sxs-lookup"><span data-stu-id="e41eb-186">Two digits to represent the year that the record was created.</span></span>
  - <span data-ttu-id="e41eb-187">A Contoso foi fundada em 2002; portanto, o menor valor possível seria 02.</span><span class="sxs-lookup"><span data-stu-id="e41eb-187">Contoso was founded in 2002; therefore, the earliest possible value would be 02.</span></span>
- <span data-ttu-id="e41eb-188">Três dígitos para representar o órgão responsável pela criação do registro.</span><span class="sxs-lookup"><span data-stu-id="e41eb-188">Three digits to represent the partner agency that created the record.</span></span>
  - <span data-ttu-id="e41eb-189">O intervalo de valores possível do órgão vai de 000 a 999.</span><span class="sxs-lookup"><span data-stu-id="e41eb-189">Possible agency values range from 000 to 999.</span></span>
- <span data-ttu-id="e41eb-190">Um caractere alfabético para representar a linha de negócios.</span><span class="sxs-lookup"><span data-stu-id="e41eb-190">An alphabetic character to represent the line of business.</span></span>
  - <span data-ttu-id="e41eb-191">Os valores possíveis são a-z e devem diferenciar maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e41eb-191">Possible values are a-z and should be case insensitive.</span></span>
- <span data-ttu-id="e41eb-192">Um número de série de quatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="e41eb-192">A four-digit serial number.</span></span>
  - <span data-ttu-id="e41eb-193">O intervalo de valores possível de um número de série que vai de 0000 a 9999.</span><span class="sxs-lookup"><span data-stu-id="e41eb-193">Possible serial number values range from 0000 to 9999.</span></span>

<span data-ttu-id="e41eb-p104">A Contoso sempre se refere aos clientes usando um CCN nas correspondências interna e externa, em documentos e outras formas. A Contoso precisa de um tipo de item confidencial personalizado para detectar o uso do CCN em conteúdo do Microsoft 365 e assim aplicar proteção no uso desse formulário de informações de identificação pessoal.</span><span class="sxs-lookup"><span data-stu-id="e41eb-p104">Contoso always refers to customers by using a CCN in internal correspondence, external correspondence, documents, and other forms. Contoso needs a custom sensitive item type to detect the use of CCNs in Microsoft 365 content so that they may apply protection to the use of this form of personal identifiable information.</span></span>

1. <span data-ttu-id="e41eb-196">Use as instruções de conexões com autenticação multifator (MFA) em [Conectar-se ao Centro de Conformidade e Segurança do PowerShell](/powershell/exchange/connect-to-scc-powershell) e conecte-se ao Centro de Conformidade e Segurança com o UPN da sua conta de administrador global.</span><span class="sxs-lookup"><span data-stu-id="e41eb-196">Use the multi-factor authentication (MFA) connection instructions in [Connect to Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell) and connect to the Security & Compliance Center with UPN of your global administrator account.</span></span>

2. <span data-ttu-id="e41eb-197">Execute os seguintes comandos do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e41eb-197">Run the following PowerShell commands.</span></span>

   ```powershell
   #Create & start search for sample data
   $searchName = "Sample Customer Information Search"
   $searchQuery = "15080P9562 OR 14040O1119 OR 15020J8317 OR 14050E2330 OR 16050E2166 OR 17040O1118"
   New-ComplianceSearch -Name $searchName -SharePointLocation All -ExchangeLocation All -ContentMatchQuery $searchQuery
   Start-ComplianceSearch -Identity $searchName#Create & start search for sample data
   $searchName = "Sample Customer Information Search"
   $searchQuery = "15080P9562 OR 14040O1119 OR 15020J8317 OR 14050E2330 OR 16050E2166 OR 17040O1118"
   New-ComplianceSearch -Name $searchName -SharePointLocation All -ExchangeLocation All -ContentMatchQuery $searchQuery
   Start-ComplianceSearch -Identity $searchName
   ```

3. <span data-ttu-id="e41eb-198">Execute os seguintes comandos do PowerShell e copie os GUIDs gerados para uma instância aberta do Bloco de Notas no computador na ordem em que estão listados.</span><span class="sxs-lookup"><span data-stu-id="e41eb-198">Run the following PowerShell commands and copy the generated GUIDs to an open instance of Notepad on your computer in the order in which they are listed.</span></span>

   ```powershell
   #Generate three unique GUIDs
   Write-Host "GUID1 = "([guid]::NewGuid().Guid)
   Write-Host "GUID2 = "([guid]::NewGuid().Guid)
   Write-Host "GUID3 = "([guid]::NewGuid().Guid)
   ```

4. <span data-ttu-id="e41eb-199">No computador local, abra outra instância do Bloco de Notas e cole o seguinte conteúdo:</span><span class="sxs-lookup"><span data-stu-id="e41eb-199">On your local computer, open another instance of Notepad and paste in the following content:</span></span>

   ```text
   <?xml version="1.0" encoding="utf-8"?>
   <RulePackage xmlns="https://schemas.microsoft.com/office/2011/mce">
   <RulePack id="GUID1">
   <Version major="1" minor="0" build="0" revision="0" />
   <Publisher id="GUID2" />
   <Details defaultLangCode="en">
   <LocalizedDetails langcode="en">
   <PublisherName>Contoso Ltd.</PublisherName>
   <Name>Contoso Rule Package</Name>
   <Description>Defines Contoso's custom set of classification rules</Description>
   </LocalizedDetails>
   </Details>
   </RulePack>
   <Rules>
   <!-- Contoso Customer Number (CCN) -->
   <Entity id="GUID3" patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
   <IdMatch idRef="Regex_contoso_ccn" />
   <Match idRef="Keyword_contoso_ccn" />
   <Match idRef="Regex_eu_date" />
   </Pattern>
   </Entity>
   <Regex id="Regex_contoso_ccn">[0-1][0-9][0-9]{3}[A-Za-z][0-9]{4}</Regex>
   <Keyword id="Keyword_contoso_ccn">
   <Group matchStyle="word">
   <Term caseSensitive="false">customer number</Term>
   <Term caseSensitive="false">customer no</Term>
   <Term caseSensitive="false">customer #</Term>
   <Term caseSensitive="false">customer#</Term>
   <Term caseSensitive="false">Contoso customer</Term>
   </Group>
   </Keyword>
   <Regex id="Regex_eu_date"> (0?[1-9]|[12][0-9]|3[0-1])[\/-](0?[1-9]|1[0-2]|j\x00e4n(uar)?|jan(uary|uari|uar|eiro|vier|v)?|ene(ro)?|genn(aio)? |feb(ruary|ruari|rero|braio|ruar|br)?|f\x00e9vr(ier)?|fev(ereiro)?|mar(zo|o|ch|s)?|m\x00e4rz|maart|apr(ile|il)?|abr(il)?|avril |may(o)?|magg(io)?|mai|mei|mai(o)?|jun(io|i|e|ho)?|giugno|juin|jul(y|io|i|ho)?|lu(glio)?|juil(let)?|ag(o|osto)?|aug(ustus|ust)?|ao\x00fbt|sep|sept(ember|iembre|embre)?|sett(embre)?|set(embro)?|oct(ober|ubre|obre)?|ott(obre)?|okt(ober)?|out(ubro)? |nov(ember|iembre|embre|embro)?|dec(ember)?|dic(iembre|embre)?|dez(ember|embro)?|d\x00e9c(embre)?)[ \/-](19|20)?[0-9]{2}</Regex>
   <LocalizedStrings>
   <Resource idRef="GUID3">
   <Name default="true" langcode="en-us">Contoso Customer Number (CCN)</Name>
   <Description default="true" langcode="en-us">Contoso Customer Number (CCN) that looks for additional keywords and EU formatted date</Description>
   </Resource>
   </LocalizedStrings>
   </Rules>
   </RulePackage>
   ```

5. <span data-ttu-id="e41eb-200">Substitua os valores de GUID1, GUID2 e GUID3 no texto XML da etapa 4 pelos valores da etapa 3 e salve o conteúdo no computador local com o nome ContosoCCN.xml.</span><span class="sxs-lookup"><span data-stu-id="e41eb-200">Replace the values of GUID1, GUID2, and GUID3 in the XML text of step 4 with their values from step 3, and then save the contents on your local computer with the name ContosoCCN.xml.</span></span>

6. <span data-ttu-id="e41eb-201">Preencha o caminho para o arquivo ContosoCCN.xml e execute os comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="e41eb-201">Fill in the path to your ContosoCCN.xml file and run the following commands.</span></span>

   ```powershell
   #Create new Sensitive Information Type
   $path="<path to the ContosoCCN.xml file, such as C:\Scripts\ContosoCCN.xml>"
   New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path $path -Encoding Byte -ReadCount 0)
   ```

7. <span data-ttu-id="e41eb-p105">Na guia Segurança e Conformidade, clique em **Classificações** > **Tipos de informação confidencial**. Você verá o número de clientes da Contoso (CCN) na lista.</span><span class="sxs-lookup"><span data-stu-id="e41eb-p105">From the Security & Compliance tab, click **Classifications** > **Sensitive information types**. You should see the Contoso Customer Number (CCN) in the list.</span></span>

## <a name="phase-5-demonstrate-data-protection"></a><span data-ttu-id="e41eb-204">Fase 5: Demonstrar a proteção de dados</span><span class="sxs-lookup"><span data-stu-id="e41eb-204">Phase 5: Demonstrate data protection</span></span>

<span data-ttu-id="e41eb-205">A proteção de informações pessoais no Microsoft 365 inclui o uso de recursos de prevenção contra perda de dados (DLP).</span><span class="sxs-lookup"><span data-stu-id="e41eb-205">Protection of personal information in Microsoft 365 includes using data loss prevention (DLP) capabilities.</span></span>  <span data-ttu-id="e41eb-206">Com as políticas de DLP, é possível proteger automaticamente informações confidenciais no Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e41eb-206">With DLP policies, you can automatically protect sensitive information across Microsoft 365.</span></span>

<span data-ttu-id="e41eb-p107">Há várias maneiras de aplicar a proteção. Instruindo e aumentar a conscientização sobre onde os dados de residentes da UE estão armazenados em seu ambiente e como os seus funcionários têm permissão para gerenciá-los representa um nível de proteção de informações usando a DLP do Office 365.</span><span class="sxs-lookup"><span data-stu-id="e41eb-p107">There are multiple ways you can apply the protection. Educating and raising awareness to where EU resident data is stored in your environment and how your employees are permitted to handle it represents one level of information protection using Office 365 DLP.</span></span>

<span data-ttu-id="e41eb-209">Nesta fase, você cria uma nova política DLP e demonstra como ela é aplicada a arquivos IBANs.docx armazenados no SharePoint Online na fase 2 e quando você tenta enviar um email com IBANs.</span><span class="sxs-lookup"><span data-stu-id="e41eb-209">In this phase, you create a new DLP policy and demonstrate how it gets applied to the IBANs.docx file you stored in SharePoint Online in Phase 2 and when you attempt to send an email containing IBANs.</span></span>

1. <span data-ttu-id="e41eb-210">Na guia Segurança e Conformidade do navegador, clique em **Página Inicial**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-210">From the Security & Compliance tab of your browser, click **Home**.</span></span>
2. <span data-ttu-id="e41eb-211">Clique em **Prevenção contra perda de dados** > **Política**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-211">Click **Data loss prevention** > **Policy**.</span></span>
3. <span data-ttu-id="e41eb-212">Clique em **+ Criar uma política**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-212">Click **+ Create a policy**.</span></span>
4. <span data-ttu-id="e41eb-213">Em **Iniciar com um modelo ou criar uma política personalizada**, clique em **Personalizado** > **Política personalizada** > **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-213">In **Start with a template or create a custom policy**, click **Custom** > **Custom policy** > **Next**.</span></span>
5. <span data-ttu-id="e41eb-p108">Em **Nomear sua política**, forneça os seguintes detalhes e clique em **Avançar**: a. Nome: **Política de PII de cidadão da UE** b Descrição: **Proteger as informações de identificação pessoal de cidadãos europeus**</span><span class="sxs-lookup"><span data-stu-id="e41eb-p108">In **Name your policy**, provide the following details and then click **Next**:  a. Name: **EU Citizen PII Policy** b. Description: **Protect the personally identifiable information of European citizens**</span></span>
6. <span data-ttu-id="e41eb-p109">Em **escolher locais**, selecione **todos os locais no Microsoft 365**. Isso inclui conteúdo no email do Exchange e documentos do OneDrive e do SharePoint. E, em seguida, clique em **avançar**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-p109">In **Choose locations**, select **All locations in Microsoft 365**. This will include content in Exchange email and OneDrive and SharePoint documents. And then click **Next**.</span></span>
7. <span data-ttu-id="e41eb-220">Em **Personalizar o tipo de conteúdo que deseja proteger**, clique em **Encontrar conteúdo que contém:** e clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-220">In **Customize the type of content you want to protect**, click **Find content that contains:** and then click **Edit**.</span></span>
8. <span data-ttu-id="e41eb-221">Em **Escolher os tipos de conteúdo para proteger**, clique em **Adicionar** > **Tipos de informações confidenciais**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-221">In **Choose the types of content to protect**, click **Add** > **Sensitive info types**.</span></span>
9. <span data-ttu-id="e41eb-222">Em **Tipos de informações confidenciais**, clique em **+ Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-222">In **Sensitive info types**, click **+ Add**.</span></span>
10. <span data-ttu-id="e41eb-223">Em **Tipos de informações confidenciais**, pesquise **IBAN**, marque a caixa de seleção **Número internacional de conta bancária (IBAN)** e, em seguida, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-223">In **Sensitive info types**, search for **IBAN**, select the check box for **International Banking Account Number (IBAN)**, and then click **Add**.</span></span>
11. <span data-ttu-id="e41eb-224">Confirme se o tipo de informações confidenciais do **Número internacional de conta bancária (IBAN)** foi adicionado e clique em **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-224">Confirm that the **International Banking Account Number (IBAN)** sensitive information type was added, and then click **Done**.</span></span>
12. <span data-ttu-id="e41eb-225">Em **O conteúdo contém**, confirme que os tipos de informação confidencial foram adicionados e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-225">In **Content contains**, confirm that the sensitive information types were added and then click **Save**.</span></span>
13. <span data-ttu-id="e41eb-226">Em **Personalize o tipo de conteúdo que deseja proteger**, confirme **Localizar conteúdo com:** o **Número internacional de conta bancária (IBAN)** e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-226">In **Customize the type of content you want to protect**, confirm  **Find content that contains:** contains the **International Banking Account Number (IBAN)**, and then click **Next**.</span></span>
14. <span data-ttu-id="e41eb-227">Em **Detectar quando o conteúdo que está sendo compartilhado contém:**, altere o valor de **10** para **1** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-227">In **Detect when content that's being shared contains:**, change the value from **10** to **1**, and then click **Next**.</span></span>
15. <span data-ttu-id="e41eb-228">Em **Deseja ativar a política ou testar primeiro?**, escolha as configurações a seguir e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-228">In **Do you want to turn on the policy or test things out first?**, choose the following settings, and then click **Next**.</span></span>
    <span data-ttu-id="e41eb-229">a.</span><span class="sxs-lookup"><span data-stu-id="e41eb-229">a.</span></span> <span data-ttu-id="e41eb-230">Selecione a opção para **Gostaria de testá-lo primeiro** b.</span><span class="sxs-lookup"><span data-stu-id="e41eb-230">Select the option for **I'd like to test it out first** b.</span></span> <span data-ttu-id="e41eb-231">Marque a caixa de seleção **Mostrar dicas de política em modo teste**</span><span class="sxs-lookup"><span data-stu-id="e41eb-231">Select the check box for **Show policy tips while in test mode**</span></span>
16. <span data-ttu-id="e41eb-p111">Em **Analisar as configurações**, clique em **Criar** depois de analisar as configurações. Observação: depois de criar uma nova política DLP, pode levar algum tempo para ela entrar em vigor.</span><span class="sxs-lookup"><span data-stu-id="e41eb-p111">In **Review your settings**, click **Create** after reviewing the settings. NOTE: After you create a new DLP policy, it will take a while for it to take effect.</span></span>
17. <span data-ttu-id="e41eb-234">No computador local, abra uma instância privada do navegador.</span><span class="sxs-lookup"><span data-stu-id="e41eb-234">On your local computer, open a private instance of your browser.</span></span>
18. <span data-ttu-id="e41eb-235">Na barra de endereços, digite **https://**\<YourTenantName\>**.sharepoint.com** e entre usando sua conta de administrador global.</span><span class="sxs-lookup"><span data-stu-id="e41eb-235">In the address bar, type **https://**\<YourTenantName\>**.sharepoint.com** and sign in using your global administrator account.</span></span>
19. <span data-ttu-id="e41eb-236">Clique em **Documentos**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-236">Click **Documents**.</span></span>
20. <span data-ttu-id="e41eb-p112">Clique no arquivo chamado "IBANs.docx". Você verá "Dica de política para IBANs.docx". O arquivo IBANs.docx foi compartilhado com destinatários externos, o que viola a política DLP.</span><span class="sxs-lookup"><span data-stu-id="e41eb-p112">Click the file named 'IBANs.docx'. You should see 'Policy tip for IBANs.docx'.  The IBANs.docx file was shared with external recipients, which violates the DLP policy.</span></span>
21. <span data-ttu-id="e41eb-240">Na barra de endereços, digite: `https://outlook.office365.com`</span><span class="sxs-lookup"><span data-stu-id="e41eb-240">In the address bar, type: `https://outlook.office365.com`</span></span>
22. <span data-ttu-id="e41eb-241">Clique em **Novo** - **Email** e forneça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e41eb-241">Click **New** - **Email message** and provide the following:</span></span>

    - <span data-ttu-id="e41eb-242">**Para:** \<a personal email address\></span><span class="sxs-lookup"><span data-stu-id="e41eb-242">**To:** \<a personal email address\></span></span>
    - <span data-ttu-id="e41eb-243">**Assunto:** Teste de RGPD</span><span class="sxs-lookup"><span data-stu-id="e41eb-243">**Subject:** GDPR Test</span></span>
    - <span data-ttu-id="e41eb-244">**Corpo:** Cópia na tabela de valores mostrados abaixo.</span><span class="sxs-lookup"><span data-stu-id="e41eb-244">**Body:** Copy in the table of values shown below.</span></span>

      |<span data-ttu-id="e41eb-245">Número</span><span class="sxs-lookup"><span data-stu-id="e41eb-245">Number</span></span>|<span data-ttu-id="e41eb-246">País</span><span class="sxs-lookup"><span data-stu-id="e41eb-246">Country</span></span>|<span data-ttu-id="e41eb-247">Código</span><span class="sxs-lookup"><span data-stu-id="e41eb-247">Code</span></span>|<span data-ttu-id="e41eb-248">IBAN</span><span class="sxs-lookup"><span data-stu-id="e41eb-248">IBAN</span></span>|
      |---|---|---|---|
      |<span data-ttu-id="e41eb-249">1</span><span class="sxs-lookup"><span data-stu-id="e41eb-249">1</span></span>|<span data-ttu-id="e41eb-250">SEPA Áustria</span><span class="sxs-lookup"><span data-stu-id="e41eb-250">Austria SEPA</span></span>|<span data-ttu-id="e41eb-251">AT</span><span class="sxs-lookup"><span data-stu-id="e41eb-251">AT</span></span>|<span data-ttu-id="e41eb-252">AT611904300234573201</span><span class="sxs-lookup"><span data-stu-id="e41eb-252">AT611904300234573201</span></span>|
      |<span data-ttu-id="e41eb-253">2</span><span class="sxs-lookup"><span data-stu-id="e41eb-253">2</span></span>|<span data-ttu-id="e41eb-254">SEPA Bulgária</span><span class="sxs-lookup"><span data-stu-id="e41eb-254">Bulgaria SEPA</span></span>|<span data-ttu-id="e41eb-255">BG</span><span class="sxs-lookup"><span data-stu-id="e41eb-255">BG</span></span>|<span data-ttu-id="e41eb-256">BG80BNBG96611020345678</span><span class="sxs-lookup"><span data-stu-id="e41eb-256">BG80BNBG96611020345678</span></span>|
      |<span data-ttu-id="e41eb-257">3</span><span class="sxs-lookup"><span data-stu-id="e41eb-257">3</span></span>|<span data-ttu-id="e41eb-258">SEPA Dinamarca</span><span class="sxs-lookup"><span data-stu-id="e41eb-258">Denmark SEPA</span></span>|<span data-ttu-id="e41eb-259">DK</span><span class="sxs-lookup"><span data-stu-id="e41eb-259">DK</span></span>|<span data-ttu-id="e41eb-260">DK5000400440116243</span><span class="sxs-lookup"><span data-stu-id="e41eb-260">DK5000400440116243</span></span>|
      |<span data-ttu-id="e41eb-261">4</span><span class="sxs-lookup"><span data-stu-id="e41eb-261">4</span></span>|<span data-ttu-id="e41eb-262">SEPA Finlândia</span><span class="sxs-lookup"><span data-stu-id="e41eb-262">Finland SEPA</span></span>|<span data-ttu-id="e41eb-263">FI</span><span class="sxs-lookup"><span data-stu-id="e41eb-263">FI</span></span>|<span data-ttu-id="e41eb-264">FI2112345600000785</span><span class="sxs-lookup"><span data-stu-id="e41eb-264">FI2112345600000785</span></span>|
      |<span data-ttu-id="e41eb-265">5</span><span class="sxs-lookup"><span data-stu-id="e41eb-265">5</span></span>|<span data-ttu-id="e41eb-266">SEPA França</span><span class="sxs-lookup"><span data-stu-id="e41eb-266">France SEPA</span></span>|<span data-ttu-id="e41eb-267">FR</span><span class="sxs-lookup"><span data-stu-id="e41eb-267">FR</span></span>|<span data-ttu-id="e41eb-268">FR1420041010050500013M02606</span><span class="sxs-lookup"><span data-stu-id="e41eb-268">FR1420041010050500013M02606</span></span>|
      |<span data-ttu-id="e41eb-269">6</span><span class="sxs-lookup"><span data-stu-id="e41eb-269">6</span></span>|<span data-ttu-id="e41eb-270">SEPA Alemanha</span><span class="sxs-lookup"><span data-stu-id="e41eb-270">Germany SEPA</span></span>|<span data-ttu-id="e41eb-271">DE</span><span class="sxs-lookup"><span data-stu-id="e41eb-271">DE</span></span>|<span data-ttu-id="e41eb-272">DE89370400440532013000</span><span class="sxs-lookup"><span data-stu-id="e41eb-272">DE89370400440532013000</span></span>|
      |<span data-ttu-id="e41eb-273">7</span><span class="sxs-lookup"><span data-stu-id="e41eb-273">7</span></span>|<span data-ttu-id="e41eb-274">SEPA Grécia</span><span class="sxs-lookup"><span data-stu-id="e41eb-274">Greece SEPA</span></span>|<span data-ttu-id="e41eb-275">GA</span><span class="sxs-lookup"><span data-stu-id="e41eb-275">GR</span></span>|<span data-ttu-id="e41eb-276">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="e41eb-276">GR1601101250000000012300695</span></span>|
      |<span data-ttu-id="e41eb-277">8</span><span class="sxs-lookup"><span data-stu-id="e41eb-277">8</span></span>|<span data-ttu-id="e41eb-278">SEPA Itália</span><span class="sxs-lookup"><span data-stu-id="e41eb-278">Italy SEPA</span></span>|<span data-ttu-id="e41eb-279">IT</span><span class="sxs-lookup"><span data-stu-id="e41eb-279">IT</span></span>|<span data-ttu-id="e41eb-280">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="e41eb-280">GR1601101250000000012300695</span></span>|
      |<span data-ttu-id="e41eb-281">9</span><span class="sxs-lookup"><span data-stu-id="e41eb-281">9</span></span>|<span data-ttu-id="e41eb-282">SEPA Países Baixos</span><span class="sxs-lookup"><span data-stu-id="e41eb-282">Netherlands SEPA</span></span>|<span data-ttu-id="e41eb-283">NL</span><span class="sxs-lookup"><span data-stu-id="e41eb-283">NL</span></span>|<span data-ttu-id="e41eb-284">NL91ABNA0417164300</span><span class="sxs-lookup"><span data-stu-id="e41eb-284">NL91ABNA0417164300</span></span>|
      |<span data-ttu-id="e41eb-285">10</span><span class="sxs-lookup"><span data-stu-id="e41eb-285">10</span></span>|<span data-ttu-id="e41eb-286">SEPA Polônia</span><span class="sxs-lookup"><span data-stu-id="e41eb-286">Poland SEPA</span></span>|<span data-ttu-id="e41eb-287">PL</span><span class="sxs-lookup"><span data-stu-id="e41eb-287">PL</span></span>|<span data-ttu-id="e41eb-288">PL27114020040000300201355387</span><span class="sxs-lookup"><span data-stu-id="e41eb-288">PL27114020040000300201355387</span></span>|
      |

    <span data-ttu-id="e41eb-289">Observação:- este conjunto de dados de amostra é derivado de informações publicamente disponíveis e destina-se a ser usado somente para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="e41eb-289">Note:- This sample data set is derived from publicly available information and is intended to be used for test purposes only.</span></span>

23. <span data-ttu-id="e41eb-290">Você verá que a política DLP reconheceu que o corpo do email contém IBANs e informa a dica de política na parte superior da janela da mensagem.</span><span class="sxs-lookup"><span data-stu-id="e41eb-290">You will see that the DLP policy recognized that body of the email contains IBANs and provides you with the policy tip at the top of the message window.</span></span>
24. <span data-ttu-id="e41eb-291">Feche a instância privada do navegador.</span><span class="sxs-lookup"><span data-stu-id="e41eb-291">Close the private instance of your browser.</span></span>

## <a name="phase-6-demonstrate-reporting"></a><span data-ttu-id="e41eb-292">Etapa 6: Demonstrar relatórios</span><span class="sxs-lookup"><span data-stu-id="e41eb-292">Phase 6: Demonstrate reporting</span></span>

<span data-ttu-id="e41eb-293">Nesta fase, você demonstra relatórios do Microsoft 365 com base na política DLP configurada na fase 5.</span><span class="sxs-lookup"><span data-stu-id="e41eb-293">In this phase, you demonstrate Microsoft 365 reporting based on the DLP policy configured in Phase 5.</span></span>

   1. <span data-ttu-id="e41eb-294">Na guia Segurança e Conformidade do navegador, clique em **Página Inicial**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-294">From the Security & Compliance tab of your browser, click **Home**.</span></span>
   2. <span data-ttu-id="e41eb-295">Clique em **Relatórios** > **Painel** > **Correspondências de políticas DLP**.</span><span class="sxs-lookup"><span data-stu-id="e41eb-295">Click **Reports** > **Dashboard** > **DLP policy matches**.</span></span>
   3. <span data-ttu-id="e41eb-p113">Sua política DLP ajuda a identificar e proteger informações confidenciais da organização. Por exemplo, no relatório, você verá que a política identificou o documento que contém IBANs armazenados no SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="e41eb-p113">Your DLP policy helps identify and protect organization's sensitive information. For example, in the report you will see that the policy identified the document that contains IBANs stored in SharePoint Online.</span></span>

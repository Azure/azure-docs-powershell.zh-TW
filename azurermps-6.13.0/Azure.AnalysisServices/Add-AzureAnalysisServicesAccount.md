---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/add-azureanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Add-AzureAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Add-AzureAnalysisServicesAccount.md
ms.openlocfilehash: 39d15940b85e7da19cf4f8f23abee5db6223235f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445884"
---
# <span data-ttu-id="64391-101">Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="64391-101">Add-AzureAnalysisServicesAccount</span></span>

## <span data-ttu-id="64391-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64391-102">SYNOPSIS</span></span>
<span data-ttu-id="64391-103">新增要用於 Azure Analysis Services server Cmdlet 要求的經過驗證的帳戶。</span><span class="sxs-lookup"><span data-stu-id="64391-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64391-104">句法</span><span class="sxs-lookup"><span data-stu-id="64391-104">SYNTAX</span></span>

### <span data-ttu-id="64391-105">UserParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="64391-105">UserParameterSetName (Default)</span></span>
```
Add-AzureAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64391-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="64391-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzureAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential>
 [-ServicePrincipal] -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64391-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="64391-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzureAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64391-108">說明</span><span class="sxs-lookup"><span data-stu-id="64391-108">DESCRIPTION</span></span>
<span data-ttu-id="64391-109">Add-AzureAnalysisServicesAccount Cmdlet 是用來登入 Azure Analysis Services 伺服器實例</span><span class="sxs-lookup"><span data-stu-id="64391-109">The Add-AzureAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="64391-110">示例</span><span class="sxs-lookup"><span data-stu-id="64391-110">EXAMPLES</span></span>

### <span data-ttu-id="64391-111">範例1</span><span class="sxs-lookup"><span data-stu-id="64391-111">Example 1</span></span>
```
PS C:\>Add-AzureAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="64391-112">這個範例會將 $UserCredential 變數所指定的帳號新增至 westcentralus.asazure.windows.net Analysis Services 環境。</span><span class="sxs-lookup"><span data-stu-id="64391-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="64391-113">範例2</span><span class="sxs-lookup"><span data-stu-id="64391-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzureAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="64391-114">第一個命令會取得應用程式服務主體認證，然後將它們儲存在 $ApplicationCredential 變數中。</span><span class="sxs-lookup"><span data-stu-id="64391-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="64391-115">第二個命令會將 $ApplicationCredential 變數和 TenantId 所指定的應用程式服務主體帳戶新增至 westcentralus.asazure.windows.net Analysis Services 環境。</span><span class="sxs-lookup"><span data-stu-id="64391-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="64391-116">範例3</span><span class="sxs-lookup"><span data-stu-id="64391-116">Example 3</span></span>
```
PS C:\>Add-AzureAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="64391-117">這個範例會將 ApplicationId、TenantId 和 CertificateThumbprint 所指定的應用程式服務主體帳戶新增至 westcentralus.asazure.windows.net Analysis Services 環境。</span><span class="sxs-lookup"><span data-stu-id="64391-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="64391-118">參數</span><span class="sxs-lookup"><span data-stu-id="64391-118">PARAMETERS</span></span>

### <span data-ttu-id="64391-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="64391-119">-ApplicationId</span></span>
<span data-ttu-id="64391-120">應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="64391-120">The application ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64391-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="64391-121">-CertificateThumbprint</span></span>
<span data-ttu-id="64391-122">憑證雜湊 (指紋) </span><span class="sxs-lookup"><span data-stu-id="64391-122">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64391-123">-認證</span><span class="sxs-lookup"><span data-stu-id="64391-123">-Credential</span></span>
<span data-ttu-id="64391-124">登入認證</span><span class="sxs-lookup"><span data-stu-id="64391-124">Login credentials</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithPasswordParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64391-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="64391-125">-RolloutEnvironment</span></span>
<span data-ttu-id="64391-126">要登入之 Azure Analysis Services 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="64391-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="64391-127">考慮到伺服器的完整名稱（例如 asazure://westcentralus.asazure.windows.net/testserver），此變數的正確值將會 westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="64391-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64391-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="64391-128">-ServicePrincipal</span></span>
<span data-ttu-id="64391-129">指示此帳戶透過提供服務主體認證來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="64391-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64391-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="64391-130">-TenantId</span></span>
<span data-ttu-id="64391-131">租使用者名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="64391-131">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64391-132">-確認</span><span class="sxs-lookup"><span data-stu-id="64391-132">-Confirm</span></span>
<span data-ttu-id="64391-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="64391-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64391-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64391-134">-WhatIf</span></span>
<span data-ttu-id="64391-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="64391-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64391-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="64391-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64391-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64391-137">CommonParameters</span></span>
<span data-ttu-id="64391-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64391-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64391-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="64391-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64391-140">輸入</span><span class="sxs-lookup"><span data-stu-id="64391-140">INPUTS</span></span>

### <span data-ttu-id="64391-141">所有</span><span class="sxs-lookup"><span data-stu-id="64391-141">None</span></span>

## <span data-ttu-id="64391-142">輸出</span><span class="sxs-lookup"><span data-stu-id="64391-142">OUTPUTS</span></span>

### <span data-ttu-id="64391-143">AnalysisServices. Dataplane. AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="64391-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="64391-144">筆記</span><span class="sxs-lookup"><span data-stu-id="64391-144">NOTES</span></span>
<span data-ttu-id="64391-145">別名： Login-AzureAsAccount</span><span class="sxs-lookup"><span data-stu-id="64391-145">Alias: Login-AzureAsAccount</span></span>

## <span data-ttu-id="64391-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="64391-146">RELATED LINKS</span></span>
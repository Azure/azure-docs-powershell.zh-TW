---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/add-azanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
ms.openlocfilehash: f1d59a0a34072a91242c6595c269ba55c4397e0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127940"
---
# <span data-ttu-id="60f05-101">Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="60f05-101">Add-AzAnalysisServicesAccount</span></span>

## <span data-ttu-id="60f05-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60f05-102">SYNOPSIS</span></span>
<span data-ttu-id="60f05-103">新增要用於 Azure Analysis Services server Cmdlet 要求的經過驗證的帳戶。</span><span class="sxs-lookup"><span data-stu-id="60f05-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

## <span data-ttu-id="60f05-104">句法</span><span class="sxs-lookup"><span data-stu-id="60f05-104">SYNTAX</span></span>

### <span data-ttu-id="60f05-105">UserParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="60f05-105">UserParameterSetName (Default)</span></span>
```
Add-AzAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60f05-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="60f05-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60f05-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="60f05-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60f05-108">說明</span><span class="sxs-lookup"><span data-stu-id="60f05-108">DESCRIPTION</span></span>
<span data-ttu-id="60f05-109">Add-AzAnalysisServicesAccount Cmdlet 是用來登入 Azure Analysis Services 伺服器實例</span><span class="sxs-lookup"><span data-stu-id="60f05-109">The Add-AzAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="60f05-110">示例</span><span class="sxs-lookup"><span data-stu-id="60f05-110">EXAMPLES</span></span>

### <span data-ttu-id="60f05-111">範例1</span><span class="sxs-lookup"><span data-stu-id="60f05-111">Example 1</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="60f05-112">這個範例會將 $UserCredential 變數所指定的帳號新增至 westcentralus.asazure.windows.net Analysis Services 環境。</span><span class="sxs-lookup"><span data-stu-id="60f05-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="60f05-113">範例2</span><span class="sxs-lookup"><span data-stu-id="60f05-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="60f05-114">第一個命令會取得應用程式服務主體認證，然後將它們儲存在 $ApplicationCredential 變數中。</span><span class="sxs-lookup"><span data-stu-id="60f05-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="60f05-115">第二個命令會將 $ApplicationCredential 變數和 TenantId 所指定的應用程式服務主體帳戶新增至 westcentralus.asazure.windows.net Analysis Services 環境。</span><span class="sxs-lookup"><span data-stu-id="60f05-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="60f05-116">範例3</span><span class="sxs-lookup"><span data-stu-id="60f05-116">Example 3</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="60f05-117">這個範例會將 ApplicationId、TenantId 和 CertificateThumbprint 所指定的應用程式服務主體帳戶新增至 westcentralus.asazure.windows.net Analysis Services 環境。</span><span class="sxs-lookup"><span data-stu-id="60f05-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="60f05-118">參數</span><span class="sxs-lookup"><span data-stu-id="60f05-118">PARAMETERS</span></span>

### <span data-ttu-id="60f05-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="60f05-119">-ApplicationId</span></span>
<span data-ttu-id="60f05-120">應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="60f05-120">The application ID.</span></span>

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

### <span data-ttu-id="60f05-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="60f05-121">-CertificateThumbprint</span></span>
<span data-ttu-id="60f05-122">憑證雜湊 (指紋) </span><span class="sxs-lookup"><span data-stu-id="60f05-122">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="60f05-123">-認證</span><span class="sxs-lookup"><span data-stu-id="60f05-123">-Credential</span></span>
<span data-ttu-id="60f05-124">登入認證</span><span class="sxs-lookup"><span data-stu-id="60f05-124">Login credentials</span></span>

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

### <span data-ttu-id="60f05-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="60f05-125">-RolloutEnvironment</span></span>
<span data-ttu-id="60f05-126">要登入之 Azure Analysis Services 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="60f05-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="60f05-127">考慮到伺服器的完整名稱（例如 asazure://westcentralus.asazure.windows.net/testserver），此變數的正確值將會 westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="60f05-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

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

### <span data-ttu-id="60f05-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="60f05-128">-ServicePrincipal</span></span>
<span data-ttu-id="60f05-129">指示此帳戶透過提供服務主體認證來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="60f05-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="60f05-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="60f05-130">-TenantId</span></span>
<span data-ttu-id="60f05-131">租使用者名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="60f05-131">Tenant name or ID</span></span>

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

### <span data-ttu-id="60f05-132">-確認</span><span class="sxs-lookup"><span data-stu-id="60f05-132">-Confirm</span></span>
<span data-ttu-id="60f05-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60f05-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60f05-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60f05-134">-WhatIf</span></span>
<span data-ttu-id="60f05-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60f05-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60f05-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60f05-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60f05-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f05-137">CommonParameters</span></span>
<span data-ttu-id="60f05-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60f05-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f05-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="60f05-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f05-140">輸入</span><span class="sxs-lookup"><span data-stu-id="60f05-140">INPUTS</span></span>

### <span data-ttu-id="60f05-141">所有</span><span class="sxs-lookup"><span data-stu-id="60f05-141">None</span></span>

## <span data-ttu-id="60f05-142">輸出</span><span class="sxs-lookup"><span data-stu-id="60f05-142">OUTPUTS</span></span>

### <span data-ttu-id="60f05-143">AnalysisServices. Dataplane. AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="60f05-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="60f05-144">筆記</span><span class="sxs-lookup"><span data-stu-id="60f05-144">NOTES</span></span>
<span data-ttu-id="60f05-145">別名： Login-AzAsAccount</span><span class="sxs-lookup"><span data-stu-id="60f05-145">Alias: Login-AzAsAccount</span></span>

## <span data-ttu-id="60f05-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="60f05-146">RELATED LINKS</span></span>

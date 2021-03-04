---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/add-azanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
ms.openlocfilehash: 523ccfb44d29473e41560de88d34519f98272375
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917813"
---
# <span data-ttu-id="f32c0-101">Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f32c0-101">Add-AzAnalysisServicesAccount</span></span>

## <span data-ttu-id="f32c0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f32c0-102">SYNOPSIS</span></span>
<span data-ttu-id="f32c0-103">新增已驗證的帳戶，以用於 Azure Analysis Services 伺服器 Cmdlet 要求。</span><span class="sxs-lookup"><span data-stu-id="f32c0-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

## <span data-ttu-id="f32c0-104">語法</span><span class="sxs-lookup"><span data-stu-id="f32c0-104">SYNTAX</span></span>

### <span data-ttu-id="f32c0-105">UserParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="f32c0-105">UserParameterSetName (Default)</span></span>
```
Add-AzAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f32c0-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f32c0-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f32c0-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f32c0-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f32c0-108">描述</span><span class="sxs-lookup"><span data-stu-id="f32c0-108">DESCRIPTION</span></span>
<span data-ttu-id="f32c0-109">Cmdlet Add-AzAnalysisServicesAccount用來登入 Azure Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="f32c0-109">The Add-AzAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="f32c0-110">例子</span><span class="sxs-lookup"><span data-stu-id="f32c0-110">EXAMPLES</span></span>

### <span data-ttu-id="f32c0-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f32c0-111">Example 1</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="f32c0-112">此範例會新增由 $UserCredential 變數指定的帳號westcentralus.asazure.windows.net Analysis Services 環境。</span><span class="sxs-lookup"><span data-stu-id="f32c0-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="f32c0-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="f32c0-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="f32c0-114">第一個命令會獲得應用程式服務主體認證，然後將這些認證儲存在$ApplicationCredential變數中。</span><span class="sxs-lookup"><span data-stu-id="f32c0-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="f32c0-115">第二個命令會新增由 $ApplicationCredential 變數和 TenantId 指定的應用程式服務主體帳戶westcentralus.asazure.windows.net Analysis Services 環境。</span><span class="sxs-lookup"><span data-stu-id="f32c0-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="f32c0-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="f32c0-116">Example 3</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="f32c0-117">此範例會新增 ApplicationId、TenantId 和 CertificateThumbprint 指定的應用程式服務主體帳戶至 westcentralus.asazure.windows.net Analysis Services 環境。</span><span class="sxs-lookup"><span data-stu-id="f32c0-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="f32c0-118">參數</span><span class="sxs-lookup"><span data-stu-id="f32c0-118">PARAMETERS</span></span>

### <span data-ttu-id="f32c0-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f32c0-119">-ApplicationId</span></span>
<span data-ttu-id="f32c0-120">應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="f32c0-120">The application ID.</span></span>

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

### <span data-ttu-id="f32c0-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="f32c0-121">-CertificateThumbprint</span></span>
<span data-ttu-id="f32c0-122">憑證雜湊 (指紋) </span><span class="sxs-lookup"><span data-stu-id="f32c0-122">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="f32c0-123">-認證</span><span class="sxs-lookup"><span data-stu-id="f32c0-123">-Credential</span></span>
<span data-ttu-id="f32c0-124">登入認證</span><span class="sxs-lookup"><span data-stu-id="f32c0-124">Login credentials</span></span>

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

### <span data-ttu-id="f32c0-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="f32c0-125">-RolloutEnvironment</span></span>
<span data-ttu-id="f32c0-126">要登入的 Azure Analysis Services 環境名稱。</span><span class="sxs-lookup"><span data-stu-id="f32c0-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="f32c0-127">假設伺服器的完整名稱 ，例如 asazure://westcentralus.asazure.windows.net/testserver，此變數的正確值將會westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="f32c0-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

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

### <span data-ttu-id="f32c0-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f32c0-128">-ServicePrincipal</span></span>
<span data-ttu-id="f32c0-129">表示此帳戶會提供服務主體認證來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="f32c0-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="f32c0-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="f32c0-130">-TenantId</span></span>
<span data-ttu-id="f32c0-131">租使用者名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="f32c0-131">Tenant name or ID</span></span>

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

### <span data-ttu-id="f32c0-132">-確認</span><span class="sxs-lookup"><span data-stu-id="f32c0-132">-Confirm</span></span>
<span data-ttu-id="f32c0-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f32c0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f32c0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f32c0-134">-WhatIf</span></span>
<span data-ttu-id="f32c0-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f32c0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f32c0-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f32c0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f32c0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f32c0-137">CommonParameters</span></span>
<span data-ttu-id="f32c0-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f32c0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f32c0-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f32c0-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f32c0-140">輸入</span><span class="sxs-lookup"><span data-stu-id="f32c0-140">INPUTS</span></span>

### <span data-ttu-id="f32c0-141">沒有</span><span class="sxs-lookup"><span data-stu-id="f32c0-141">None</span></span>

## <span data-ttu-id="f32c0-142">輸出</span><span class="sxs-lookup"><span data-stu-id="f32c0-142">OUTPUTS</span></span>

### <span data-ttu-id="f32c0-143">Microsoft.Azure.Commands.AnalysisServices.Dataservices.Dataservice.AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="f32c0-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="f32c0-144">筆記</span><span class="sxs-lookup"><span data-stu-id="f32c0-144">NOTES</span></span>
<span data-ttu-id="f32c0-145">別名：Login-AzAsAccount</span><span class="sxs-lookup"><span data-stu-id="f32c0-145">Alias: Login-AzAsAccount</span></span>

## <span data-ttu-id="f32c0-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="f32c0-146">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 98e160253db571c32fe14455b8642337029a9707
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905305"
---
# <span data-ttu-id="b0614-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="b0614-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="b0614-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b0614-102">SYNOPSIS</span></span>
<span data-ttu-id="b0614-103">為現有的閘道建立 hostname configuratin。</span><span class="sxs-lookup"><span data-stu-id="b0614-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="b0614-104">語法</span><span class="sxs-lookup"><span data-stu-id="b0614-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0614-105">描述</span><span class="sxs-lookup"><span data-stu-id="b0614-105">DESCRIPTION</span></span>
<span data-ttu-id="b0614-106">**New-AzApiManagementGatewayHostnameConfiguration** Cmdlet 會為現有的閘道建立 hostname configuratin。</span><span class="sxs-lookup"><span data-stu-id="b0614-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="b0614-107">例子</span><span class="sxs-lookup"><span data-stu-id="b0614-107">EXAMPLES</span></span>

### <span data-ttu-id="b0614-108">範例 1：建立現有閘道的主機名稱組</span><span class="sxs-lookup"><span data-stu-id="b0614-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="b0614-109">此命令會為「g01」閘道建立「h01」主機名稱組。</span><span class="sxs-lookup"><span data-stu-id="b0614-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="b0614-110">參數</span><span class="sxs-lookup"><span data-stu-id="b0614-110">PARAMETERS</span></span>

### <span data-ttu-id="b0614-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="b0614-111">-CertificateResourceId</span></span>
<span data-ttu-id="b0614-112">現有憑證識別碼的資源識別碼。此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="b0614-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0614-113">-內容</span><span class="sxs-lookup"><span data-stu-id="b0614-113">-Context</span></span>
<span data-ttu-id="b0614-114">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="b0614-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b0614-115">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="b0614-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0614-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0614-116">-DefaultProfile</span></span>
<span data-ttu-id="b0614-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0614-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0614-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b0614-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="b0614-119">新閘道主機名稱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0614-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="b0614-120">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b0614-120">This parameter is optional.</span></span>
<span data-ttu-id="b0614-121">如果未指定，將會產生。</span><span class="sxs-lookup"><span data-stu-id="b0614-121">If not specified will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0614-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="b0614-122">-GatewayId</span></span>
<span data-ttu-id="b0614-123">現有閘道的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0614-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="b0614-124">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="b0614-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0614-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="b0614-125">-Hostname</span></span>
<span data-ttu-id="b0614-126">主機 名。</span><span class="sxs-lookup"><span data-stu-id="b0614-126">Hostname.</span></span>
<span data-ttu-id="b0614-127">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="b0614-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0614-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b0614-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="b0614-129">標出以強制執行 NegotiateClientCertificate。</span><span class="sxs-lookup"><span data-stu-id="b0614-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="b0614-130">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b0614-130">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0614-131">-確認</span><span class="sxs-lookup"><span data-stu-id="b0614-131">-Confirm</span></span>
<span data-ttu-id="b0614-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b0614-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0614-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0614-133">-WhatIf</span></span>
<span data-ttu-id="b0614-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b0614-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0614-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0614-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0614-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0614-136">CommonParameters</span></span>
<span data-ttu-id="b0614-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b0614-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0614-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0614-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0614-139">輸入</span><span class="sxs-lookup"><span data-stu-id="b0614-139">INPUTS</span></span>

### <span data-ttu-id="b0614-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="b0614-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b0614-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b0614-141">System.String</span></span>

### <span data-ttu-id="b0614-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b0614-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b0614-143">輸出</span><span class="sxs-lookup"><span data-stu-id="b0614-143">OUTPUTS</span></span>

### <span data-ttu-id="b0614-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="b0614-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="b0614-145">筆記</span><span class="sxs-lookup"><span data-stu-id="b0614-145">NOTES</span></span>

## <span data-ttu-id="b0614-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0614-146">RELATED LINKS</span></span>

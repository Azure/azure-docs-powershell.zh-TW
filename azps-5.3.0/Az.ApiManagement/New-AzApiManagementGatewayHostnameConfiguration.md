---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 6aadf94ff379df322907be66c73052196de803c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447443"
---
# <span data-ttu-id="39d64-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="39d64-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="39d64-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39d64-102">SYNOPSIS</span></span>
<span data-ttu-id="39d64-103">為現有的閘道建立主機名稱 configuratin。</span><span class="sxs-lookup"><span data-stu-id="39d64-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="39d64-104">句法</span><span class="sxs-lookup"><span data-stu-id="39d64-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39d64-105">說明</span><span class="sxs-lookup"><span data-stu-id="39d64-105">DESCRIPTION</span></span>
<span data-ttu-id="39d64-106">**新的-AzApiManagementGatewayHostnameConfiguration** Cmdlet 會建立現有閘道的主機名稱 configuratin。</span><span class="sxs-lookup"><span data-stu-id="39d64-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="39d64-107">示例</span><span class="sxs-lookup"><span data-stu-id="39d64-107">EXAMPLES</span></span>

### <span data-ttu-id="39d64-108">範例1：建立現有閘道的主機名稱設定</span><span class="sxs-lookup"><span data-stu-id="39d64-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="39d64-109">這個命令會建立「g01」閘道的「h01」主機名稱設定。</span><span class="sxs-lookup"><span data-stu-id="39d64-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="39d64-110">參數</span><span class="sxs-lookup"><span data-stu-id="39d64-110">PARAMETERS</span></span>

### <span data-ttu-id="39d64-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="39d64-111">-CertificateResourceId</span></span>
<span data-ttu-id="39d64-112">現有憑證識別碼的資源識別碼。這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="39d64-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

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

### <span data-ttu-id="39d64-113">-內容</span><span class="sxs-lookup"><span data-stu-id="39d64-113">-Context</span></span>
<span data-ttu-id="39d64-114">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="39d64-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="39d64-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="39d64-115">This parameter is required.</span></span>

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

### <span data-ttu-id="39d64-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d64-116">-DefaultProfile</span></span>
<span data-ttu-id="39d64-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39d64-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39d64-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="39d64-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="39d64-119">新閘道主機名稱 confiuration 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="39d64-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="39d64-120">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="39d64-120">This parameter is optional.</span></span>
<span data-ttu-id="39d64-121">如果未指定，將會產生。</span><span class="sxs-lookup"><span data-stu-id="39d64-121">If not specified will be generated.</span></span>

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

### <span data-ttu-id="39d64-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="39d64-122">-GatewayId</span></span>
<span data-ttu-id="39d64-123">現有閘道的識別碼。</span><span class="sxs-lookup"><span data-stu-id="39d64-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="39d64-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="39d64-124">This parameter is required.</span></span>

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

### <span data-ttu-id="39d64-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="39d64-125">-Hostname</span></span>
<span data-ttu-id="39d64-126">主機.</span><span class="sxs-lookup"><span data-stu-id="39d64-126">Hostname.</span></span>
<span data-ttu-id="39d64-127">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="39d64-127">This parameter is required.</span></span>

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

### <span data-ttu-id="39d64-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="39d64-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="39d64-129">[旗標] 可強制 NegotiateClientCertificate。</span><span class="sxs-lookup"><span data-stu-id="39d64-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="39d64-130">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="39d64-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="39d64-131">-確認</span><span class="sxs-lookup"><span data-stu-id="39d64-131">-Confirm</span></span>
<span data-ttu-id="39d64-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="39d64-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39d64-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39d64-133">-WhatIf</span></span>
<span data-ttu-id="39d64-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="39d64-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39d64-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39d64-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39d64-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d64-136">CommonParameters</span></span>
<span data-ttu-id="39d64-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39d64-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d64-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="39d64-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d64-139">輸入</span><span class="sxs-lookup"><span data-stu-id="39d64-139">INPUTS</span></span>

### <span data-ttu-id="39d64-140">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="39d64-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="39d64-141">System.object</span><span class="sxs-lookup"><span data-stu-id="39d64-141">System.String</span></span>

### <span data-ttu-id="39d64-142">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="39d64-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="39d64-143">輸出</span><span class="sxs-lookup"><span data-stu-id="39d64-143">OUTPUTS</span></span>

### <span data-ttu-id="39d64-144">ServiceManagement. PsApiManagementGatewayHostnameConfiguration （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="39d64-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="39d64-145">筆記</span><span class="sxs-lookup"><span data-stu-id="39d64-145">NOTES</span></span>

## <span data-ttu-id="39d64-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="39d64-146">RELATED LINKS</span></span>

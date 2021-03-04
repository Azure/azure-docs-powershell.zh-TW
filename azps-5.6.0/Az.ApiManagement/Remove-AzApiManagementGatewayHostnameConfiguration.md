---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ad0c40e649384d4fb2bef9220f6ab8a994dea96c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917133"
---
# <span data-ttu-id="187b3-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="187b3-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="187b3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="187b3-102">SYNOPSIS</span></span>
<span data-ttu-id="187b3-103">移除現有閘道的主機名稱組。</span><span class="sxs-lookup"><span data-stu-id="187b3-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="187b3-104">語法</span><span class="sxs-lookup"><span data-stu-id="187b3-104">SYNTAX</span></span>

### <span data-ttu-id="187b3-105">CoNtextParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="187b3-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="187b3-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="187b3-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="187b3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="187b3-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="187b3-108">描述</span><span class="sxs-lookup"><span data-stu-id="187b3-108">DESCRIPTION</span></span>
<span data-ttu-id="187b3-109">**Remove-AzApiManagementGatewayHostnameConfiguration** Cmdlet 會移除現有閘道的主機名稱組式。</span><span class="sxs-lookup"><span data-stu-id="187b3-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="187b3-110">例子</span><span class="sxs-lookup"><span data-stu-id="187b3-110">EXAMPLES</span></span>

### <span data-ttu-id="187b3-111">範例 1：移除現有的閘道主機名稱組</span><span class="sxs-lookup"><span data-stu-id="187b3-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="187b3-112">此命令會移除現有的閘道主機名稱組，不會提示使用者確認。</span><span class="sxs-lookup"><span data-stu-id="187b3-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="187b3-113">參數</span><span class="sxs-lookup"><span data-stu-id="187b3-113">PARAMETERS</span></span>

### <span data-ttu-id="187b3-114">-內容</span><span class="sxs-lookup"><span data-stu-id="187b3-114">-Context</span></span>
<span data-ttu-id="187b3-115">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="187b3-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="187b3-116">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="187b3-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="187b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="187b3-117">-DefaultProfile</span></span>
<span data-ttu-id="187b3-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="187b3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="187b3-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="187b3-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="187b3-120">現有閘道主機名稱配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="187b3-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="187b3-121">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="187b3-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187b3-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="187b3-122">-GatewayId</span></span>
<span data-ttu-id="187b3-123">現有閘道的識別碼。</span><span class="sxs-lookup"><span data-stu-id="187b3-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="187b3-124">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="187b3-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187b3-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="187b3-125">-InputObject</span></span>
<span data-ttu-id="187b3-126">PsApiManagementGatewayHostnameConfiguration 的實例。</span><span class="sxs-lookup"><span data-stu-id="187b3-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="187b3-127">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="187b3-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="187b3-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="187b3-128">-PassThru</span></span>
<span data-ttu-id="187b3-129">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="187b3-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="187b3-130">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="187b3-130">This parameter is optional.</span></span>
<span data-ttu-id="187b3-131">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="187b3-131">Default value is false.</span></span>

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

### <span data-ttu-id="187b3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="187b3-132">-ResourceId</span></span>
<span data-ttu-id="187b3-133">GatewayHostnameConfiguration 的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="187b3-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="187b3-134">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="187b3-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187b3-135">-確認</span><span class="sxs-lookup"><span data-stu-id="187b3-135">-Confirm</span></span>
<span data-ttu-id="187b3-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="187b3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="187b3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="187b3-137">-WhatIf</span></span>
<span data-ttu-id="187b3-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="187b3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="187b3-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="187b3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="187b3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="187b3-140">CommonParameters</span></span>
<span data-ttu-id="187b3-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="187b3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="187b3-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="187b3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="187b3-143">輸入</span><span class="sxs-lookup"><span data-stu-id="187b3-143">INPUTS</span></span>

### <span data-ttu-id="187b3-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="187b3-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="187b3-145">System.String</span><span class="sxs-lookup"><span data-stu-id="187b3-145">System.String</span></span>

### <span data-ttu-id="187b3-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="187b3-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="187b3-147">輸出</span><span class="sxs-lookup"><span data-stu-id="187b3-147">OUTPUTS</span></span>

### <span data-ttu-id="187b3-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="187b3-148">System.Boolean</span></span>

## <span data-ttu-id="187b3-149">筆記</span><span class="sxs-lookup"><span data-stu-id="187b3-149">NOTES</span></span>

## <span data-ttu-id="187b3-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="187b3-150">RELATED LINKS</span></span>

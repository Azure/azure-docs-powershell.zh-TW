---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: e1999387cc2beb5a55fba3aef771a76440804f22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969993"
---
# <span data-ttu-id="f27ed-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f27ed-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="f27ed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f27ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f27ed-103">從現有的閘道中移除主機名稱設定。</span><span class="sxs-lookup"><span data-stu-id="f27ed-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="f27ed-104">句法</span><span class="sxs-lookup"><span data-stu-id="f27ed-104">SYNTAX</span></span>

### <span data-ttu-id="f27ed-105">CoNtextParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="f27ed-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f27ed-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f27ed-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f27ed-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f27ed-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f27ed-108">說明</span><span class="sxs-lookup"><span data-stu-id="f27ed-108">DESCRIPTION</span></span>
<span data-ttu-id="f27ed-109">**AzApiManagementGatewayHostnameConfiguration** Cmdlet 會從現有的閘道中移除主機名稱設定。</span><span class="sxs-lookup"><span data-stu-id="f27ed-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="f27ed-110">示例</span><span class="sxs-lookup"><span data-stu-id="f27ed-110">EXAMPLES</span></span>

### <span data-ttu-id="f27ed-111">範例1：移除現有的閘道主機名稱設定</span><span class="sxs-lookup"><span data-stu-id="f27ed-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="f27ed-112">這個命令會移除現有的閘道主機名稱設定，不會提示使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="f27ed-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="f27ed-113">參數</span><span class="sxs-lookup"><span data-stu-id="f27ed-113">PARAMETERS</span></span>

### <span data-ttu-id="f27ed-114">-內容</span><span class="sxs-lookup"><span data-stu-id="f27ed-114">-Context</span></span>
<span data-ttu-id="f27ed-115">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="f27ed-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f27ed-116">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f27ed-116">This parameter is required.</span></span>

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

### <span data-ttu-id="f27ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f27ed-117">-DefaultProfile</span></span>
<span data-ttu-id="f27ed-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f27ed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f27ed-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f27ed-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="f27ed-120">現有閘道主機名稱設定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f27ed-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="f27ed-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f27ed-121">This parameter is required.</span></span>

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

### <span data-ttu-id="f27ed-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="f27ed-122">-GatewayId</span></span>
<span data-ttu-id="f27ed-123">現有閘道的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f27ed-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="f27ed-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f27ed-124">This parameter is required.</span></span>

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

### <span data-ttu-id="f27ed-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f27ed-125">-InputObject</span></span>
<span data-ttu-id="f27ed-126">PsApiManagementGatewayHostnameConfiguration 的實例。</span><span class="sxs-lookup"><span data-stu-id="f27ed-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="f27ed-127">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f27ed-127">This parameter is required.</span></span>

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

### <span data-ttu-id="f27ed-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f27ed-128">-PassThru</span></span>
<span data-ttu-id="f27ed-129">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="f27ed-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="f27ed-130">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f27ed-130">This parameter is optional.</span></span>
<span data-ttu-id="f27ed-131">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="f27ed-131">Default value is false.</span></span>

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

### <span data-ttu-id="f27ed-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f27ed-132">-ResourceId</span></span>
<span data-ttu-id="f27ed-133">GatewayHostnameConfiguration 的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="f27ed-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="f27ed-134">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f27ed-134">This parameter is required.</span></span>

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

### <span data-ttu-id="f27ed-135">-確認</span><span class="sxs-lookup"><span data-stu-id="f27ed-135">-Confirm</span></span>
<span data-ttu-id="f27ed-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f27ed-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f27ed-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f27ed-137">-WhatIf</span></span>
<span data-ttu-id="f27ed-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f27ed-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f27ed-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f27ed-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f27ed-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f27ed-140">CommonParameters</span></span>
<span data-ttu-id="f27ed-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f27ed-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f27ed-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f27ed-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f27ed-143">輸入</span><span class="sxs-lookup"><span data-stu-id="f27ed-143">INPUTS</span></span>

### <span data-ttu-id="f27ed-144">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f27ed-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f27ed-145">System.object</span><span class="sxs-lookup"><span data-stu-id="f27ed-145">System.String</span></span>

### <span data-ttu-id="f27ed-146">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="f27ed-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f27ed-147">輸出</span><span class="sxs-lookup"><span data-stu-id="f27ed-147">OUTPUTS</span></span>

### <span data-ttu-id="f27ed-148">System.object</span><span class="sxs-lookup"><span data-stu-id="f27ed-148">System.Boolean</span></span>

## <span data-ttu-id="f27ed-149">筆記</span><span class="sxs-lookup"><span data-stu-id="f27ed-149">NOTES</span></span>

## <span data-ttu-id="f27ed-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="f27ed-150">RELATED LINKS</span></span>

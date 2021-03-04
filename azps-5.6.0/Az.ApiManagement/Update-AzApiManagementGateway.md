---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: 62131f634d049afe137b635d6a970d37e2173b8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914937"
---
# <span data-ttu-id="4daea-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="4daea-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="4daea-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4daea-102">SYNOPSIS</span></span>
<span data-ttu-id="4daea-103">設定 API 管理閘道。</span><span class="sxs-lookup"><span data-stu-id="4daea-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="4daea-104">語法</span><span class="sxs-lookup"><span data-stu-id="4daea-104">SYNTAX</span></span>

### <span data-ttu-id="4daea-105">展開Parameter (預設) </span><span class="sxs-lookup"><span data-stu-id="4daea-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4daea-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4daea-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4daea-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4daea-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4daea-108">描述</span><span class="sxs-lookup"><span data-stu-id="4daea-108">DESCRIPTION</span></span>
<span data-ttu-id="4daea-109">**Update-AzApiManagementGateway** Cmdlet 會設定 API 管理閘道。</span><span class="sxs-lookup"><span data-stu-id="4daea-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="4daea-110">例子</span><span class="sxs-lookup"><span data-stu-id="4daea-110">EXAMPLES</span></span>

### <span data-ttu-id="4daea-111">範例 1：設定管理群組</span><span class="sxs-lookup"><span data-stu-id="4daea-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="4daea-112">此命令會設定閘道。</span><span class="sxs-lookup"><span data-stu-id="4daea-112">This command configures a gateway.</span></span>

## <span data-ttu-id="4daea-113">參數</span><span class="sxs-lookup"><span data-stu-id="4daea-113">PARAMETERS</span></span>

### <span data-ttu-id="4daea-114">-內容</span><span class="sxs-lookup"><span data-stu-id="4daea-114">-Context</span></span>
<span data-ttu-id="4daea-115">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="4daea-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4daea-116">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="4daea-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4daea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4daea-117">-DefaultProfile</span></span>
<span data-ttu-id="4daea-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4daea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4daea-119">-描述</span><span class="sxs-lookup"><span data-stu-id="4daea-119">-Description</span></span>
<span data-ttu-id="4daea-120">閘道描述。</span><span class="sxs-lookup"><span data-stu-id="4daea-120">Gateway description.</span></span>
<span data-ttu-id="4daea-121">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="4daea-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="4daea-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="4daea-122">-GatewayId</span></span>
<span data-ttu-id="4daea-123">現有閘道的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4daea-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="4daea-124">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="4daea-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4daea-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4daea-125">-InputObject</span></span>
<span data-ttu-id="4daea-126">PsApiManagementGateway 的實例。</span><span class="sxs-lookup"><span data-stu-id="4daea-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="4daea-127">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="4daea-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4daea-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="4daea-128">-LocationData</span></span>
<span data-ttu-id="4daea-129">閘道位置。</span><span class="sxs-lookup"><span data-stu-id="4daea-129">Gateway location.</span></span>
<span data-ttu-id="4daea-130">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="4daea-130">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4daea-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4daea-131">-PassThru</span></span>
<span data-ttu-id="4daea-132">如果指定的話，代表已修改閘道的 Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway 類型實例。</span><span class="sxs-lookup"><span data-stu-id="4daea-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="4daea-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4daea-133">-ResourceId</span></span>
<span data-ttu-id="4daea-134">閘道的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="4daea-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="4daea-135">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="4daea-135">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4daea-136">-確認</span><span class="sxs-lookup"><span data-stu-id="4daea-136">-Confirm</span></span>
<span data-ttu-id="4daea-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4daea-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4daea-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4daea-138">-WhatIf</span></span>
<span data-ttu-id="4daea-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4daea-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4daea-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4daea-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4daea-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4daea-141">CommonParameters</span></span>
<span data-ttu-id="4daea-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4daea-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4daea-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4daea-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4daea-144">輸入</span><span class="sxs-lookup"><span data-stu-id="4daea-144">INPUTS</span></span>

### <span data-ttu-id="4daea-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="4daea-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4daea-146">System.String</span><span class="sxs-lookup"><span data-stu-id="4daea-146">System.String</span></span>

### <span data-ttu-id="4daea-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="4daea-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="4daea-148">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4daea-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4daea-149">輸出</span><span class="sxs-lookup"><span data-stu-id="4daea-149">OUTPUTS</span></span>

### <span data-ttu-id="4daea-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="4daea-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="4daea-151">筆記</span><span class="sxs-lookup"><span data-stu-id="4daea-151">NOTES</span></span>

## <span data-ttu-id="4daea-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="4daea-152">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 2ccd68fb5c1028408771e3011642797c8125ace3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912917"
---
# <span data-ttu-id="445a7-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="445a7-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="445a7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="445a7-102">SYNOPSIS</span></span>
<span data-ttu-id="445a7-103">將 API 與閘道分開。</span><span class="sxs-lookup"><span data-stu-id="445a7-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="445a7-104">語法</span><span class="sxs-lookup"><span data-stu-id="445a7-104">SYNTAX</span></span>

### <span data-ttu-id="445a7-105">CoNtextParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="445a7-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="445a7-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="445a7-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="445a7-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="445a7-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="445a7-108">描述</span><span class="sxs-lookup"><span data-stu-id="445a7-108">DESCRIPTION</span></span>
<span data-ttu-id="445a7-109">**Remove-AzApiManagementGateway** Cmdlet 會從閘道移除 API。</span><span class="sxs-lookup"><span data-stu-id="445a7-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="445a7-110">例子</span><span class="sxs-lookup"><span data-stu-id="445a7-110">EXAMPLES</span></span>

### <span data-ttu-id="445a7-111">範例 1：移除現有的閘道</span><span class="sxs-lookup"><span data-stu-id="445a7-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="445a7-112">此命令會移除現有的閘道，不會提示使用者確認。</span><span class="sxs-lookup"><span data-stu-id="445a7-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="445a7-113">參數</span><span class="sxs-lookup"><span data-stu-id="445a7-113">PARAMETERS</span></span>

### <span data-ttu-id="445a7-114">-內容</span><span class="sxs-lookup"><span data-stu-id="445a7-114">-Context</span></span>
<span data-ttu-id="445a7-115">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="445a7-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="445a7-116">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="445a7-116">This parameter is required.</span></span>

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

### <span data-ttu-id="445a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="445a7-117">-DefaultProfile</span></span>
<span data-ttu-id="445a7-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="445a7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="445a7-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="445a7-119">-GatewayId</span></span>
<span data-ttu-id="445a7-120">現有閘道的識別碼。</span><span class="sxs-lookup"><span data-stu-id="445a7-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="445a7-121">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="445a7-121">This parameter is required.</span></span>

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

### <span data-ttu-id="445a7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="445a7-122">-InputObject</span></span>
<span data-ttu-id="445a7-123">PsApiManagementGateway 的實例。</span><span class="sxs-lookup"><span data-stu-id="445a7-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="445a7-124">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="445a7-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="445a7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="445a7-125">-PassThru</span></span>
<span data-ttu-id="445a7-126">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="445a7-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="445a7-127">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="445a7-127">This parameter is optional.</span></span>
<span data-ttu-id="445a7-128">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="445a7-128">Default value is false.</span></span>

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

### <span data-ttu-id="445a7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="445a7-129">-ResourceId</span></span>
<span data-ttu-id="445a7-130">閘道的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="445a7-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="445a7-131">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="445a7-131">This parameter is required.</span></span>

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

### <span data-ttu-id="445a7-132">-確認</span><span class="sxs-lookup"><span data-stu-id="445a7-132">-Confirm</span></span>
<span data-ttu-id="445a7-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="445a7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="445a7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="445a7-134">-WhatIf</span></span>
<span data-ttu-id="445a7-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="445a7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="445a7-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="445a7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="445a7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="445a7-137">CommonParameters</span></span>
<span data-ttu-id="445a7-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="445a7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="445a7-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="445a7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="445a7-140">輸入</span><span class="sxs-lookup"><span data-stu-id="445a7-140">INPUTS</span></span>

### <span data-ttu-id="445a7-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="445a7-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="445a7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="445a7-142">System.String</span></span>

### <span data-ttu-id="445a7-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="445a7-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="445a7-144">輸出</span><span class="sxs-lookup"><span data-stu-id="445a7-144">OUTPUTS</span></span>

### <span data-ttu-id="445a7-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="445a7-145">System.Boolean</span></span>

## <span data-ttu-id="445a7-146">筆記</span><span class="sxs-lookup"><span data-stu-id="445a7-146">NOTES</span></span>

## <span data-ttu-id="445a7-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="445a7-147">RELATED LINKS</span></span>

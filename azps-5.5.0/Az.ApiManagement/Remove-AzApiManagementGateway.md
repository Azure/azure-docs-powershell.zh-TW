---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 9b6eac7a0c0c994797de51c936840da515ef3f4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128039"
---
# <span data-ttu-id="24150-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="24150-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="24150-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24150-102">SYNOPSIS</span></span>
<span data-ttu-id="24150-103">從閘道分離 API。</span><span class="sxs-lookup"><span data-stu-id="24150-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="24150-104">句法</span><span class="sxs-lookup"><span data-stu-id="24150-104">SYNTAX</span></span>

### <span data-ttu-id="24150-105">CoNtextParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="24150-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24150-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24150-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24150-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24150-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24150-108">說明</span><span class="sxs-lookup"><span data-stu-id="24150-108">DESCRIPTION</span></span>
<span data-ttu-id="24150-109">**AzApiManagementGateway** Cmdlet 會從閘道分離 API。</span><span class="sxs-lookup"><span data-stu-id="24150-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="24150-110">示例</span><span class="sxs-lookup"><span data-stu-id="24150-110">EXAMPLES</span></span>

### <span data-ttu-id="24150-111">範例1：移除現有的閘道</span><span class="sxs-lookup"><span data-stu-id="24150-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="24150-112">這個命令會移除現有的閘道，不會提示使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="24150-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="24150-113">參數</span><span class="sxs-lookup"><span data-stu-id="24150-113">PARAMETERS</span></span>

### <span data-ttu-id="24150-114">-內容</span><span class="sxs-lookup"><span data-stu-id="24150-114">-Context</span></span>
<span data-ttu-id="24150-115">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="24150-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="24150-116">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="24150-116">This parameter is required.</span></span>

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

### <span data-ttu-id="24150-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24150-117">-DefaultProfile</span></span>
<span data-ttu-id="24150-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24150-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24150-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="24150-119">-GatewayId</span></span>
<span data-ttu-id="24150-120">現有閘道的識別碼。</span><span class="sxs-lookup"><span data-stu-id="24150-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="24150-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="24150-121">This parameter is required.</span></span>

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

### <span data-ttu-id="24150-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24150-122">-InputObject</span></span>
<span data-ttu-id="24150-123">PsApiManagementGateway 的實例。</span><span class="sxs-lookup"><span data-stu-id="24150-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="24150-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="24150-124">This parameter is required.</span></span>

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

### <span data-ttu-id="24150-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24150-125">-PassThru</span></span>
<span data-ttu-id="24150-126">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="24150-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="24150-127">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="24150-127">This parameter is optional.</span></span>
<span data-ttu-id="24150-128">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="24150-128">Default value is false.</span></span>

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

### <span data-ttu-id="24150-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24150-129">-ResourceId</span></span>
<span data-ttu-id="24150-130">閘道的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="24150-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="24150-131">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="24150-131">This parameter is required.</span></span>

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

### <span data-ttu-id="24150-132">-確認</span><span class="sxs-lookup"><span data-stu-id="24150-132">-Confirm</span></span>
<span data-ttu-id="24150-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24150-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24150-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24150-134">-WhatIf</span></span>
<span data-ttu-id="24150-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24150-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24150-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24150-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24150-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24150-137">CommonParameters</span></span>
<span data-ttu-id="24150-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24150-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24150-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="24150-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24150-140">輸入</span><span class="sxs-lookup"><span data-stu-id="24150-140">INPUTS</span></span>

### <span data-ttu-id="24150-141">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="24150-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="24150-142">System.object</span><span class="sxs-lookup"><span data-stu-id="24150-142">System.String</span></span>

### <span data-ttu-id="24150-143">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="24150-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="24150-144">輸出</span><span class="sxs-lookup"><span data-stu-id="24150-144">OUTPUTS</span></span>

### <span data-ttu-id="24150-145">System.object</span><span class="sxs-lookup"><span data-stu-id="24150-145">System.Boolean</span></span>

## <span data-ttu-id="24150-146">筆記</span><span class="sxs-lookup"><span data-stu-id="24150-146">NOTES</span></span>

## <span data-ttu-id="24150-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="24150-147">RELATED LINKS</span></span>

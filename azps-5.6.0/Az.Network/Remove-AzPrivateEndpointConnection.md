---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: be060c320c05b44a4b0d8f79b519f63e4dd47bcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913381"
---
# <span data-ttu-id="58b2d-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="58b2d-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="58b2d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="58b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="58b2d-103">移除私人端點連接。</span><span class="sxs-lookup"><span data-stu-id="58b2d-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="58b2d-104">語法</span><span class="sxs-lookup"><span data-stu-id="58b2d-104">SYNTAX</span></span>

### <span data-ttu-id="58b2d-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="58b2d-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58b2d-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="58b2d-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58b2d-107">描述</span><span class="sxs-lookup"><span data-stu-id="58b2d-107">DESCRIPTION</span></span>
<span data-ttu-id="58b2d-108">**Remove-AzPrivateEndpointConnection** Cmdlet 會移除私人端點連接。</span><span class="sxs-lookup"><span data-stu-id="58b2d-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="58b2d-109">例子</span><span class="sxs-lookup"><span data-stu-id="58b2d-109">EXAMPLES</span></span>

### <span data-ttu-id="58b2d-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="58b2d-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="58b2d-111">此範例移除名為 MyPrivateEndpointConnection1 的私人端點連接</span><span class="sxs-lookup"><span data-stu-id="58b2d-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="58b2d-112">參數</span><span class="sxs-lookup"><span data-stu-id="58b2d-112">PARAMETERS</span></span>

### <span data-ttu-id="58b2d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58b2d-113">-AsJob</span></span>
<span data-ttu-id="58b2d-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="58b2d-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58b2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b2d-115">-DefaultProfile</span></span>
<span data-ttu-id="58b2d-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="58b2d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58b2d-117">-強制</span><span class="sxs-lookup"><span data-stu-id="58b2d-117">-Force</span></span>
<span data-ttu-id="58b2d-118">如果您要刪除資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="58b2d-118">Do not ask for confirmation if you want to delete resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58b2d-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="58b2d-119">-Name</span></span>
<span data-ttu-id="58b2d-120">私人端點連接的名稱。</span><span class="sxs-lookup"><span data-stu-id="58b2d-120">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58b2d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58b2d-121">-PassThru</span></span>
<span data-ttu-id="58b2d-122">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="58b2d-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="58b2d-123">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="58b2d-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58b2d-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="58b2d-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="58b2d-125">私人連結資源類型。</span><span class="sxs-lookup"><span data-stu-id="58b2d-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58b2d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58b2d-126">-ResourceGroupName</span></span>
<span data-ttu-id="58b2d-127">私人端點連接的資源組名。</span><span class="sxs-lookup"><span data-stu-id="58b2d-127">The resource group name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58b2d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58b2d-128">-ResourceId</span></span>
<span data-ttu-id="58b2d-129">私人端點連接的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="58b2d-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="58b2d-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="58b2d-130">-ServiceName</span></span>
<span data-ttu-id="58b2d-131">私人端點連接所屬的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="58b2d-131">The name of service that the private endpoint connection belong to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58b2d-132">-確認</span><span class="sxs-lookup"><span data-stu-id="58b2d-132">-Confirm</span></span>
<span data-ttu-id="58b2d-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="58b2d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58b2d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58b2d-134">-WhatIf</span></span>
<span data-ttu-id="58b2d-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58b2d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58b2d-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58b2d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58b2d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b2d-137">CommonParameters</span></span>
<span data-ttu-id="58b2d-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="58b2d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b2d-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58b2d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b2d-140">輸入</span><span class="sxs-lookup"><span data-stu-id="58b2d-140">INPUTS</span></span>

### <span data-ttu-id="58b2d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="58b2d-141">System.String</span></span>

## <span data-ttu-id="58b2d-142">輸出</span><span class="sxs-lookup"><span data-stu-id="58b2d-142">OUTPUTS</span></span>

### <span data-ttu-id="58b2d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="58b2d-143">System.Boolean</span></span>

## <span data-ttu-id="58b2d-144">筆記</span><span class="sxs-lookup"><span data-stu-id="58b2d-144">NOTES</span></span>

## <span data-ttu-id="58b2d-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="58b2d-145">RELATED LINKS</span></span>

[<span data-ttu-id="58b2d-146">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="58b2d-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="58b2d-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="58b2d-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="58b2d-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="58b2d-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="58b2d-149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="58b2d-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)

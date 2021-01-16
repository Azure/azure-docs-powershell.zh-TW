---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 2b7b6755b15c5dcaf0442557eb32b563f0c1af6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280225"
---
# <span data-ttu-id="9c279-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9c279-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="9c279-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c279-102">SYNOPSIS</span></span>
<span data-ttu-id="9c279-103">移除私人端點連線。</span><span class="sxs-lookup"><span data-stu-id="9c279-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="9c279-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c279-104">SYNTAX</span></span>

### <span data-ttu-id="9c279-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="9c279-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c279-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="9c279-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c279-107">說明</span><span class="sxs-lookup"><span data-stu-id="9c279-107">DESCRIPTION</span></span>
<span data-ttu-id="9c279-108">**AzPrivateEndpointConnection** Cmdlet 會移除私用端點連線。</span><span class="sxs-lookup"><span data-stu-id="9c279-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="9c279-109">示例</span><span class="sxs-lookup"><span data-stu-id="9c279-109">EXAMPLES</span></span>

### <span data-ttu-id="9c279-110">範例1</span><span class="sxs-lookup"><span data-stu-id="9c279-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="9c279-111">這個範例會移除名為 MyPrivateEndpointConnection1 的私人端點連接</span><span class="sxs-lookup"><span data-stu-id="9c279-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="9c279-112">參數</span><span class="sxs-lookup"><span data-stu-id="9c279-112">PARAMETERS</span></span>

### <span data-ttu-id="9c279-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c279-113">-AsJob</span></span>
<span data-ttu-id="9c279-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9c279-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c279-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c279-115">-DefaultProfile</span></span>
<span data-ttu-id="9c279-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c279-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c279-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9c279-117">-Force</span></span>
<span data-ttu-id="9c279-118">如果您想要刪除資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="9c279-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="9c279-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="9c279-119">-Name</span></span>
<span data-ttu-id="9c279-120">私人端點連接的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c279-120">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="9c279-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c279-121">-PassThru</span></span>
<span data-ttu-id="9c279-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="9c279-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9c279-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="9c279-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9c279-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="9c279-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="9c279-125">私人連結資源類型。</span><span class="sxs-lookup"><span data-stu-id="9c279-125">The private link resource type.</span></span>

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

### <span data-ttu-id="9c279-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c279-126">-ResourceGroupName</span></span>
<span data-ttu-id="9c279-127">私人端點連線的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9c279-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="9c279-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c279-128">-ResourceId</span></span>
<span data-ttu-id="9c279-129">專用端點連接的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c279-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="9c279-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9c279-130">-ServiceName</span></span>
<span data-ttu-id="9c279-131">私人端點連線所屬的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="9c279-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="9c279-132">-確認</span><span class="sxs-lookup"><span data-stu-id="9c279-132">-Confirm</span></span>
<span data-ttu-id="9c279-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9c279-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c279-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c279-134">-WhatIf</span></span>
<span data-ttu-id="9c279-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9c279-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c279-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c279-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c279-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c279-137">CommonParameters</span></span>
<span data-ttu-id="9c279-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c279-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c279-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9c279-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c279-140">輸入</span><span class="sxs-lookup"><span data-stu-id="9c279-140">INPUTS</span></span>

### <span data-ttu-id="9c279-141">System.object</span><span class="sxs-lookup"><span data-stu-id="9c279-141">System.String</span></span>

## <span data-ttu-id="9c279-142">輸出</span><span class="sxs-lookup"><span data-stu-id="9c279-142">OUTPUTS</span></span>

### <span data-ttu-id="9c279-143">System.object</span><span class="sxs-lookup"><span data-stu-id="9c279-143">System.Boolean</span></span>

## <span data-ttu-id="9c279-144">筆記</span><span class="sxs-lookup"><span data-stu-id="9c279-144">NOTES</span></span>

## <span data-ttu-id="9c279-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c279-145">RELATED LINKS</span></span>

[<span data-ttu-id="9c279-146">核准-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9c279-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9c279-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9c279-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9c279-148">AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9c279-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9c279-149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9c279-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)

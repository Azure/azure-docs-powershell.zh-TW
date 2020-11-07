---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 9de25adae04afd0f09a2a09118c55d4e679a44db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790606"
---
# <span data-ttu-id="ee00f-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ee00f-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="ee00f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ee00f-102">SYNOPSIS</span></span>
<span data-ttu-id="ee00f-103">移除私人端點連線。</span><span class="sxs-lookup"><span data-stu-id="ee00f-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="ee00f-104">句法</span><span class="sxs-lookup"><span data-stu-id="ee00f-104">SYNTAX</span></span>

### <span data-ttu-id="ee00f-105">ByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="ee00f-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee00f-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="ee00f-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -Name <String> -ServiceName <String>
 -ResourceGroupName <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee00f-107">說明</span><span class="sxs-lookup"><span data-stu-id="ee00f-107">DESCRIPTION</span></span>
<span data-ttu-id="ee00f-108">**AzPrivateEndpointConnection** Cmdlet 會移除私用端點連線。</span><span class="sxs-lookup"><span data-stu-id="ee00f-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span> 

## <span data-ttu-id="ee00f-109">示例</span><span class="sxs-lookup"><span data-stu-id="ee00f-109">EXAMPLES</span></span>

### <span data-ttu-id="ee00f-110">範例1</span><span class="sxs-lookup"><span data-stu-id="ee00f-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="ee00f-111">這個範例會移除名為 MyPrivateEndpointConnection1 的私人端點連接</span><span class="sxs-lookup"><span data-stu-id="ee00f-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="ee00f-112">參數</span><span class="sxs-lookup"><span data-stu-id="ee00f-112">PARAMETERS</span></span>

### <span data-ttu-id="ee00f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee00f-113">-AsJob</span></span>
<span data-ttu-id="ee00f-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ee00f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee00f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee00f-115">-DefaultProfile</span></span>
<span data-ttu-id="ee00f-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee00f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee00f-117">-描述</span><span class="sxs-lookup"><span data-stu-id="ee00f-117">-Description</span></span>
<span data-ttu-id="ee00f-118">動作的原因。</span><span class="sxs-lookup"><span data-stu-id="ee00f-118">The reason of action.</span></span>

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

### <span data-ttu-id="ee00f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ee00f-119">-Force</span></span>
<span data-ttu-id="ee00f-120">如果您想要刪除資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="ee00f-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="ee00f-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ee00f-121">-Name</span></span>
<span data-ttu-id="ee00f-122">私人端點連接的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee00f-122">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="ee00f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee00f-123">-PassThru</span></span>
<span data-ttu-id="ee00f-124">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ee00f-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ee00f-125">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ee00f-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ee00f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee00f-126">-ResourceGroupName</span></span>
<span data-ttu-id="ee00f-127">私人端點連線的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ee00f-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="ee00f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee00f-128">-ResourceId</span></span>
<span data-ttu-id="ee00f-129">專用端點連接的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee00f-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="ee00f-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ee00f-130">-ServiceName</span></span>
<span data-ttu-id="ee00f-131">具有專用端點連線之專用連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee00f-131">The name of the private link service that has the private endpoint connection.</span></span>

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

### <span data-ttu-id="ee00f-132">-確認</span><span class="sxs-lookup"><span data-stu-id="ee00f-132">-Confirm</span></span>
<span data-ttu-id="ee00f-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ee00f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee00f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee00f-134">-WhatIf</span></span>
<span data-ttu-id="ee00f-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ee00f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee00f-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee00f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee00f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee00f-137">CommonParameters</span></span>
<span data-ttu-id="ee00f-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ee00f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee00f-139">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ee00f-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee00f-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ee00f-140">INPUTS</span></span>

### <span data-ttu-id="ee00f-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ee00f-141">System.String</span></span>

## <span data-ttu-id="ee00f-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ee00f-142">OUTPUTS</span></span>

### <span data-ttu-id="ee00f-143">System.object</span><span class="sxs-lookup"><span data-stu-id="ee00f-143">System.Boolean</span></span>

## <span data-ttu-id="ee00f-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ee00f-144">NOTES</span></span>

## <span data-ttu-id="ee00f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee00f-145">RELATED LINKS</span></span>

[<span data-ttu-id="ee00f-146">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ee00f-146">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)

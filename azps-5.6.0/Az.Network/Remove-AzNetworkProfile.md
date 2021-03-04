---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 02a8fef51ca0689fb92d3990bf5bcc182f902549
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913406"
---
# <span data-ttu-id="9806f-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9806f-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="9806f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9806f-102">SYNOPSIS</span></span>
<span data-ttu-id="9806f-103">移除網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="9806f-103">Removes a network profile.</span></span>

## <span data-ttu-id="9806f-104">語法</span><span class="sxs-lookup"><span data-stu-id="9806f-104">SYNTAX</span></span>

### <span data-ttu-id="9806f-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9806f-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9806f-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9806f-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9806f-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9806f-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9806f-108">描述</span><span class="sxs-lookup"><span data-stu-id="9806f-108">DESCRIPTION</span></span>
<span data-ttu-id="9806f-109">如果沒有建立與容器網路介面組 (相反的容器網路介面 **，Remove-AzNetworkProfile** Cmdlet 會移除網路設定檔) 。 </span><span class="sxs-lookup"><span data-stu-id="9806f-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration**) have been created.</span></span>

## <span data-ttu-id="9806f-110">例子</span><span class="sxs-lookup"><span data-stu-id="9806f-110">EXAMPLES</span></span>

### <span data-ttu-id="9806f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="9806f-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="9806f-112">這會從資源群組 rg1 移除名稱為 np1 的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="9806f-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="9806f-113">參數</span><span class="sxs-lookup"><span data-stu-id="9806f-113">PARAMETERS</span></span>

### <span data-ttu-id="9806f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9806f-114">-AsJob</span></span>
<span data-ttu-id="9806f-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9806f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9806f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9806f-116">-DefaultProfile</span></span>
<span data-ttu-id="9806f-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9806f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9806f-118">-強制</span><span class="sxs-lookup"><span data-stu-id="9806f-118">-Force</span></span>
<span data-ttu-id="9806f-119">如果您要刪除資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="9806f-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="9806f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9806f-120">-InputObject</span></span>
<span data-ttu-id="9806f-121">網路設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="9806f-121">Network profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9806f-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="9806f-122">-Name</span></span>
<span data-ttu-id="9806f-123">網路設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="9806f-123">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9806f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9806f-124">-PassThru</span></span>
<span data-ttu-id="9806f-125">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="9806f-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="9806f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9806f-126">-ResourceGroupName</span></span>
<span data-ttu-id="9806f-127">網路設定檔的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9806f-127">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9806f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9806f-128">-ResourceId</span></span>
<span data-ttu-id="9806f-129">網路設定檔的 Azure 資源管理器資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9806f-129">The Azure resource manager resource ID of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9806f-130">-確認</span><span class="sxs-lookup"><span data-stu-id="9806f-130">-Confirm</span></span>
<span data-ttu-id="9806f-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9806f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9806f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9806f-132">-WhatIf</span></span>
<span data-ttu-id="9806f-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9806f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9806f-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9806f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9806f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9806f-135">CommonParameters</span></span>
<span data-ttu-id="9806f-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9806f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9806f-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9806f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9806f-138">輸入</span><span class="sxs-lookup"><span data-stu-id="9806f-138">INPUTS</span></span>

### <span data-ttu-id="9806f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9806f-139">System.String</span></span>

### <span data-ttu-id="9806f-140">Microsoft.Azure.Commands.Network.models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9806f-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="9806f-141">輸出</span><span class="sxs-lookup"><span data-stu-id="9806f-141">OUTPUTS</span></span>

### <span data-ttu-id="9806f-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9806f-142">System.Boolean</span></span>

## <span data-ttu-id="9806f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="9806f-143">NOTES</span></span>

## <span data-ttu-id="9806f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="9806f-144">RELATED LINKS</span></span>

[<span data-ttu-id="9806f-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9806f-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="9806f-146">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9806f-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="9806f-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9806f-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)

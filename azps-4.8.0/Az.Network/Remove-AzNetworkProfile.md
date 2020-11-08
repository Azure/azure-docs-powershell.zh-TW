---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 3a83b7200f7634574fd457d2fa08f926a62b9a82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126401"
---
# <span data-ttu-id="8431d-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8431d-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="8431d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8431d-102">SYNOPSIS</span></span>
<span data-ttu-id="8431d-103">移除網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="8431d-103">Removes a network profile.</span></span>

## <span data-ttu-id="8431d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8431d-104">SYNTAX</span></span>

### <span data-ttu-id="8431d-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8431d-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8431d-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8431d-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8431d-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8431d-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8431d-108">說明</span><span class="sxs-lookup"><span data-stu-id="8431d-108">DESCRIPTION</span></span>
<span data-ttu-id="8431d-109">如果沒有容器網路介面 (與已建立的容器網路介面 **配置** ) 相對，則 **Remove AzNetworkProfile** Cmdlet 會移除網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="8431d-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="8431d-110">示例</span><span class="sxs-lookup"><span data-stu-id="8431d-110">EXAMPLES</span></span>

### <span data-ttu-id="8431d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8431d-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="8431d-112">這會從資源群組 rg1 中移除名稱為 np1 的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="8431d-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="8431d-113">參數</span><span class="sxs-lookup"><span data-stu-id="8431d-113">PARAMETERS</span></span>

### <span data-ttu-id="8431d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8431d-114">-AsJob</span></span>
<span data-ttu-id="8431d-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8431d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8431d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8431d-116">-DefaultProfile</span></span>
<span data-ttu-id="8431d-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8431d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8431d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8431d-118">-Force</span></span>
<span data-ttu-id="8431d-119">如果您想要刪除資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="8431d-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="8431d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8431d-120">-InputObject</span></span>
<span data-ttu-id="8431d-121">網路設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="8431d-121">Network profile object.</span></span>

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

### <span data-ttu-id="8431d-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="8431d-122">-Name</span></span>
<span data-ttu-id="8431d-123">網路設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="8431d-123">The name of the network profile.</span></span>

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

### <span data-ttu-id="8431d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8431d-124">-PassThru</span></span>
<span data-ttu-id="8431d-125">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="8431d-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="8431d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8431d-126">-ResourceGroupName</span></span>
<span data-ttu-id="8431d-127">網路設定檔的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8431d-127">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="8431d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8431d-128">-ResourceId</span></span>
<span data-ttu-id="8431d-129">網路設定檔的 Azure 資源管理員資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8431d-129">The Azure resource manager resource ID of the network profile.</span></span>

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

### <span data-ttu-id="8431d-130">-確認</span><span class="sxs-lookup"><span data-stu-id="8431d-130">-Confirm</span></span>
<span data-ttu-id="8431d-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8431d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8431d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8431d-132">-WhatIf</span></span>
<span data-ttu-id="8431d-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8431d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8431d-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8431d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8431d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8431d-135">CommonParameters</span></span>
<span data-ttu-id="8431d-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8431d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8431d-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8431d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8431d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="8431d-138">INPUTS</span></span>

### <span data-ttu-id="8431d-139">System.object</span><span class="sxs-lookup"><span data-stu-id="8431d-139">System.String</span></span>

### <span data-ttu-id="8431d-140">PSNetworkProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8431d-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="8431d-141">輸出</span><span class="sxs-lookup"><span data-stu-id="8431d-141">OUTPUTS</span></span>

### <span data-ttu-id="8431d-142">System.object</span><span class="sxs-lookup"><span data-stu-id="8431d-142">System.Boolean</span></span>

## <span data-ttu-id="8431d-143">筆記</span><span class="sxs-lookup"><span data-stu-id="8431d-143">NOTES</span></span>

## <span data-ttu-id="8431d-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="8431d-144">RELATED LINKS</span></span>

[<span data-ttu-id="8431d-145">AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8431d-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="8431d-146">新-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8431d-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="8431d-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8431d-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
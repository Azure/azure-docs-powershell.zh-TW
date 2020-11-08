---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126399"
---
# <span data-ttu-id="cf6ff-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="cf6ff-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="cf6ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf6ff-102">SYNOPSIS</span></span>
<span data-ttu-id="cf6ff-103">移除網路虛擬裝置資源。</span><span class="sxs-lookup"><span data-stu-id="cf6ff-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="cf6ff-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf6ff-104">SYNTAX</span></span>

### <span data-ttu-id="cf6ff-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cf6ff-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf6ff-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf6ff-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf6ff-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf6ff-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf6ff-108">說明</span><span class="sxs-lookup"><span data-stu-id="cf6ff-108">DESCRIPTION</span></span>
<span data-ttu-id="cf6ff-109">[Remove-AzNetworkVirtualAppliance] 命令會移除網路虛擬裝置資源。</span><span class="sxs-lookup"><span data-stu-id="cf6ff-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="cf6ff-110">示例</span><span class="sxs-lookup"><span data-stu-id="cf6ff-110">EXAMPLES</span></span>

### <span data-ttu-id="cf6ff-111">範例1</span><span class="sxs-lookup"><span data-stu-id="cf6ff-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="cf6ff-112">刪除網路虛擬裝置資源。</span><span class="sxs-lookup"><span data-stu-id="cf6ff-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="cf6ff-113">參數</span><span class="sxs-lookup"><span data-stu-id="cf6ff-113">PARAMETERS</span></span>

### <span data-ttu-id="cf6ff-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf6ff-114">-AsJob</span></span>
<span data-ttu-id="cf6ff-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cf6ff-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf6ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf6ff-116">-DefaultProfile</span></span>
<span data-ttu-id="cf6ff-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf6ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf6ff-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cf6ff-118">-Force</span></span>
<span data-ttu-id="cf6ff-119">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="cf6ff-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cf6ff-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf6ff-120">-Name</span></span>
<span data-ttu-id="cf6ff-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="cf6ff-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf6ff-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="cf6ff-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="cf6ff-123">資源物件。</span><span class="sxs-lookup"><span data-stu-id="cf6ff-123">The resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf6ff-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf6ff-124">-PassThru</span></span>
<span data-ttu-id="cf6ff-125">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="cf6ff-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="cf6ff-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="cf6ff-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cf6ff-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf6ff-127">-ResourceGroupName</span></span>
<span data-ttu-id="cf6ff-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf6ff-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf6ff-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf6ff-129">-ResourceId</span></span>
<span data-ttu-id="cf6ff-130">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="cf6ff-130">The Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf6ff-131">-確認</span><span class="sxs-lookup"><span data-stu-id="cf6ff-131">-Confirm</span></span>
<span data-ttu-id="cf6ff-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cf6ff-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf6ff-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf6ff-133">-WhatIf</span></span>
<span data-ttu-id="cf6ff-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf6ff-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf6ff-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf6ff-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf6ff-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf6ff-136">CommonParameters</span></span>
<span data-ttu-id="cf6ff-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf6ff-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf6ff-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cf6ff-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf6ff-139">輸入</span><span class="sxs-lookup"><span data-stu-id="cf6ff-139">INPUTS</span></span>

### <span data-ttu-id="cf6ff-140">System.object</span><span class="sxs-lookup"><span data-stu-id="cf6ff-140">System.String</span></span>

### <span data-ttu-id="cf6ff-141">PSNetworkVirtualAppliance 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cf6ff-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="cf6ff-142">輸出</span><span class="sxs-lookup"><span data-stu-id="cf6ff-142">OUTPUTS</span></span>

### <span data-ttu-id="cf6ff-143">System.object</span><span class="sxs-lookup"><span data-stu-id="cf6ff-143">System.Boolean</span></span>

## <span data-ttu-id="cf6ff-144">筆記</span><span class="sxs-lookup"><span data-stu-id="cf6ff-144">NOTES</span></span>

## <span data-ttu-id="cf6ff-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf6ff-145">RELATED LINKS</span></span>
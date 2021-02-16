---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132487"
---
# <span data-ttu-id="ccbe7-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="ccbe7-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="ccbe7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ccbe7-102">SYNOPSIS</span></span>
<span data-ttu-id="ccbe7-103">移除網路虛擬裝置資源。</span><span class="sxs-lookup"><span data-stu-id="ccbe7-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="ccbe7-104">句法</span><span class="sxs-lookup"><span data-stu-id="ccbe7-104">SYNTAX</span></span>

### <span data-ttu-id="ccbe7-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ccbe7-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccbe7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccbe7-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccbe7-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccbe7-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccbe7-108">說明</span><span class="sxs-lookup"><span data-stu-id="ccbe7-108">DESCRIPTION</span></span>
<span data-ttu-id="ccbe7-109">[Remove-AzNetworkVirtualAppliance] 命令會移除網路虛擬裝置資源。</span><span class="sxs-lookup"><span data-stu-id="ccbe7-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="ccbe7-110">示例</span><span class="sxs-lookup"><span data-stu-id="ccbe7-110">EXAMPLES</span></span>

### <span data-ttu-id="ccbe7-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ccbe7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="ccbe7-112">刪除網路虛擬裝置資源。</span><span class="sxs-lookup"><span data-stu-id="ccbe7-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="ccbe7-113">參數</span><span class="sxs-lookup"><span data-stu-id="ccbe7-113">PARAMETERS</span></span>

### <span data-ttu-id="ccbe7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccbe7-114">-AsJob</span></span>
<span data-ttu-id="ccbe7-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ccbe7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccbe7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccbe7-116">-DefaultProfile</span></span>
<span data-ttu-id="ccbe7-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ccbe7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccbe7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ccbe7-118">-Force</span></span>
<span data-ttu-id="ccbe7-119">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="ccbe7-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ccbe7-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ccbe7-120">-Name</span></span>
<span data-ttu-id="ccbe7-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ccbe7-121">The resource name.</span></span>

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

### <span data-ttu-id="ccbe7-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="ccbe7-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="ccbe7-123">資源物件。</span><span class="sxs-lookup"><span data-stu-id="ccbe7-123">The resource object.</span></span>

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

### <span data-ttu-id="ccbe7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccbe7-124">-PassThru</span></span>
<span data-ttu-id="ccbe7-125">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ccbe7-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="ccbe7-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ccbe7-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ccbe7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccbe7-127">-ResourceGroupName</span></span>
<span data-ttu-id="ccbe7-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ccbe7-128">The resource group name.</span></span>

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

### <span data-ttu-id="ccbe7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccbe7-129">-ResourceId</span></span>
<span data-ttu-id="ccbe7-130">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="ccbe7-130">The Resource Id.</span></span>

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

### <span data-ttu-id="ccbe7-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ccbe7-131">-Confirm</span></span>
<span data-ttu-id="ccbe7-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ccbe7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccbe7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccbe7-133">-WhatIf</span></span>
<span data-ttu-id="ccbe7-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ccbe7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccbe7-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ccbe7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccbe7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccbe7-136">CommonParameters</span></span>
<span data-ttu-id="ccbe7-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ccbe7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccbe7-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ccbe7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccbe7-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ccbe7-139">INPUTS</span></span>

### <span data-ttu-id="ccbe7-140">System.object</span><span class="sxs-lookup"><span data-stu-id="ccbe7-140">System.String</span></span>

### <span data-ttu-id="ccbe7-141">PSNetworkVirtualAppliance 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ccbe7-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="ccbe7-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ccbe7-142">OUTPUTS</span></span>

### <span data-ttu-id="ccbe7-143">System.object</span><span class="sxs-lookup"><span data-stu-id="ccbe7-143">System.Boolean</span></span>

## <span data-ttu-id="ccbe7-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ccbe7-144">NOTES</span></span>

## <span data-ttu-id="ccbe7-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ccbe7-145">RELATED LINKS</span></span>

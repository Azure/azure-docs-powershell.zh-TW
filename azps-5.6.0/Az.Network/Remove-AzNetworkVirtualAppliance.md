---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: b75eb7e9bbac3efddc49bcccf384f288c01960a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913401"
---
# <span data-ttu-id="5436b-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="5436b-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="5436b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5436b-102">SYNOPSIS</span></span>
<span data-ttu-id="5436b-103">移除網路虛擬裝置資源。</span><span class="sxs-lookup"><span data-stu-id="5436b-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="5436b-104">語法</span><span class="sxs-lookup"><span data-stu-id="5436b-104">SYNTAX</span></span>

### <span data-ttu-id="5436b-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5436b-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5436b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5436b-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5436b-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5436b-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5436b-108">描述</span><span class="sxs-lookup"><span data-stu-id="5436b-108">DESCRIPTION</span></span>
<span data-ttu-id="5436b-109">命令Remove-AzNetworkVirtualAppliance網路虛擬裝置資源。</span><span class="sxs-lookup"><span data-stu-id="5436b-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="5436b-110">例子</span><span class="sxs-lookup"><span data-stu-id="5436b-110">EXAMPLES</span></span>

### <span data-ttu-id="5436b-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="5436b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="5436b-112">刪除網路虛擬裝置資源。</span><span class="sxs-lookup"><span data-stu-id="5436b-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="5436b-113">參數</span><span class="sxs-lookup"><span data-stu-id="5436b-113">PARAMETERS</span></span>

### <span data-ttu-id="5436b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5436b-114">-AsJob</span></span>
<span data-ttu-id="5436b-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5436b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5436b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5436b-116">-DefaultProfile</span></span>
<span data-ttu-id="5436b-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5436b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5436b-118">-強制</span><span class="sxs-lookup"><span data-stu-id="5436b-118">-Force</span></span>
<span data-ttu-id="5436b-119">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="5436b-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5436b-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="5436b-120">-Name</span></span>
<span data-ttu-id="5436b-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="5436b-121">The resource name.</span></span>

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

### <span data-ttu-id="5436b-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="5436b-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="5436b-123">資源物件。</span><span class="sxs-lookup"><span data-stu-id="5436b-123">The resource object.</span></span>

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

### <span data-ttu-id="5436b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5436b-124">-PassThru</span></span>
<span data-ttu-id="5436b-125">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="5436b-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="5436b-126">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="5436b-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5436b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5436b-127">-ResourceGroupName</span></span>
<span data-ttu-id="5436b-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="5436b-128">The resource group name.</span></span>

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

### <span data-ttu-id="5436b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5436b-129">-ResourceId</span></span>
<span data-ttu-id="5436b-130">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5436b-130">The Resource Id.</span></span>

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

### <span data-ttu-id="5436b-131">-確認</span><span class="sxs-lookup"><span data-stu-id="5436b-131">-Confirm</span></span>
<span data-ttu-id="5436b-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5436b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5436b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5436b-133">-WhatIf</span></span>
<span data-ttu-id="5436b-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5436b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5436b-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5436b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5436b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5436b-136">CommonParameters</span></span>
<span data-ttu-id="5436b-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5436b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5436b-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5436b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5436b-139">輸入</span><span class="sxs-lookup"><span data-stu-id="5436b-139">INPUTS</span></span>

### <span data-ttu-id="5436b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5436b-140">System.String</span></span>

### <span data-ttu-id="5436b-141">Microsoft.Azure.Commands.Network.models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="5436b-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="5436b-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5436b-142">OUTPUTS</span></span>

### <span data-ttu-id="5436b-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5436b-143">System.Boolean</span></span>

## <span data-ttu-id="5436b-144">筆記</span><span class="sxs-lookup"><span data-stu-id="5436b-144">NOTES</span></span>

## <span data-ttu-id="5436b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="5436b-145">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
ms.openlocfilehash: bfe1c586d85a44460b1adbb84942be9b556973dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280912"
---
# <span data-ttu-id="e22bf-101">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e22bf-101">Remove-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="e22bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e22bf-102">SYNOPSIS</span></span>
<span data-ttu-id="e22bf-103">移除虛擬網路攻絲。</span><span class="sxs-lookup"><span data-stu-id="e22bf-103">Removes a virtual network tap.</span></span>

## <span data-ttu-id="e22bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="e22bf-104">SYNTAX</span></span>

### <span data-ttu-id="e22bf-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e22bf-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e22bf-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e22bf-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e22bf-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e22bf-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e22bf-108">說明</span><span class="sxs-lookup"><span data-stu-id="e22bf-108">DESCRIPTION</span></span>
<span data-ttu-id="e22bf-109">**AzVirtualNetworkTap** Cmdlet 會移除 Azure 虛擬網路分流。</span><span class="sxs-lookup"><span data-stu-id="e22bf-109">The **Remove-AzVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="e22bf-110">示例</span><span class="sxs-lookup"><span data-stu-id="e22bf-110">EXAMPLES</span></span>

### <span data-ttu-id="e22bf-111">範例1：移除虛擬網路攻絲</span><span class="sxs-lookup"><span data-stu-id="e22bf-111">Example 1: Remove a virtual network tap</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="e22bf-112">這個命令會移除資源群組 ResourceGroup1 中的 VirtualNetworkTap1。</span><span class="sxs-lookup"><span data-stu-id="e22bf-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="e22bf-113">由於不使用 *Force* 參數，系統會提示使用者確認此動作。</span><span class="sxs-lookup"><span data-stu-id="e22bf-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="e22bf-114">參數</span><span class="sxs-lookup"><span data-stu-id="e22bf-114">PARAMETERS</span></span>

### <span data-ttu-id="e22bf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e22bf-115">-AsJob</span></span>
<span data-ttu-id="e22bf-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e22bf-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e22bf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e22bf-117">-DefaultProfile</span></span>
<span data-ttu-id="e22bf-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e22bf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e22bf-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e22bf-119">-Force</span></span>
<span data-ttu-id="e22bf-120">如果您想要刪除資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="e22bf-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="e22bf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e22bf-121">-InputObject</span></span>
<span data-ttu-id="e22bf-122">VirtualNetworkTap 資源的參照</span><span class="sxs-lookup"><span data-stu-id="e22bf-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e22bf-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="e22bf-123">-Name</span></span>
<span data-ttu-id="e22bf-124">攻絲的名稱。</span><span class="sxs-lookup"><span data-stu-id="e22bf-124">The name of the tap.</span></span>

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

### <span data-ttu-id="e22bf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e22bf-125">-PassThru</span></span>
<span data-ttu-id="e22bf-126">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e22bf-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e22bf-127">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e22bf-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e22bf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e22bf-128">-ResourceGroupName</span></span>
<span data-ttu-id="e22bf-129">虛擬網路的 [資源] 群組名稱。</span><span class="sxs-lookup"><span data-stu-id="e22bf-129">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="e22bf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e22bf-130">-ResourceId</span></span>
<span data-ttu-id="e22bf-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="e22bf-131">VirtualNetworkTap resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e22bf-132">-確認</span><span class="sxs-lookup"><span data-stu-id="e22bf-132">-Confirm</span></span>
<span data-ttu-id="e22bf-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e22bf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e22bf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e22bf-134">-WhatIf</span></span>
<span data-ttu-id="e22bf-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e22bf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e22bf-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e22bf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e22bf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e22bf-137">CommonParameters</span></span>
<span data-ttu-id="e22bf-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e22bf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e22bf-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e22bf-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e22bf-140">輸入</span><span class="sxs-lookup"><span data-stu-id="e22bf-140">INPUTS</span></span>

### <span data-ttu-id="e22bf-141">System.object</span><span class="sxs-lookup"><span data-stu-id="e22bf-141">System.String</span></span>

### <span data-ttu-id="e22bf-142">PSVirtualNetworkTap 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e22bf-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="e22bf-143">輸出</span><span class="sxs-lookup"><span data-stu-id="e22bf-143">OUTPUTS</span></span>

### <span data-ttu-id="e22bf-144">System.object</span><span class="sxs-lookup"><span data-stu-id="e22bf-144">System.Boolean</span></span>

## <span data-ttu-id="e22bf-145">筆記</span><span class="sxs-lookup"><span data-stu-id="e22bf-145">NOTES</span></span>

## <span data-ttu-id="e22bf-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="e22bf-146">RELATED LINKS</span></span>

[<span data-ttu-id="e22bf-147">AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e22bf-147">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="e22bf-148">新-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e22bf-148">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="e22bf-149">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e22bf-149">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)

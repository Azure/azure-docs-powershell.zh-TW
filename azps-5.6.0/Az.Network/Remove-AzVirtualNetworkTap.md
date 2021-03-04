---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
ms.openlocfilehash: a0188236a5ce0b4da29a61b38d7c1889bc909968
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915945"
---
# <span data-ttu-id="61be2-101">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="61be2-101">Remove-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="61be2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="61be2-102">SYNOPSIS</span></span>
<span data-ttu-id="61be2-103">移除虛擬網路點一下。</span><span class="sxs-lookup"><span data-stu-id="61be2-103">Removes a virtual network tap.</span></span>

## <span data-ttu-id="61be2-104">語法</span><span class="sxs-lookup"><span data-stu-id="61be2-104">SYNTAX</span></span>

### <span data-ttu-id="61be2-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="61be2-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61be2-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61be2-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61be2-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61be2-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61be2-108">描述</span><span class="sxs-lookup"><span data-stu-id="61be2-108">DESCRIPTION</span></span>
<span data-ttu-id="61be2-109">**Remove-AzVirtualNetworkTap** Cmdlet 會移除 Azure 虛擬網路點一下。</span><span class="sxs-lookup"><span data-stu-id="61be2-109">The **Remove-AzVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="61be2-110">例子</span><span class="sxs-lookup"><span data-stu-id="61be2-110">EXAMPLES</span></span>

### <span data-ttu-id="61be2-111">範例 1：移除虛擬網路點一下</span><span class="sxs-lookup"><span data-stu-id="61be2-111">Example 1: Remove a virtual network tap</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="61be2-112">此命令會移除資源群組 ResourceGroup1 中的 VirtualNetworkTap1。</span><span class="sxs-lookup"><span data-stu-id="61be2-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="61be2-113">由於 *不會使用 Force* 參數，因此系統會提示使用者確認此動作。</span><span class="sxs-lookup"><span data-stu-id="61be2-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="61be2-114">參數</span><span class="sxs-lookup"><span data-stu-id="61be2-114">PARAMETERS</span></span>

### <span data-ttu-id="61be2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61be2-115">-AsJob</span></span>
<span data-ttu-id="61be2-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="61be2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61be2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61be2-117">-DefaultProfile</span></span>
<span data-ttu-id="61be2-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="61be2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61be2-119">-強制</span><span class="sxs-lookup"><span data-stu-id="61be2-119">-Force</span></span>
<span data-ttu-id="61be2-120">如果您要刪除資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="61be2-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="61be2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61be2-121">-InputObject</span></span>
<span data-ttu-id="61be2-122">VirtualNetworkTap 資源的參照</span><span class="sxs-lookup"><span data-stu-id="61be2-122">Reference to VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="61be2-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="61be2-123">-Name</span></span>
<span data-ttu-id="61be2-124">點一下的名稱。</span><span class="sxs-lookup"><span data-stu-id="61be2-124">The name of the tap.</span></span>

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

### <span data-ttu-id="61be2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61be2-125">-PassThru</span></span>
<span data-ttu-id="61be2-126">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="61be2-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="61be2-127">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="61be2-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="61be2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61be2-128">-ResourceGroupName</span></span>
<span data-ttu-id="61be2-129">點一下虛擬網路的資源組名。</span><span class="sxs-lookup"><span data-stu-id="61be2-129">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="61be2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61be2-130">-ResourceId</span></span>
<span data-ttu-id="61be2-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="61be2-131">VirtualNetworkTap resourceId</span></span>

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

### <span data-ttu-id="61be2-132">-確認</span><span class="sxs-lookup"><span data-stu-id="61be2-132">-Confirm</span></span>
<span data-ttu-id="61be2-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="61be2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61be2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61be2-134">-WhatIf</span></span>
<span data-ttu-id="61be2-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61be2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61be2-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61be2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61be2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61be2-137">CommonParameters</span></span>
<span data-ttu-id="61be2-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="61be2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61be2-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="61be2-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61be2-140">輸入</span><span class="sxs-lookup"><span data-stu-id="61be2-140">INPUTS</span></span>

### <span data-ttu-id="61be2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="61be2-141">System.String</span></span>

### <span data-ttu-id="61be2-142">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="61be2-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="61be2-143">輸出</span><span class="sxs-lookup"><span data-stu-id="61be2-143">OUTPUTS</span></span>

### <span data-ttu-id="61be2-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="61be2-144">System.Boolean</span></span>

## <span data-ttu-id="61be2-145">筆記</span><span class="sxs-lookup"><span data-stu-id="61be2-145">NOTES</span></span>

## <span data-ttu-id="61be2-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="61be2-146">RELATED LINKS</span></span>

[<span data-ttu-id="61be2-147">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="61be2-147">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="61be2-148">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="61be2-148">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="61be2-149">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="61be2-149">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: ae05b4afd18bb1cdb55c8c1b748068f1f6c5191f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903993"
---
# <span data-ttu-id="29fa5-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="29fa5-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="29fa5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="29fa5-102">SYNOPSIS</span></span>
<span data-ttu-id="29fa5-103">移除 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="29fa5-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="29fa5-104">語法</span><span class="sxs-lookup"><span data-stu-id="29fa5-104">SYNTAX</span></span>

### <span data-ttu-id="29fa5-105">ByVirtualWanName (預設) </span><span class="sxs-lookup"><span data-stu-id="29fa5-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29fa5-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="29fa5-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29fa5-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="29fa5-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29fa5-108">描述</span><span class="sxs-lookup"><span data-stu-id="29fa5-108">DESCRIPTION</span></span>
<span data-ttu-id="29fa5-109">移除 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="29fa5-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="29fa5-110">例子</span><span class="sxs-lookup"><span data-stu-id="29fa5-110">EXAMPLES</span></span>

### <span data-ttu-id="29fa5-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="29fa5-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="29fa5-112">此範例在資源群組中建立虛擬 WAN，然後立即刪除。</span><span class="sxs-lookup"><span data-stu-id="29fa5-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="29fa5-113">若要隱藏刪除虛擬 WAN 時提示，請使用 -Force 旗標。</span><span class="sxs-lookup"><span data-stu-id="29fa5-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="29fa5-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="29fa5-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="29fa5-115">此範例在資源群組中建立虛擬 WAN，然後立即刪除。</span><span class="sxs-lookup"><span data-stu-id="29fa5-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="29fa5-116">此刪除會使用 New-AzVirtual Wan 所返回的虛擬 wan 物件執行。</span><span class="sxs-lookup"><span data-stu-id="29fa5-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="29fa5-117">若要隱藏刪除虛擬 WAN 時提示，請使用 -Force 旗標。</span><span class="sxs-lookup"><span data-stu-id="29fa5-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="29fa5-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="29fa5-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="29fa5-119">此範例在資源群組中建立虛擬 WAN，然後立即刪除。</span><span class="sxs-lookup"><span data-stu-id="29fa5-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="29fa5-120">此刪除會使用 New-AzVirtual Wan 所返回的虛擬 wan 資源識別碼進行。</span><span class="sxs-lookup"><span data-stu-id="29fa5-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="29fa5-121">若要隱藏刪除虛擬 WAN 時提示，請使用 -Force 旗標。</span><span class="sxs-lookup"><span data-stu-id="29fa5-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="29fa5-122">參數</span><span class="sxs-lookup"><span data-stu-id="29fa5-122">PARAMETERS</span></span>

### <span data-ttu-id="29fa5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29fa5-123">-DefaultProfile</span></span>
<span data-ttu-id="29fa5-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="29fa5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29fa5-125">-強制</span><span class="sxs-lookup"><span data-stu-id="29fa5-125">-Force</span></span>
<span data-ttu-id="29fa5-126">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="29fa5-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="29fa5-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29fa5-127">-InputObject</span></span>
<span data-ttu-id="29fa5-128">要刪除的虛擬 wan 物件。</span><span class="sxs-lookup"><span data-stu-id="29fa5-128">The virtual wan object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29fa5-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="29fa5-129">-Name</span></span>
<span data-ttu-id="29fa5-130">虛擬 wan 名稱。</span><span class="sxs-lookup"><span data-stu-id="29fa5-130">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29fa5-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29fa5-131">-PassThru</span></span>
<span data-ttu-id="29fa5-132">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="29fa5-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="29fa5-133">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="29fa5-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="29fa5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29fa5-134">-ResourceGroupName</span></span>
<span data-ttu-id="29fa5-135">資源組名。</span><span class="sxs-lookup"><span data-stu-id="29fa5-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29fa5-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29fa5-136">-ResourceId</span></span>
<span data-ttu-id="29fa5-137">要刪除虛擬 Wan 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="29fa5-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29fa5-138">-確認</span><span class="sxs-lookup"><span data-stu-id="29fa5-138">-Confirm</span></span>
<span data-ttu-id="29fa5-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="29fa5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29fa5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29fa5-140">-WhatIf</span></span>
<span data-ttu-id="29fa5-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29fa5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29fa5-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29fa5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29fa5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29fa5-143">CommonParameters</span></span>
<span data-ttu-id="29fa5-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="29fa5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29fa5-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="29fa5-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29fa5-146">輸入</span><span class="sxs-lookup"><span data-stu-id="29fa5-146">INPUTS</span></span>

### <span data-ttu-id="29fa5-147">Microsoft.Azure.Commands.Network.models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="29fa5-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="29fa5-148">System.String</span><span class="sxs-lookup"><span data-stu-id="29fa5-148">System.String</span></span>

## <span data-ttu-id="29fa5-149">輸出</span><span class="sxs-lookup"><span data-stu-id="29fa5-149">OUTPUTS</span></span>

### <span data-ttu-id="29fa5-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="29fa5-150">System.Boolean</span></span>

## <span data-ttu-id="29fa5-151">筆記</span><span class="sxs-lookup"><span data-stu-id="29fa5-151">NOTES</span></span>

## <span data-ttu-id="29fa5-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="29fa5-152">RELATED LINKS</span></span>

[<span data-ttu-id="29fa5-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="29fa5-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="29fa5-154">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="29fa5-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="29fa5-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="29fa5-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)

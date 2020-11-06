---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: d1ec777d6574aa34a6b19fa7cdc94d9c349dbc48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621539"
---
# <span data-ttu-id="26340-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="26340-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="26340-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26340-102">SYNOPSIS</span></span>
<span data-ttu-id="26340-103">移除 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="26340-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="26340-104">句法</span><span class="sxs-lookup"><span data-stu-id="26340-104">SYNTAX</span></span>

### <span data-ttu-id="26340-105">ByVirtualWanName (預設) </span><span class="sxs-lookup"><span data-stu-id="26340-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26340-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="26340-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26340-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="26340-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26340-108">說明</span><span class="sxs-lookup"><span data-stu-id="26340-108">DESCRIPTION</span></span>
<span data-ttu-id="26340-109">移除 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="26340-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="26340-110">示例</span><span class="sxs-lookup"><span data-stu-id="26340-110">EXAMPLES</span></span>

### <span data-ttu-id="26340-111">範例1</span><span class="sxs-lookup"><span data-stu-id="26340-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="26340-112">這個範例會在資源群組中建立一個虛擬 WAN，然後立即將它刪除。</span><span class="sxs-lookup"><span data-stu-id="26340-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="26340-113">若要在刪除虛擬 WAN 時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="26340-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="26340-114">範例2</span><span class="sxs-lookup"><span data-stu-id="26340-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="26340-115">這個範例會在資源群組中建立一個虛擬 WAN，然後立即將它刪除。</span><span class="sxs-lookup"><span data-stu-id="26340-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="26340-116">這個刪除會在使用由新的 AzVirtualWan 所傳回的虛擬 wan 物件時發生。</span><span class="sxs-lookup"><span data-stu-id="26340-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="26340-117">若要在刪除虛擬 WAN 時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="26340-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="26340-118">範例3</span><span class="sxs-lookup"><span data-stu-id="26340-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="26340-119">這個範例會在資源群組中建立一個虛擬 WAN，然後立即將它刪除。</span><span class="sxs-lookup"><span data-stu-id="26340-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="26340-120">這個刪除會在使用由新的 AzVirtualWan 傳回的虛擬 wan 資源識別碼時發生。</span><span class="sxs-lookup"><span data-stu-id="26340-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="26340-121">若要在刪除虛擬 WAN 時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="26340-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="26340-122">參數</span><span class="sxs-lookup"><span data-stu-id="26340-122">PARAMETERS</span></span>

### <span data-ttu-id="26340-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26340-123">-DefaultProfile</span></span>
<span data-ttu-id="26340-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26340-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26340-125">-Force</span><span class="sxs-lookup"><span data-stu-id="26340-125">-Force</span></span>
<span data-ttu-id="26340-126">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="26340-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="26340-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26340-127">-InputObject</span></span>
<span data-ttu-id="26340-128">要刪除的虛擬 wan 物件。</span><span class="sxs-lookup"><span data-stu-id="26340-128">The virtual wan object to be deleted.</span></span>

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

### <span data-ttu-id="26340-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="26340-129">-Name</span></span>
<span data-ttu-id="26340-130">虛擬 wan 名稱。</span><span class="sxs-lookup"><span data-stu-id="26340-130">The virtual wan name.</span></span>

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

### <span data-ttu-id="26340-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26340-131">-PassThru</span></span>
<span data-ttu-id="26340-132">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="26340-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="26340-133">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="26340-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="26340-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26340-134">-ResourceGroupName</span></span>
<span data-ttu-id="26340-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="26340-135">The resource group name.</span></span>

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

### <span data-ttu-id="26340-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26340-136">-ResourceId</span></span>
<span data-ttu-id="26340-137">要刪除之虛擬 wan 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="26340-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

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

### <span data-ttu-id="26340-138">-確認</span><span class="sxs-lookup"><span data-stu-id="26340-138">-Confirm</span></span>
<span data-ttu-id="26340-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26340-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26340-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26340-140">-WhatIf</span></span>
<span data-ttu-id="26340-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26340-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26340-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26340-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26340-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26340-143">CommonParameters</span></span>
<span data-ttu-id="26340-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26340-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26340-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26340-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26340-146">輸入</span><span class="sxs-lookup"><span data-stu-id="26340-146">INPUTS</span></span>

### <span data-ttu-id="26340-147">PSVirtualWan 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="26340-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="26340-148">System.object</span><span class="sxs-lookup"><span data-stu-id="26340-148">System.String</span></span>

## <span data-ttu-id="26340-149">輸出</span><span class="sxs-lookup"><span data-stu-id="26340-149">OUTPUTS</span></span>

### <span data-ttu-id="26340-150">System.object</span><span class="sxs-lookup"><span data-stu-id="26340-150">System.Boolean</span></span>

## <span data-ttu-id="26340-151">筆記</span><span class="sxs-lookup"><span data-stu-id="26340-151">NOTES</span></span>

## <span data-ttu-id="26340-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="26340-152">RELATED LINKS</span></span>

[<span data-ttu-id="26340-153">AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="26340-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="26340-154">新-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="26340-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="26340-155">更新-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="26340-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
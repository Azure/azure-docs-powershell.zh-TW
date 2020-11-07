---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: 802a87b4ba420fb84036756185c68a6250e70920
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959905"
---
# <span data-ttu-id="8893d-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8893d-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="8893d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8893d-102">SYNOPSIS</span></span>
<span data-ttu-id="8893d-103">移除 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="8893d-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="8893d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8893d-104">SYNTAX</span></span>

### <span data-ttu-id="8893d-105">ByVirtualWanName (預設) </span><span class="sxs-lookup"><span data-stu-id="8893d-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8893d-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="8893d-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8893d-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="8893d-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8893d-108">說明</span><span class="sxs-lookup"><span data-stu-id="8893d-108">DESCRIPTION</span></span>
<span data-ttu-id="8893d-109">移除 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="8893d-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="8893d-110">示例</span><span class="sxs-lookup"><span data-stu-id="8893d-110">EXAMPLES</span></span>

### <span data-ttu-id="8893d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8893d-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="8893d-112">這個範例會在資源群組中建立一個虛擬 WAN，然後立即將它刪除。</span><span class="sxs-lookup"><span data-stu-id="8893d-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="8893d-113">若要在刪除虛擬 WAN 時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="8893d-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="8893d-114">範例2</span><span class="sxs-lookup"><span data-stu-id="8893d-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="8893d-115">這個範例會在資源群組中建立一個虛擬 WAN，然後立即將它刪除。</span><span class="sxs-lookup"><span data-stu-id="8893d-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="8893d-116">這個刪除會在使用由新的 AzVirtualWan 所傳回的虛擬 wan 物件時發生。</span><span class="sxs-lookup"><span data-stu-id="8893d-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="8893d-117">若要在刪除虛擬 WAN 時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="8893d-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="8893d-118">範例3</span><span class="sxs-lookup"><span data-stu-id="8893d-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="8893d-119">這個範例會在資源群組中建立一個虛擬 WAN，然後立即將它刪除。</span><span class="sxs-lookup"><span data-stu-id="8893d-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="8893d-120">這個刪除會在使用由新的 AzVirtualWan 傳回的虛擬 wan 資源識別碼時發生。</span><span class="sxs-lookup"><span data-stu-id="8893d-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="8893d-121">若要在刪除虛擬 WAN 時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="8893d-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="8893d-122">參數</span><span class="sxs-lookup"><span data-stu-id="8893d-122">PARAMETERS</span></span>

### <span data-ttu-id="8893d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8893d-123">-DefaultProfile</span></span>
<span data-ttu-id="8893d-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8893d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8893d-125">-Force</span><span class="sxs-lookup"><span data-stu-id="8893d-125">-Force</span></span>
<span data-ttu-id="8893d-126">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="8893d-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8893d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8893d-127">-InputObject</span></span>
<span data-ttu-id="8893d-128">要刪除的虛擬 wan 物件。</span><span class="sxs-lookup"><span data-stu-id="8893d-128">The virtual wan object to be deleted.</span></span>

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

### <span data-ttu-id="8893d-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="8893d-129">-Name</span></span>
<span data-ttu-id="8893d-130">虛擬 wan 名稱。</span><span class="sxs-lookup"><span data-stu-id="8893d-130">The virtual wan name.</span></span>

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

### <span data-ttu-id="8893d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8893d-131">-PassThru</span></span>
<span data-ttu-id="8893d-132">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="8893d-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8893d-133">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8893d-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8893d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8893d-134">-ResourceGroupName</span></span>
<span data-ttu-id="8893d-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8893d-135">The resource group name.</span></span>

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

### <span data-ttu-id="8893d-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8893d-136">-ResourceId</span></span>
<span data-ttu-id="8893d-137">要刪除之虛擬 wan 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8893d-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

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

### <span data-ttu-id="8893d-138">-確認</span><span class="sxs-lookup"><span data-stu-id="8893d-138">-Confirm</span></span>
<span data-ttu-id="8893d-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8893d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8893d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8893d-140">-WhatIf</span></span>
<span data-ttu-id="8893d-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8893d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8893d-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8893d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8893d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8893d-143">CommonParameters</span></span>
<span data-ttu-id="8893d-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8893d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8893d-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8893d-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8893d-146">輸入</span><span class="sxs-lookup"><span data-stu-id="8893d-146">INPUTS</span></span>

### <span data-ttu-id="8893d-147">PSVirtualWan 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8893d-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="8893d-148">System.object</span><span class="sxs-lookup"><span data-stu-id="8893d-148">System.String</span></span>

## <span data-ttu-id="8893d-149">輸出</span><span class="sxs-lookup"><span data-stu-id="8893d-149">OUTPUTS</span></span>

### <span data-ttu-id="8893d-150">System.object</span><span class="sxs-lookup"><span data-stu-id="8893d-150">System.Boolean</span></span>

## <span data-ttu-id="8893d-151">筆記</span><span class="sxs-lookup"><span data-stu-id="8893d-151">NOTES</span></span>

## <span data-ttu-id="8893d-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="8893d-152">RELATED LINKS</span></span>

[<span data-ttu-id="8893d-153">AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8893d-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="8893d-154">新-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8893d-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="8893d-155">更新-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8893d-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)

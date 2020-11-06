---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualWan.md
ms.openlocfilehash: 1ff9eb4307c4419dd303d74f7528a8ee0d50bdf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448306"
---
# <span data-ttu-id="2bee2-101">Remove-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="2bee2-101">Remove-AzureRmVirtualWan</span></span>

## <span data-ttu-id="2bee2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2bee2-102">SYNOPSIS</span></span>
<span data-ttu-id="2bee2-103">移除 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="2bee2-103">Removes an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bee2-104">句法</span><span class="sxs-lookup"><span data-stu-id="2bee2-104">SYNTAX</span></span>

### <span data-ttu-id="2bee2-105">ByVirtualWanName (預設) </span><span class="sxs-lookup"><span data-stu-id="2bee2-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bee2-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="2bee2-106">ByVirtualWanObject</span></span>
```
Remove-AzureRmVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bee2-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="2bee2-107">ByVirtualWanResourceId</span></span>
```
Remove-AzureRmVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bee2-108">說明</span><span class="sxs-lookup"><span data-stu-id="2bee2-108">DESCRIPTION</span></span>
<span data-ttu-id="2bee2-109">移除 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="2bee2-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="2bee2-110">示例</span><span class="sxs-lookup"><span data-stu-id="2bee2-110">EXAMPLES</span></span>

### <span data-ttu-id="2bee2-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2bee2-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="2bee2-112">這個範例會在資源群組中建立一個虛擬 WAN，然後立即將它刪除。</span><span class="sxs-lookup"><span data-stu-id="2bee2-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="2bee2-113">若要在刪除虛擬 WAN 時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="2bee2-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="2bee2-114">範例2</span><span class="sxs-lookup"><span data-stu-id="2bee2-114">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzureRmVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="2bee2-115">這個範例會在資源群組中建立一個虛擬 WAN，然後立即將它刪除。</span><span class="sxs-lookup"><span data-stu-id="2bee2-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="2bee2-116">這個刪除會在使用由新的 AzureRmVirtualWan 所傳回的虛擬 wan 物件時發生。</span><span class="sxs-lookup"><span data-stu-id="2bee2-116">This deletion happens using the virtual wan object returned by New-AzureRmVirtualWan.</span></span>
<span data-ttu-id="2bee2-117">若要在刪除虛擬 WAN 時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="2bee2-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="2bee2-118">範例3</span><span class="sxs-lookup"><span data-stu-id="2bee2-118">Example 3</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzureRmVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzureRmVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="2bee2-119">這個範例會在資源群組中建立一個虛擬 WAN，然後立即將它刪除。</span><span class="sxs-lookup"><span data-stu-id="2bee2-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="2bee2-120">這個刪除會在使用由新的 AzureRmVirtualWan 傳回的虛擬 wan 資源識別碼時發生。</span><span class="sxs-lookup"><span data-stu-id="2bee2-120">This deletion happens using the virtual wan resource id returned by New-AzureRmVirtualWan.</span></span>
<span data-ttu-id="2bee2-121">若要在刪除虛擬 WAN 時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="2bee2-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="2bee2-122">參數</span><span class="sxs-lookup"><span data-stu-id="2bee2-122">PARAMETERS</span></span>

### <span data-ttu-id="2bee2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bee2-123">-DefaultProfile</span></span>
<span data-ttu-id="2bee2-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2bee2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bee2-125">-Force</span><span class="sxs-lookup"><span data-stu-id="2bee2-125">-Force</span></span>
<span data-ttu-id="2bee2-126">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="2bee2-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2bee2-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bee2-127">-InputObject</span></span>
<span data-ttu-id="2bee2-128">要刪除的虛擬 wan 物件。</span><span class="sxs-lookup"><span data-stu-id="2bee2-128">The virtual wan object to be deleted.</span></span>

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

### <span data-ttu-id="2bee2-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="2bee2-129">-Name</span></span>
<span data-ttu-id="2bee2-130">虛擬 wan 名稱。</span><span class="sxs-lookup"><span data-stu-id="2bee2-130">The virtual wan name.</span></span>

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

### <span data-ttu-id="2bee2-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2bee2-131">-PassThru</span></span>
<span data-ttu-id="2bee2-132">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="2bee2-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2bee2-133">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="2bee2-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2bee2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bee2-134">-ResourceGroupName</span></span>
<span data-ttu-id="2bee2-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bee2-135">The resource group name.</span></span>

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

### <span data-ttu-id="2bee2-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bee2-136">-ResourceId</span></span>
<span data-ttu-id="2bee2-137">要刪除之虛擬 wan 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2bee2-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

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

### <span data-ttu-id="2bee2-138">-確認</span><span class="sxs-lookup"><span data-stu-id="2bee2-138">-Confirm</span></span>
<span data-ttu-id="2bee2-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2bee2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bee2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bee2-140">-WhatIf</span></span>
<span data-ttu-id="2bee2-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2bee2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bee2-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2bee2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bee2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bee2-143">CommonParameters</span></span>
<span data-ttu-id="2bee2-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2bee2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bee2-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2bee2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bee2-146">輸入</span><span class="sxs-lookup"><span data-stu-id="2bee2-146">INPUTS</span></span>

### <span data-ttu-id="2bee2-147">PSVirtualWan 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2bee2-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="2bee2-148">System.object</span><span class="sxs-lookup"><span data-stu-id="2bee2-148">System.String</span></span>

## <span data-ttu-id="2bee2-149">輸出</span><span class="sxs-lookup"><span data-stu-id="2bee2-149">OUTPUTS</span></span>

### <span data-ttu-id="2bee2-150">System.object</span><span class="sxs-lookup"><span data-stu-id="2bee2-150">System.Boolean</span></span>

## <span data-ttu-id="2bee2-151">筆記</span><span class="sxs-lookup"><span data-stu-id="2bee2-151">NOTES</span></span>

## <span data-ttu-id="2bee2-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="2bee2-152">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: 116cffabc942572db48d6f86b469a954bccbc1c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282051"
---
# <span data-ttu-id="86198-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="86198-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="86198-102">摘要</span><span class="sxs-lookup"><span data-stu-id="86198-102">SYNOPSIS</span></span>
<span data-ttu-id="86198-103">移除 Azure VirtualHub 資源。</span><span class="sxs-lookup"><span data-stu-id="86198-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="86198-104">句法</span><span class="sxs-lookup"><span data-stu-id="86198-104">SYNTAX</span></span>

### <span data-ttu-id="86198-105">ByVirtualHubName (預設) </span><span class="sxs-lookup"><span data-stu-id="86198-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86198-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="86198-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86198-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="86198-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86198-108">說明</span><span class="sxs-lookup"><span data-stu-id="86198-108">DESCRIPTION</span></span>
<span data-ttu-id="86198-109">移除 Azure VirtualHub 資源。</span><span class="sxs-lookup"><span data-stu-id="86198-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="86198-110">示例</span><span class="sxs-lookup"><span data-stu-id="86198-110">EXAMPLES</span></span>

### <span data-ttu-id="86198-111">範例1</span><span class="sxs-lookup"><span data-stu-id="86198-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="86198-112">上述將會建立一個資源群組 "testRG"，也就是 Azure 中該資源群組的 [西部我們] 中的虛擬 WAN 和虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="86198-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="86198-113">虛擬中樞會將位址空間 "10.0.1.0/24"。</span><span class="sxs-lookup"><span data-stu-id="86198-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="86198-114">然後它會使用其 ResourceGroupName 和 CoNtext.resourcename 來刪除虛擬中心。</span><span class="sxs-lookup"><span data-stu-id="86198-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="86198-115">範例2</span><span class="sxs-lookup"><span data-stu-id="86198-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="86198-116">上述將會建立一個資源群組 "testRG"，也就是 Azure 中該資源群組的 [西部我們] 中的虛擬 WAN 和虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="86198-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="86198-117">虛擬中樞會將位址空間 "10.0.1.0/24"。</span><span class="sxs-lookup"><span data-stu-id="86198-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="86198-118">接著，它會使用輸入物件刪除虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="86198-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="86198-119">輸入物件的類型是 PSVirtualHub。</span><span class="sxs-lookup"><span data-stu-id="86198-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="86198-120">範例3</span><span class="sxs-lookup"><span data-stu-id="86198-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="86198-121">上述將會建立一個資源群組 "testRG"，也就是 Azure 中該資源群組的 [西部我們] 中的虛擬 WAN 和虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="86198-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="86198-122">虛擬中樞會將位址空間 "10.0.1.0/24"。</span><span class="sxs-lookup"><span data-stu-id="86198-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="86198-123">然後它會使用 [AzVirtualHub] 中的 [輸出]，來刪除使用 powershell 管道的虛擬中心。</span><span class="sxs-lookup"><span data-stu-id="86198-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="86198-124">參數</span><span class="sxs-lookup"><span data-stu-id="86198-124">PARAMETERS</span></span>

### <span data-ttu-id="86198-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86198-125">-AsJob</span></span>
<span data-ttu-id="86198-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="86198-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86198-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86198-127">-DefaultProfile</span></span>
<span data-ttu-id="86198-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="86198-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86198-129">-Force</span><span class="sxs-lookup"><span data-stu-id="86198-129">-Force</span></span>
<span data-ttu-id="86198-130">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="86198-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="86198-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86198-131">-InputObject</span></span>
<span data-ttu-id="86198-132">要修改的虛擬中心物件。</span><span class="sxs-lookup"><span data-stu-id="86198-132">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86198-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="86198-133">-Name</span></span>
<span data-ttu-id="86198-134">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="86198-134">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86198-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86198-135">-PassThru</span></span>
<span data-ttu-id="86198-136">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="86198-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="86198-137">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="86198-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="86198-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86198-138">-ResourceGroupName</span></span>
<span data-ttu-id="86198-139">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="86198-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86198-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86198-140">-ResourceId</span></span>
<span data-ttu-id="86198-141">要修改之虛擬中心的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="86198-141">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86198-142">-確認</span><span class="sxs-lookup"><span data-stu-id="86198-142">-Confirm</span></span>
<span data-ttu-id="86198-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="86198-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86198-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86198-144">-WhatIf</span></span>
<span data-ttu-id="86198-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="86198-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86198-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="86198-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86198-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86198-147">CommonParameters</span></span>
<span data-ttu-id="86198-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="86198-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86198-149">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="86198-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86198-150">輸入</span><span class="sxs-lookup"><span data-stu-id="86198-150">INPUTS</span></span>

### <span data-ttu-id="86198-151">System.object</span><span class="sxs-lookup"><span data-stu-id="86198-151">System.String</span></span>

### <span data-ttu-id="86198-152">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="86198-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="86198-153">輸出</span><span class="sxs-lookup"><span data-stu-id="86198-153">OUTPUTS</span></span>

### <span data-ttu-id="86198-154">System.object</span><span class="sxs-lookup"><span data-stu-id="86198-154">System.Boolean</span></span>

## <span data-ttu-id="86198-155">筆記</span><span class="sxs-lookup"><span data-stu-id="86198-155">NOTES</span></span>

## <span data-ttu-id="86198-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="86198-156">RELATED LINKS</span></span>

[<span data-ttu-id="86198-157">AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="86198-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="86198-158">新-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="86198-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="86198-159">更新-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="86198-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)

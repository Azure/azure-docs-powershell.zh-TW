---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
ms.openlocfilehash: d43595d3ad5b0d92546c9d4f13ad8f5dcc6087be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908817"
---
# <span data-ttu-id="40515-101">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="40515-101">Get-AzVirtualWan</span></span>

## <span data-ttu-id="40515-102">簡介</span><span class="sxs-lookup"><span data-stu-id="40515-102">SYNOPSIS</span></span>
<span data-ttu-id="40515-103">在資源群組或訂閱中，獲得虛擬 WAN 或所有虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="40515-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="40515-104">語法</span><span class="sxs-lookup"><span data-stu-id="40515-104">SYNTAX</span></span>

### <span data-ttu-id="40515-105">ListBySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="40515-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40515-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40515-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualWan [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40515-107">描述</span><span class="sxs-lookup"><span data-stu-id="40515-107">DESCRIPTION</span></span>
<span data-ttu-id="40515-108">在資源群組或訂閱中，獲得虛擬 WAN 或所有虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="40515-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="40515-109">例子</span><span class="sxs-lookup"><span data-stu-id="40515-109">EXAMPLES</span></span>

### <span data-ttu-id="40515-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="40515-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : myVirtualWAN
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="40515-111">此命令在資源群組 testRG 中，會獲得名為 myVirtual WAN 的虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="40515-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

### <span data-ttu-id="40515-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="40515-112">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualWan -Name test*

Name                       : test1
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test1
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded

Name                       : test2
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test2
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="40515-113">此命令會從「測試」開始獲得所有虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="40515-113">This command gets all Virtual WANs starting with "test".</span></span>

## <span data-ttu-id="40515-114">參數</span><span class="sxs-lookup"><span data-stu-id="40515-114">PARAMETERS</span></span>

### <span data-ttu-id="40515-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40515-115">-DefaultProfile</span></span>
<span data-ttu-id="40515-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="40515-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40515-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="40515-117">-Name</span></span>
<span data-ttu-id="40515-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="40515-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="40515-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40515-119">-ResourceGroupName</span></span>
<span data-ttu-id="40515-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="40515-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="40515-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40515-121">CommonParameters</span></span>
<span data-ttu-id="40515-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="40515-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40515-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40515-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40515-124">輸入</span><span class="sxs-lookup"><span data-stu-id="40515-124">INPUTS</span></span>

### <span data-ttu-id="40515-125">沒有</span><span class="sxs-lookup"><span data-stu-id="40515-125">None</span></span>

## <span data-ttu-id="40515-126">輸出</span><span class="sxs-lookup"><span data-stu-id="40515-126">OUTPUTS</span></span>

### <span data-ttu-id="40515-127">Microsoft.Azure.Commands.Network.models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="40515-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="40515-128">筆記</span><span class="sxs-lookup"><span data-stu-id="40515-128">NOTES</span></span>

## <span data-ttu-id="40515-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="40515-129">RELATED LINKS</span></span>

[<span data-ttu-id="40515-130">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="40515-130">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="40515-131">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="40515-131">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="40515-132">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="40515-132">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)

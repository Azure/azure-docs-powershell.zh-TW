---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: b4daa24f787633d2f18896910faed340a969a0f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913826"
---
# <span data-ttu-id="25acc-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="25acc-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="25acc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="25acc-102">SYNOPSIS</span></span>
<span data-ttu-id="25acc-103">獲得虛擬網路目前的使用量。</span><span class="sxs-lookup"><span data-stu-id="25acc-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="25acc-104">語法</span><span class="sxs-lookup"><span data-stu-id="25acc-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25acc-105">描述</span><span class="sxs-lookup"><span data-stu-id="25acc-105">DESCRIPTION</span></span>
<span data-ttu-id="25acc-106">**Get-AzVirtualNetworkUsageList** Cmdlet 會針對指定的虛擬網路取得每個子網使用量。</span><span class="sxs-lookup"><span data-stu-id="25acc-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="25acc-107">例子</span><span class="sxs-lookup"><span data-stu-id="25acc-107">EXAMPLES</span></span>

### <span data-ttu-id="25acc-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="25acc-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet
CurrentValue : 1
Limit        : 65531
Unit         : Count

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet11
CurrentValue : 0
Limit        : 251
Unit         : Count
```

<span data-ttu-id="25acc-109">針對使用方式測試虛擬網路，每個子網目前的使用量值進行計算。</span><span class="sxs-lookup"><span data-stu-id="25acc-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="25acc-110">參數</span><span class="sxs-lookup"><span data-stu-id="25acc-110">PARAMETERS</span></span>

### <span data-ttu-id="25acc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25acc-111">-DefaultProfile</span></span>
<span data-ttu-id="25acc-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="25acc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25acc-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="25acc-113">-Name</span></span>
<span data-ttu-id="25acc-114">指定要顯示其使用量的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="25acc-114">Specifies the name of the virtual network to show usages for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25acc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25acc-115">-ResourceGroupName</span></span>
<span data-ttu-id="25acc-116">指定虛擬網路所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="25acc-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25acc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25acc-117">CommonParameters</span></span>
<span data-ttu-id="25acc-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="25acc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25acc-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25acc-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25acc-120">輸入</span><span class="sxs-lookup"><span data-stu-id="25acc-120">INPUTS</span></span>

### <span data-ttu-id="25acc-121">System.String</span><span class="sxs-lookup"><span data-stu-id="25acc-121">System.String</span></span>

## <span data-ttu-id="25acc-122">輸出</span><span class="sxs-lookup"><span data-stu-id="25acc-122">OUTPUTS</span></span>

### <span data-ttu-id="25acc-123">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="25acc-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="25acc-124">筆記</span><span class="sxs-lookup"><span data-stu-id="25acc-124">NOTES</span></span>

## <span data-ttu-id="25acc-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="25acc-125">RELATED LINKS</span></span>

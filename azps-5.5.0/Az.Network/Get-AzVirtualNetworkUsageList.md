---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: 023eb245132a7b451fc6e30351db5751fb754cde
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131323"
---
# <span data-ttu-id="bc850-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="bc850-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="bc850-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc850-102">SYNOPSIS</span></span>
<span data-ttu-id="bc850-103">取得虛擬網路的目前使用量。</span><span class="sxs-lookup"><span data-stu-id="bc850-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="bc850-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc850-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc850-105">說明</span><span class="sxs-lookup"><span data-stu-id="bc850-105">DESCRIPTION</span></span>
<span data-ttu-id="bc850-106">**AzVirtualNetworkUsageList** Cmdlet 會取得指定虛擬網路的每個子網使用量。</span><span class="sxs-lookup"><span data-stu-id="bc850-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="bc850-107">示例</span><span class="sxs-lookup"><span data-stu-id="bc850-107">EXAMPLES</span></span>

### <span data-ttu-id="bc850-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bc850-108">Example 1</span></span>
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

<span data-ttu-id="bc850-109">針對 usagetest 虛擬網路的使用方式，取得每個子網上的目前值。</span><span class="sxs-lookup"><span data-stu-id="bc850-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="bc850-110">參數</span><span class="sxs-lookup"><span data-stu-id="bc850-110">PARAMETERS</span></span>

### <span data-ttu-id="bc850-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc850-111">-DefaultProfile</span></span>
<span data-ttu-id="bc850-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bc850-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc850-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="bc850-113">-Name</span></span>
<span data-ttu-id="bc850-114">指定虛擬網路的名稱以顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="bc850-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="bc850-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc850-115">-ResourceGroupName</span></span>
<span data-ttu-id="bc850-116">指定虛擬網路所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc850-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="bc850-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc850-117">CommonParameters</span></span>
<span data-ttu-id="bc850-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc850-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc850-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bc850-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc850-120">輸入</span><span class="sxs-lookup"><span data-stu-id="bc850-120">INPUTS</span></span>

### <span data-ttu-id="bc850-121">System.object</span><span class="sxs-lookup"><span data-stu-id="bc850-121">System.String</span></span>

## <span data-ttu-id="bc850-122">輸出</span><span class="sxs-lookup"><span data-stu-id="bc850-122">OUTPUTS</span></span>

### <span data-ttu-id="bc850-123">PSVirtualNetworkUsage 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bc850-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="bc850-124">筆記</span><span class="sxs-lookup"><span data-stu-id="bc850-124">NOTES</span></span>

## <span data-ttu-id="bc850-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc850-125">RELATED LINKS</span></span>

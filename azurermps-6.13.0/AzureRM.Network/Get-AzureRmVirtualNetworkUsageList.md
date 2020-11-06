---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
ms.openlocfilehash: 855385b55922f6255b407ceafef7422113968516
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448377"
---
# <span data-ttu-id="d26fc-101">Get-AzureRmVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="d26fc-101">Get-AzureRmVirtualNetworkUsageList</span></span>

## <span data-ttu-id="d26fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d26fc-102">SYNOPSIS</span></span>
<span data-ttu-id="d26fc-103">取得虛擬網路的目前使用量。</span><span class="sxs-lookup"><span data-stu-id="d26fc-103">Gets virtual network current usage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d26fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="d26fc-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d26fc-105">說明</span><span class="sxs-lookup"><span data-stu-id="d26fc-105">DESCRIPTION</span></span>
<span data-ttu-id="d26fc-106">**AzureRmVirtualNetworkUsageList** Cmdlet 會取得指定虛擬網路的每個子網使用量。</span><span class="sxs-lookup"><span data-stu-id="d26fc-106">The **Get-AzureRmVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="d26fc-107">示例</span><span class="sxs-lookup"><span data-stu-id="d26fc-107">EXAMPLES</span></span>

### <span data-ttu-id="d26fc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d26fc-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

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

<span data-ttu-id="d26fc-109">針對 usagetest 虛擬網路的使用方式，取得每個子網上的目前值。</span><span class="sxs-lookup"><span data-stu-id="d26fc-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="d26fc-110">參數</span><span class="sxs-lookup"><span data-stu-id="d26fc-110">PARAMETERS</span></span>

### <span data-ttu-id="d26fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d26fc-111">-DefaultProfile</span></span>
<span data-ttu-id="d26fc-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d26fc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d26fc-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="d26fc-113">-Name</span></span>
<span data-ttu-id="d26fc-114">指定虛擬網路的名稱以顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="d26fc-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="d26fc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d26fc-115">-ResourceGroupName</span></span>
<span data-ttu-id="d26fc-116">指定虛擬網路所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d26fc-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="d26fc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d26fc-117">CommonParameters</span></span>
<span data-ttu-id="d26fc-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d26fc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d26fc-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d26fc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d26fc-120">輸入</span><span class="sxs-lookup"><span data-stu-id="d26fc-120">INPUTS</span></span>

### <span data-ttu-id="d26fc-121">System.object</span><span class="sxs-lookup"><span data-stu-id="d26fc-121">System.String</span></span>

## <span data-ttu-id="d26fc-122">輸出</span><span class="sxs-lookup"><span data-stu-id="d26fc-122">OUTPUTS</span></span>

### <span data-ttu-id="d26fc-123">PSVirtualNetworkUsage 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d26fc-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="d26fc-124">筆記</span><span class="sxs-lookup"><span data-stu-id="d26fc-124">NOTES</span></span>

## <span data-ttu-id="d26fc-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="d26fc-125">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: ff9ed8220cf2b30f2e652e207cb4d63db969a8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448376"
---
# <span data-ttu-id="b453b-101">Get-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="b453b-101">Get-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="b453b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b453b-102">SYNOPSIS</span></span>
<span data-ttu-id="b453b-103">取得虛擬網路攻絲</span><span class="sxs-lookup"><span data-stu-id="b453b-103">Gets a virtual network tap</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b453b-104">句法</span><span class="sxs-lookup"><span data-stu-id="b453b-104">SYNTAX</span></span>

### <span data-ttu-id="b453b-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b453b-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b453b-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b453b-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b453b-107">說明</span><span class="sxs-lookup"><span data-stu-id="b453b-107">DESCRIPTION</span></span>
<span data-ttu-id="b453b-108">**AzureRmVirtualNetworkTap** Cmdlet 會取得 azure 虛擬網路點或 azure 虛擬網路的清單，點擊 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="b453b-108">The **Get-AzureRmVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="b453b-109">示例</span><span class="sxs-lookup"><span data-stu-id="b453b-109">EXAMPLES</span></span>

### <span data-ttu-id="b453b-110">範例1：取得虛擬網路分流</span><span class="sxs-lookup"><span data-stu-id="b453b-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\>Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="b453b-111">這個命令會在「ResourceGroup1」中取得指定「VirtualTap1」的 VirtualNetwork 攻絲參照。</span><span class="sxs-lookup"><span data-stu-id="b453b-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

## <span data-ttu-id="b453b-112">參數</span><span class="sxs-lookup"><span data-stu-id="b453b-112">PARAMETERS</span></span>

### <span data-ttu-id="b453b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b453b-113">-DefaultProfile</span></span>
<span data-ttu-id="b453b-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b453b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b453b-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b453b-115">-Name</span></span>
<span data-ttu-id="b453b-116">攻絲的名稱。</span><span class="sxs-lookup"><span data-stu-id="b453b-116">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b453b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b453b-117">-ResourceGroupName</span></span>
<span data-ttu-id="b453b-118">虛擬網路的 [資源] 群組名稱。</span><span class="sxs-lookup"><span data-stu-id="b453b-118">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b453b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b453b-119">-ResourceId</span></span>
<span data-ttu-id="b453b-120">VirtualNetworkTap 資源的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="b453b-120">ResourceId of the VirtualNetworkTap resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b453b-121">-確認</span><span class="sxs-lookup"><span data-stu-id="b453b-121">-Confirm</span></span>
<span data-ttu-id="b453b-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b453b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b453b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b453b-123">-WhatIf</span></span>
<span data-ttu-id="b453b-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b453b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b453b-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b453b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b453b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b453b-126">CommonParameters</span></span>
<span data-ttu-id="b453b-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b453b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b453b-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b453b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b453b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b453b-129">INPUTS</span></span>

### <span data-ttu-id="b453b-130">System.object</span><span class="sxs-lookup"><span data-stu-id="b453b-130">System.String</span></span>

## <span data-ttu-id="b453b-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b453b-131">OUTPUTS</span></span>

### <span data-ttu-id="b453b-132">PSVirtualNetworkTap 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b453b-132">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="b453b-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b453b-133">NOTES</span></span>

## <span data-ttu-id="b453b-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b453b-134">RELATED LINKS</span></span>

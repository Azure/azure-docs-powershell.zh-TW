---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: 2cccbc06095f9ff71f4b16d40bca16d91e91dda0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913697"
---
# <span data-ttu-id="e21a8-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e21a8-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="e21a8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e21a8-102">SYNOPSIS</span></span>
<span data-ttu-id="e21a8-103">取得 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e21a8-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="e21a8-104">語法</span><span class="sxs-lookup"><span data-stu-id="e21a8-104">SYNTAX</span></span>

### <span data-ttu-id="e21a8-105">VirtualRouterSubscriptionIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e21a8-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e21a8-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e21a8-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e21a8-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e21a8-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e21a8-108">描述</span><span class="sxs-lookup"><span data-stu-id="e21a8-108">DESCRIPTION</span></span>
<span data-ttu-id="e21a8-109">**Get-AzVirtualRouter** Cmdlet 取得 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e21a8-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="e21a8-110">例子</span><span class="sxs-lookup"><span data-stu-id="e21a8-110">EXAMPLES</span></span>

### <span data-ttu-id="e21a8-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="e21a8-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="e21a8-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="e21a8-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="e21a8-113">參數</span><span class="sxs-lookup"><span data-stu-id="e21a8-113">PARAMETERS</span></span>

### <span data-ttu-id="e21a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e21a8-114">-DefaultProfile</span></span>
<span data-ttu-id="e21a8-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e21a8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e21a8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e21a8-116">-ResourceGroupName</span></span>
<span data-ttu-id="e21a8-117">虛擬路由器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e21a8-117">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e21a8-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e21a8-118">-ResourceId</span></span>
<span data-ttu-id="e21a8-119">虛擬路由器的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="e21a8-119">ResourceId of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e21a8-120">-RouterName</span><span class="sxs-lookup"><span data-stu-id="e21a8-120">-RouterName</span></span>
<span data-ttu-id="e21a8-121">虛擬路由器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e21a8-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e21a8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e21a8-122">CommonParameters</span></span>
<span data-ttu-id="e21a8-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e21a8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e21a8-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e21a8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e21a8-125">輸入</span><span class="sxs-lookup"><span data-stu-id="e21a8-125">INPUTS</span></span>

### <span data-ttu-id="e21a8-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e21a8-126">System.String</span></span>

## <span data-ttu-id="e21a8-127">輸出</span><span class="sxs-lookup"><span data-stu-id="e21a8-127">OUTPUTS</span></span>

### <span data-ttu-id="e21a8-128">Microsoft.Azure.Commands.Network.models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e21a8-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="e21a8-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e21a8-129">NOTES</span></span>

## <span data-ttu-id="e21a8-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e21a8-130">RELATED LINKS</span></span>

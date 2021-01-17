---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: e99df2f29781281ee0293f4cf52715153ff0d0cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287103"
---
# <span data-ttu-id="89424-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="89424-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="89424-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89424-102">SYNOPSIS</span></span>
<span data-ttu-id="89424-103">取得 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="89424-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="89424-104">句法</span><span class="sxs-lookup"><span data-stu-id="89424-104">SYNTAX</span></span>

### <span data-ttu-id="89424-105">VirtualRouterSubscriptionIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="89424-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89424-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="89424-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89424-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89424-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89424-108">說明</span><span class="sxs-lookup"><span data-stu-id="89424-108">DESCRIPTION</span></span>
<span data-ttu-id="89424-109">**AzVirtualRouter** Cmdlet 會取得 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="89424-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="89424-110">示例</span><span class="sxs-lookup"><span data-stu-id="89424-110">EXAMPLES</span></span>

### <span data-ttu-id="89424-111">範例1</span><span class="sxs-lookup"><span data-stu-id="89424-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="89424-112">範例2</span><span class="sxs-lookup"><span data-stu-id="89424-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="89424-113">參數</span><span class="sxs-lookup"><span data-stu-id="89424-113">PARAMETERS</span></span>

### <span data-ttu-id="89424-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89424-114">-DefaultProfile</span></span>
<span data-ttu-id="89424-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="89424-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89424-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89424-116">-ResourceGroupName</span></span>
<span data-ttu-id="89424-117">虛擬路由器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="89424-117">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="89424-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89424-118">-ResourceId</span></span>
<span data-ttu-id="89424-119">虛擬路由器的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="89424-119">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="89424-120">-RouterName</span><span class="sxs-lookup"><span data-stu-id="89424-120">-RouterName</span></span>
<span data-ttu-id="89424-121">虛擬路由器的名稱。</span><span class="sxs-lookup"><span data-stu-id="89424-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="89424-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89424-122">CommonParameters</span></span>
<span data-ttu-id="89424-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89424-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89424-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="89424-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89424-125">輸入</span><span class="sxs-lookup"><span data-stu-id="89424-125">INPUTS</span></span>

### <span data-ttu-id="89424-126">System.object</span><span class="sxs-lookup"><span data-stu-id="89424-126">System.String</span></span>

## <span data-ttu-id="89424-127">輸出</span><span class="sxs-lookup"><span data-stu-id="89424-127">OUTPUTS</span></span>

### <span data-ttu-id="89424-128">PSVirtualRouter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="89424-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="89424-129">筆記</span><span class="sxs-lookup"><span data-stu-id="89424-129">NOTES</span></span>

## <span data-ttu-id="89424-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="89424-130">RELATED LINKS</span></span>

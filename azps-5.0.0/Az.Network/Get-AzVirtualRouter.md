---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: 26e919935a65a486252cac234450adf214992b36
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138350"
---
# <span data-ttu-id="e849c-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e849c-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="e849c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e849c-102">SYNOPSIS</span></span>
<span data-ttu-id="e849c-103">取得 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e849c-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="e849c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e849c-104">SYNTAX</span></span>

### <span data-ttu-id="e849c-105">VirtualRouterSubscriptionIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e849c-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e849c-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e849c-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e849c-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e849c-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e849c-108">說明</span><span class="sxs-lookup"><span data-stu-id="e849c-108">DESCRIPTION</span></span>
<span data-ttu-id="e849c-109">**AzVirtualRouter** Cmdlet 會取得 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e849c-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="e849c-110">示例</span><span class="sxs-lookup"><span data-stu-id="e849c-110">EXAMPLES</span></span>

### <span data-ttu-id="e849c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e849c-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="e849c-112">範例2</span><span class="sxs-lookup"><span data-stu-id="e849c-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="e849c-113">參數</span><span class="sxs-lookup"><span data-stu-id="e849c-113">PARAMETERS</span></span>

### <span data-ttu-id="e849c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e849c-114">-DefaultProfile</span></span>
<span data-ttu-id="e849c-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e849c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e849c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e849c-116">-ResourceGroupName</span></span>
<span data-ttu-id="e849c-117">虛擬路由器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e849c-117">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="e849c-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e849c-118">-ResourceId</span></span>
<span data-ttu-id="e849c-119">虛擬路由器的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="e849c-119">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="e849c-120">-RouterName</span><span class="sxs-lookup"><span data-stu-id="e849c-120">-RouterName</span></span>
<span data-ttu-id="e849c-121">虛擬路由器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e849c-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="e849c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e849c-122">CommonParameters</span></span>
<span data-ttu-id="e849c-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e849c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e849c-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e849c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e849c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="e849c-125">INPUTS</span></span>

### <span data-ttu-id="e849c-126">System.object</span><span class="sxs-lookup"><span data-stu-id="e849c-126">System.String</span></span>

## <span data-ttu-id="e849c-127">輸出</span><span class="sxs-lookup"><span data-stu-id="e849c-127">OUTPUTS</span></span>

### <span data-ttu-id="e849c-128">PSVirtualRouter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e849c-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="e849c-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e849c-129">NOTES</span></span>

## <span data-ttu-id="e849c-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e849c-130">RELATED LINKS</span></span>

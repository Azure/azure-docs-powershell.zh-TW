---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: dc568657feb5f86cf7cfaa21042e03f8470a9caa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957306"
---
# <span data-ttu-id="1b3ce-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="1b3ce-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="1b3ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b3ce-102">SYNOPSIS</span></span>
<span data-ttu-id="1b3ce-103">取得 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="1b3ce-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="1b3ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b3ce-104">SYNTAX</span></span>

### <span data-ttu-id="1b3ce-105">VirtualRouterNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1b3ce-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b3ce-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b3ce-106">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b3ce-107">說明</span><span class="sxs-lookup"><span data-stu-id="1b3ce-107">DESCRIPTION</span></span>
<span data-ttu-id="1b3ce-108">**AzVirtualRouter** Cmdlet 會取得 Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="1b3ce-108">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="1b3ce-109">示例</span><span class="sxs-lookup"><span data-stu-id="1b3ce-109">EXAMPLES</span></span>

### <span data-ttu-id="1b3ce-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1b3ce-110">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter 
```

### <span data-ttu-id="1b3ce-111">範例2</span><span class="sxs-lookup"><span data-stu-id="1b3ce-111">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="1b3ce-112">參數</span><span class="sxs-lookup"><span data-stu-id="1b3ce-112">PARAMETERS</span></span>

### <span data-ttu-id="1b3ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b3ce-113">-DefaultProfile</span></span>
<span data-ttu-id="1b3ce-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b3ce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3ce-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b3ce-115">-ResourceGroupName</span></span>
<span data-ttu-id="1b3ce-116">虛擬路由器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1b3ce-116">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b3ce-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b3ce-117">-ResourceId</span></span>
<span data-ttu-id="1b3ce-118">虛擬路由器的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="1b3ce-118">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b3ce-119">-RouterName</span><span class="sxs-lookup"><span data-stu-id="1b3ce-119">-RouterName</span></span>
<span data-ttu-id="1b3ce-120">虛擬路由器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b3ce-120">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b3ce-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b3ce-121">CommonParameters</span></span>
<span data-ttu-id="1b3ce-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b3ce-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b3ce-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b3ce-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b3ce-124">輸入</span><span class="sxs-lookup"><span data-stu-id="1b3ce-124">INPUTS</span></span>

### <span data-ttu-id="1b3ce-125">System.object</span><span class="sxs-lookup"><span data-stu-id="1b3ce-125">System.String</span></span>

## <span data-ttu-id="1b3ce-126">輸出</span><span class="sxs-lookup"><span data-stu-id="1b3ce-126">OUTPUTS</span></span>

### <span data-ttu-id="1b3ce-127">PSVirtualRouter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1b3ce-127">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="1b3ce-128">筆記</span><span class="sxs-lookup"><span data-stu-id="1b3ce-128">NOTES</span></span>

## <span data-ttu-id="1b3ce-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b3ce-129">RELATED LINKS</span></span>

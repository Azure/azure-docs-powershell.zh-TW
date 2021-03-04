---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
ms.openlocfilehash: 119dec74416b8447d04aef7ae101016490408b5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901814"
---
# <span data-ttu-id="7bbaa-101">Update-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="7bbaa-101">Update-AzVirtualRouter</span></span>

## <span data-ttu-id="7bbaa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7bbaa-102">SYNOPSIS</span></span>
<span data-ttu-id="7bbaa-103">更新虛擬路由器。</span><span class="sxs-lookup"><span data-stu-id="7bbaa-103">Updates a Virtual Router.</span></span> 

## <span data-ttu-id="7bbaa-104">語法</span><span class="sxs-lookup"><span data-stu-id="7bbaa-104">SYNTAX</span></span>

### <span data-ttu-id="7bbaa-105">VirtualRouterNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7bbaa-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bbaa-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bbaa-106">VirtualRouterResourceIdParameterSet</span></span>
```
Update-AzVirtualRouter [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bbaa-107">描述</span><span class="sxs-lookup"><span data-stu-id="7bbaa-107">DESCRIPTION</span></span>
<span data-ttu-id="7bbaa-108">更新虛擬路由器以啟用或停用分支流量的分支。</span><span class="sxs-lookup"><span data-stu-id="7bbaa-108">Updates Virtual Router to enable or disable branch to branch traffic.</span></span>

## <span data-ttu-id="7bbaa-109">例子</span><span class="sxs-lookup"><span data-stu-id="7bbaa-109">EXAMPLES</span></span>

### <span data-ttu-id="7bbaa-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="7bbaa-110">Example 1</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName -AllowBranchToBranchTraffic
```

<span data-ttu-id="7bbaa-111">更新虛擬路由器以允許分支到分支流量</span><span class="sxs-lookup"><span data-stu-id="7bbaa-111">Updates the Virtual Router to allow branch to branch traffic</span></span>

### <span data-ttu-id="7bbaa-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="7bbaa-112">Example 2</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName
```

<span data-ttu-id="7bbaa-113">更新虛擬路由器以封鎖分支流量</span><span class="sxs-lookup"><span data-stu-id="7bbaa-113">Updates the Virtual Router to block branch to branch traffic</span></span>

## <span data-ttu-id="7bbaa-114">參數</span><span class="sxs-lookup"><span data-stu-id="7bbaa-114">PARAMETERS</span></span>

### <span data-ttu-id="7bbaa-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="7bbaa-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="7bbaa-116">旗標以允許虛擬路由器分支流量。</span><span class="sxs-lookup"><span data-stu-id="7bbaa-116">Flag to allow branch to branch traffic for virtual router.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bbaa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bbaa-117">-DefaultProfile</span></span>
<span data-ttu-id="7bbaa-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7bbaa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bbaa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bbaa-119">-ResourceGroupName</span></span>
<span data-ttu-id="7bbaa-120">虛擬路由器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="7bbaa-120">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bbaa-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bbaa-121">-ResourceId</span></span>
<span data-ttu-id="7bbaa-122">虛擬路由器的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="7bbaa-122">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="7bbaa-123">-RouterName</span><span class="sxs-lookup"><span data-stu-id="7bbaa-123">-RouterName</span></span>
<span data-ttu-id="7bbaa-124">虛擬路由器的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bbaa-124">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bbaa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bbaa-125">CommonParameters</span></span>
<span data-ttu-id="7bbaa-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7bbaa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bbaa-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bbaa-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bbaa-128">輸入</span><span class="sxs-lookup"><span data-stu-id="7bbaa-128">INPUTS</span></span>

### <span data-ttu-id="7bbaa-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7bbaa-129">System.String</span></span>

## <span data-ttu-id="7bbaa-130">輸出</span><span class="sxs-lookup"><span data-stu-id="7bbaa-130">OUTPUTS</span></span>

### <span data-ttu-id="7bbaa-131">Microsoft.Azure.Commands.Network.models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="7bbaa-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="7bbaa-132">筆記</span><span class="sxs-lookup"><span data-stu-id="7bbaa-132">NOTES</span></span>

## <span data-ttu-id="7bbaa-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="7bbaa-133">RELATED LINKS</span></span>

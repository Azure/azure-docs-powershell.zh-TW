---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
ms.openlocfilehash: d7f52ded01ce5b785c1e935ba8d3ebf4b1c0a5fa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280316"
---
# <span data-ttu-id="a5a50-101">Update-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a5a50-101">Update-AzVirtualRouter</span></span>

## <span data-ttu-id="a5a50-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5a50-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a50-103">更新虛擬路由器。</span><span class="sxs-lookup"><span data-stu-id="a5a50-103">Updates a Virtual Router.</span></span> 

## <span data-ttu-id="a5a50-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5a50-104">SYNTAX</span></span>

### <span data-ttu-id="a5a50-105">VirtualRouterNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a5a50-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5a50-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5a50-106">VirtualRouterResourceIdParameterSet</span></span>
```
Update-AzVirtualRouter [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5a50-107">說明</span><span class="sxs-lookup"><span data-stu-id="a5a50-107">DESCRIPTION</span></span>
<span data-ttu-id="a5a50-108">更新虛擬路由器以啟用或停用分支來分支流量。</span><span class="sxs-lookup"><span data-stu-id="a5a50-108">Updates Virtual Router to enable or disable branch to branch traffic.</span></span>

## <span data-ttu-id="a5a50-109">示例</span><span class="sxs-lookup"><span data-stu-id="a5a50-109">EXAMPLES</span></span>

### <span data-ttu-id="a5a50-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a5a50-110">Example 1</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName -AllowBranchToBranchTraffic
```

<span data-ttu-id="a5a50-111">更新虛擬路由器以允許分支分支流量</span><span class="sxs-lookup"><span data-stu-id="a5a50-111">Updates the Virtual Router to allow branch to branch traffic</span></span>

### <span data-ttu-id="a5a50-112">範例2</span><span class="sxs-lookup"><span data-stu-id="a5a50-112">Example 2</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName
```

<span data-ttu-id="a5a50-113">更新虛擬路由器以封鎖分支分支流量</span><span class="sxs-lookup"><span data-stu-id="a5a50-113">Updates the Virtual Router to block branch to branch traffic</span></span>

## <span data-ttu-id="a5a50-114">參數</span><span class="sxs-lookup"><span data-stu-id="a5a50-114">PARAMETERS</span></span>

### <span data-ttu-id="a5a50-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="a5a50-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="a5a50-116">[旗標] 可讓分支加入虛擬路由器的分支。</span><span class="sxs-lookup"><span data-stu-id="a5a50-116">Flag to allow branch to branch traffic for virtual router.</span></span>

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

### <span data-ttu-id="a5a50-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a50-117">-DefaultProfile</span></span>
<span data-ttu-id="a5a50-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5a50-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a50-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a50-119">-ResourceGroupName</span></span>
<span data-ttu-id="a5a50-120">虛擬路由器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a5a50-120">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="a5a50-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5a50-121">-ResourceId</span></span>
<span data-ttu-id="a5a50-122">虛擬路由器的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="a5a50-122">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="a5a50-123">-RouterName</span><span class="sxs-lookup"><span data-stu-id="a5a50-123">-RouterName</span></span>
<span data-ttu-id="a5a50-124">虛擬路由器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5a50-124">The name of the virtual router.</span></span>

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

### <span data-ttu-id="a5a50-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a50-125">CommonParameters</span></span>
<span data-ttu-id="a5a50-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5a50-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a50-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a5a50-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a50-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a5a50-128">INPUTS</span></span>

### <span data-ttu-id="a5a50-129">System.object</span><span class="sxs-lookup"><span data-stu-id="a5a50-129">System.String</span></span>

## <span data-ttu-id="a5a50-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a5a50-130">OUTPUTS</span></span>

### <span data-ttu-id="a5a50-131">PSVirtualRouter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a5a50-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="a5a50-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a5a50-132">NOTES</span></span>

## <span data-ttu-id="a5a50-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5a50-133">RELATED LINKS</span></span>

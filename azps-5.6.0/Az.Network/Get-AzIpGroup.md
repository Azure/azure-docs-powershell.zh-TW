---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 75a7afbb8997492e1b30ead7f745d2f5b6eb8b5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903146"
---
# <span data-ttu-id="f7735-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f7735-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="f7735-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f7735-102">SYNOPSIS</span></span>
<span data-ttu-id="f7735-103">取得 Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="f7735-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="f7735-104">語法</span><span class="sxs-lookup"><span data-stu-id="f7735-104">SYNTAX</span></span>

### <span data-ttu-id="f7735-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7735-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7735-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7735-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7735-107">描述</span><span class="sxs-lookup"><span data-stu-id="f7735-107">DESCRIPTION</span></span>
<span data-ttu-id="f7735-108">**Get-AzIpGroup** Cmdlet 會取得 Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="f7735-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="f7735-109">例子</span><span class="sxs-lookup"><span data-stu-id="f7735-109">EXAMPLES</span></span>

### <span data-ttu-id="f7735-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="f7735-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="f7735-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="f7735-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="f7735-112">參數</span><span class="sxs-lookup"><span data-stu-id="f7735-112">PARAMETERS</span></span>

### <span data-ttu-id="f7735-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7735-113">-DefaultProfile</span></span>
<span data-ttu-id="f7735-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7735-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7735-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7735-115">-Name</span></span>
<span data-ttu-id="f7735-116">ipgroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7735-116">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7735-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7735-117">-ResourceGroupName</span></span>
<span data-ttu-id="f7735-118">ipgroup 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f7735-118">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7735-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7735-119">-ResourceId</span></span>
<span data-ttu-id="f7735-120">Ipgroup 的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="f7735-120">ResourceId of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7735-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7735-121">CommonParameters</span></span>
<span data-ttu-id="f7735-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f7735-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7735-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7735-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7735-124">輸入</span><span class="sxs-lookup"><span data-stu-id="f7735-124">INPUTS</span></span>

### <span data-ttu-id="f7735-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f7735-125">System.String</span></span>

## <span data-ttu-id="f7735-126">輸出</span><span class="sxs-lookup"><span data-stu-id="f7735-126">OUTPUTS</span></span>

### <span data-ttu-id="f7735-127">Microsoft.Azure.Commands.Network.models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="f7735-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="f7735-128">筆記</span><span class="sxs-lookup"><span data-stu-id="f7735-128">NOTES</span></span>

## <span data-ttu-id="f7735-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7735-129">RELATED LINKS</span></span>

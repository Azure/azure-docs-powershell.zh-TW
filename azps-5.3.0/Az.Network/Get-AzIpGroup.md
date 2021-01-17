---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 11c5e3ff2d8ee548917de7a94b1a592ae4cce52b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436779"
---
# <span data-ttu-id="e6b0e-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e6b0e-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="e6b0e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b0e-103">取得 Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="e6b0e-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="e6b0e-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6b0e-104">SYNTAX</span></span>

### <span data-ttu-id="e6b0e-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b0e-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6b0e-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b0e-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6b0e-107">說明</span><span class="sxs-lookup"><span data-stu-id="e6b0e-107">DESCRIPTION</span></span>
<span data-ttu-id="e6b0e-108">**AzIpGroup** Cmdlet 會取得 Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="e6b0e-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="e6b0e-109">示例</span><span class="sxs-lookup"><span data-stu-id="e6b0e-109">EXAMPLES</span></span>

### <span data-ttu-id="e6b0e-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e6b0e-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="e6b0e-111">範例2</span><span class="sxs-lookup"><span data-stu-id="e6b0e-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="e6b0e-112">參數</span><span class="sxs-lookup"><span data-stu-id="e6b0e-112">PARAMETERS</span></span>

### <span data-ttu-id="e6b0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b0e-113">-DefaultProfile</span></span>
<span data-ttu-id="e6b0e-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6b0e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6b0e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e6b0e-115">-Name</span></span>
<span data-ttu-id="e6b0e-116">Ipgroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6b0e-116">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="e6b0e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6b0e-117">-ResourceGroupName</span></span>
<span data-ttu-id="e6b0e-118">Ipgroup 的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e6b0e-118">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="e6b0e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6b0e-119">-ResourceId</span></span>
<span data-ttu-id="e6b0e-120">Ipgroup 的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="e6b0e-120">ResourceId of the ipgroup.</span></span>

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

### <span data-ttu-id="e6b0e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b0e-121">CommonParameters</span></span>
<span data-ttu-id="e6b0e-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6b0e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b0e-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e6b0e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b0e-124">輸入</span><span class="sxs-lookup"><span data-stu-id="e6b0e-124">INPUTS</span></span>

### <span data-ttu-id="e6b0e-125">System.object</span><span class="sxs-lookup"><span data-stu-id="e6b0e-125">System.String</span></span>

## <span data-ttu-id="e6b0e-126">輸出</span><span class="sxs-lookup"><span data-stu-id="e6b0e-126">OUTPUTS</span></span>

### <span data-ttu-id="e6b0e-127">PSIpGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e6b0e-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="e6b0e-128">筆記</span><span class="sxs-lookup"><span data-stu-id="e6b0e-128">NOTES</span></span>

## <span data-ttu-id="e6b0e-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6b0e-129">RELATED LINKS</span></span>

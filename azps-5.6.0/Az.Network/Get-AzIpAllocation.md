---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: c08a148d1c58e08daa2fce8cd1e195887a264f19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903149"
---
# <span data-ttu-id="43e61-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="43e61-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="43e61-102">簡介</span><span class="sxs-lookup"><span data-stu-id="43e61-102">SYNOPSIS</span></span>
<span data-ttu-id="43e61-103">獲得 Azure IpAllocation。</span><span class="sxs-lookup"><span data-stu-id="43e61-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="43e61-104">語法</span><span class="sxs-lookup"><span data-stu-id="43e61-104">SYNTAX</span></span>

### <span data-ttu-id="43e61-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e61-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43e61-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e61-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43e61-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e61-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43e61-108">描述</span><span class="sxs-lookup"><span data-stu-id="43e61-108">DESCRIPTION</span></span>
<span data-ttu-id="43e61-109">**Get-AzIpAllocation** Cmdlet 會取得 Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="43e61-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="43e61-110">例子</span><span class="sxs-lookup"><span data-stu-id="43e61-110">EXAMPLES</span></span>

### <span data-ttu-id="43e61-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="43e61-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="43e61-112">參數</span><span class="sxs-lookup"><span data-stu-id="43e61-112">PARAMETERS</span></span>

### <span data-ttu-id="43e61-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43e61-113">-DefaultProfile</span></span>
<span data-ttu-id="43e61-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="43e61-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43e61-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="43e61-115">-Name</span></span>
<span data-ttu-id="43e61-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="43e61-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e61-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43e61-117">-ResourceGroupName</span></span>
<span data-ttu-id="43e61-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="43e61-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e61-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43e61-119">-ResourceId</span></span>
<span data-ttu-id="43e61-120">IpAllocation 識別碼</span><span class="sxs-lookup"><span data-stu-id="43e61-120">IpAllocation Id</span></span>

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

### <span data-ttu-id="43e61-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43e61-121">CommonParameters</span></span>
<span data-ttu-id="43e61-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="43e61-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43e61-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43e61-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43e61-124">輸入</span><span class="sxs-lookup"><span data-stu-id="43e61-124">INPUTS</span></span>

### <span data-ttu-id="43e61-125">System.String</span><span class="sxs-lookup"><span data-stu-id="43e61-125">System.String</span></span>

## <span data-ttu-id="43e61-126">輸出</span><span class="sxs-lookup"><span data-stu-id="43e61-126">OUTPUTS</span></span>

### <span data-ttu-id="43e61-127">Microsoft.Azure.Commands.Network.models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="43e61-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="43e61-128">筆記</span><span class="sxs-lookup"><span data-stu-id="43e61-128">NOTES</span></span>

## <span data-ttu-id="43e61-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="43e61-129">RELATED LINKS</span></span>

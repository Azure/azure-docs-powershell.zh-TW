---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: e03ec2b7f2ceba70ba3037bbcad232dbfa7490de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908057"
---
# <span data-ttu-id="d6bda-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="d6bda-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="d6bda-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d6bda-102">SYNOPSIS</span></span>
<span data-ttu-id="d6bda-103">會保存已修改的 IpAllocation。</span><span class="sxs-lookup"><span data-stu-id="d6bda-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="d6bda-104">語法</span><span class="sxs-lookup"><span data-stu-id="d6bda-104">SYNTAX</span></span>

### <span data-ttu-id="d6bda-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6bda-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6bda-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6bda-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6bda-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6bda-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6bda-108">描述</span><span class="sxs-lookup"><span data-stu-id="d6bda-108">DESCRIPTION</span></span>
<span data-ttu-id="d6bda-109">**Set-AzIpAllocation** Cmdlet 會更新 Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="d6bda-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="d6bda-110">例子</span><span class="sxs-lookup"><span data-stu-id="d6bda-110">EXAMPLES</span></span>

### <span data-ttu-id="d6bda-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="d6bda-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="d6bda-112">參數</span><span class="sxs-lookup"><span data-stu-id="d6bda-112">PARAMETERS</span></span>

### <span data-ttu-id="d6bda-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6bda-113">-AsJob</span></span>
<span data-ttu-id="d6bda-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d6bda-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6bda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6bda-115">-DefaultProfile</span></span>
<span data-ttu-id="d6bda-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6bda-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6bda-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6bda-117">-InputObject</span></span>
<span data-ttu-id="d6bda-118">The IpAllocation</span><span class="sxs-lookup"><span data-stu-id="d6bda-118">The IpAllocation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation
Parameter Sets: SetByInputObjectParameterSet
Aliases: IpAllocation

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6bda-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="d6bda-119">-IpAllocationTag</span></span>
<span data-ttu-id="d6bda-120">IP 配置的配置標記</span><span class="sxs-lookup"><span data-stu-id="d6bda-120">The allocation tags of the IP allocation</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6bda-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6bda-121">-Name</span></span>
<span data-ttu-id="d6bda-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d6bda-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6bda-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6bda-123">-ResourceGroupName</span></span>
<span data-ttu-id="d6bda-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d6bda-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6bda-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6bda-125">-ResourceId</span></span>
<span data-ttu-id="d6bda-126">IpAllocation 識別碼</span><span class="sxs-lookup"><span data-stu-id="d6bda-126">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: IpAllocationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6bda-127">-標記</span><span class="sxs-lookup"><span data-stu-id="d6bda-127">-Tag</span></span>
<span data-ttu-id="d6bda-128">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d6bda-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6bda-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6bda-129">CommonParameters</span></span>
<span data-ttu-id="d6bda-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d6bda-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6bda-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6bda-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6bda-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d6bda-132">INPUTS</span></span>

### <span data-ttu-id="d6bda-133">Microsoft.Azure.Commands.Network.models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="d6bda-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="d6bda-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d6bda-134">OUTPUTS</span></span>

### <span data-ttu-id="d6bda-135">Microsoft.Azure.Commands.Network.models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="d6bda-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="d6bda-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d6bda-136">NOTES</span></span>

## <span data-ttu-id="d6bda-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6bda-137">RELATED LINKS</span></span>

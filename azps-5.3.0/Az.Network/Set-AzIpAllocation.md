---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: 4d817dcabe73972b3a8f21de5b9b0906d7a95cc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450149"
---
# <span data-ttu-id="04a1a-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="04a1a-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="04a1a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="04a1a-103">儲存已修改的 IpAllocation。</span><span class="sxs-lookup"><span data-stu-id="04a1a-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="04a1a-104">句法</span><span class="sxs-lookup"><span data-stu-id="04a1a-104">SYNTAX</span></span>

### <span data-ttu-id="04a1a-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="04a1a-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04a1a-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04a1a-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04a1a-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04a1a-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04a1a-108">說明</span><span class="sxs-lookup"><span data-stu-id="04a1a-108">DESCRIPTION</span></span>
<span data-ttu-id="04a1a-109">**AzIpAllocation** Cmdlet 會更新 Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="04a1a-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="04a1a-110">示例</span><span class="sxs-lookup"><span data-stu-id="04a1a-110">EXAMPLES</span></span>

### <span data-ttu-id="04a1a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="04a1a-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="04a1a-112">參數</span><span class="sxs-lookup"><span data-stu-id="04a1a-112">PARAMETERS</span></span>

### <span data-ttu-id="04a1a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04a1a-113">-AsJob</span></span>
<span data-ttu-id="04a1a-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="04a1a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04a1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04a1a-115">-DefaultProfile</span></span>
<span data-ttu-id="04a1a-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="04a1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04a1a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04a1a-117">-InputObject</span></span>
<span data-ttu-id="04a1a-118">IpAllocation</span><span class="sxs-lookup"><span data-stu-id="04a1a-118">The IpAllocation</span></span>

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

### <span data-ttu-id="04a1a-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="04a1a-119">-IpAllocationTag</span></span>
<span data-ttu-id="04a1a-120">IP 分配的分攤標記</span><span class="sxs-lookup"><span data-stu-id="04a1a-120">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="04a1a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="04a1a-121">-Name</span></span>
<span data-ttu-id="04a1a-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="04a1a-122">The resource name.</span></span>

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

### <span data-ttu-id="04a1a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04a1a-123">-ResourceGroupName</span></span>
<span data-ttu-id="04a1a-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="04a1a-124">The resource group name.</span></span>

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

### <span data-ttu-id="04a1a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04a1a-125">-ResourceId</span></span>
<span data-ttu-id="04a1a-126">IpAllocation 識別碼</span><span class="sxs-lookup"><span data-stu-id="04a1a-126">IpAllocation Id</span></span>

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

### <span data-ttu-id="04a1a-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="04a1a-127">-Tag</span></span>
<span data-ttu-id="04a1a-128">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="04a1a-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="04a1a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04a1a-129">CommonParameters</span></span>
<span data-ttu-id="04a1a-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04a1a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04a1a-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="04a1a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04a1a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="04a1a-132">INPUTS</span></span>

### <span data-ttu-id="04a1a-133">PSIpAllocation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="04a1a-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="04a1a-134">輸出</span><span class="sxs-lookup"><span data-stu-id="04a1a-134">OUTPUTS</span></span>

### <span data-ttu-id="04a1a-135">PSIpAllocation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="04a1a-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="04a1a-136">筆記</span><span class="sxs-lookup"><span data-stu-id="04a1a-136">NOTES</span></span>

## <span data-ttu-id="04a1a-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="04a1a-137">RELATED LINKS</span></span>

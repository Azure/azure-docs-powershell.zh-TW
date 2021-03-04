---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: 1b33803ff3a33897d46519952db99ceda1b12c99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912058"
---
# <span data-ttu-id="3dd25-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="3dd25-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="3dd25-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3dd25-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd25-103">取得或列出主機。</span><span class="sxs-lookup"><span data-stu-id="3dd25-103">Get or list hosts.</span></span>

## <span data-ttu-id="3dd25-104">語法</span><span class="sxs-lookup"><span data-stu-id="3dd25-104">SYNTAX</span></span>

### <span data-ttu-id="3dd25-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="3dd25-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dd25-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="3dd25-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dd25-107">描述</span><span class="sxs-lookup"><span data-stu-id="3dd25-107">DESCRIPTION</span></span>
<span data-ttu-id="3dd25-108">此 Cmdlet 會取得主機群組。</span><span class="sxs-lookup"><span data-stu-id="3dd25-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="3dd25-109">如果未提供主機組名，此 Cmdlet 也會列出資源群組中所有的主機群組。</span><span class="sxs-lookup"><span data-stu-id="3dd25-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="3dd25-110">如果未提供主機組名和資源組名，此 Cmdlet 也會列出訂閱中所有的主機群組。</span><span class="sxs-lookup"><span data-stu-id="3dd25-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="3dd25-111">例子</span><span class="sxs-lookup"><span data-stu-id="3dd25-111">EXAMPLES</span></span>

### <span data-ttu-id="3dd25-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="3dd25-112">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="3dd25-113">此命令會返回主機群組。</span><span class="sxs-lookup"><span data-stu-id="3dd25-113">This command returns a host group.</span></span>

### <span data-ttu-id="3dd25-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="3dd25-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="3dd25-115">此命令會返回給定資源群組中所有的主機群組。</span><span class="sxs-lookup"><span data-stu-id="3dd25-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="3dd25-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="3dd25-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="3dd25-117">此命令會返回訂閱中所有的主機群組。</span><span class="sxs-lookup"><span data-stu-id="3dd25-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="3dd25-118">參數</span><span class="sxs-lookup"><span data-stu-id="3dd25-118">PARAMETERS</span></span>

### <span data-ttu-id="3dd25-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd25-119">-DefaultProfile</span></span>
<span data-ttu-id="3dd25-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3dd25-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dd25-121">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="3dd25-121">-InstanceView</span></span>
<span data-ttu-id="3dd25-122">展開所返回的物件，同時列出主機的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="3dd25-122">Expand the returned object to also list the host's instance views.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dd25-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="3dd25-123">-Name</span></span>
<span data-ttu-id="3dd25-124">主機組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3dd25-124">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd25-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dd25-125">-ResourceGroupName</span></span>
<span data-ttu-id="3dd25-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3dd25-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd25-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3dd25-127">-ResourceId</span></span>
<span data-ttu-id="3dd25-128">資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3dd25-128">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd25-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd25-129">CommonParameters</span></span>
<span data-ttu-id="3dd25-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3dd25-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd25-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3dd25-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd25-132">輸入</span><span class="sxs-lookup"><span data-stu-id="3dd25-132">INPUTS</span></span>

### <span data-ttu-id="3dd25-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3dd25-133">System.String</span></span>

## <span data-ttu-id="3dd25-134">輸出</span><span class="sxs-lookup"><span data-stu-id="3dd25-134">OUTPUTS</span></span>

### <span data-ttu-id="3dd25-135">Microsoft.Azure.Commands.Compute.Automation.models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="3dd25-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="3dd25-136">筆記</span><span class="sxs-lookup"><span data-stu-id="3dd25-136">NOTES</span></span>

## <span data-ttu-id="3dd25-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="3dd25-137">RELATED LINKS</span></span>

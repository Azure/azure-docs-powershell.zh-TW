---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: e0d15be05bf5678eb645a2a26dc2459e6790210a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446463"
---
# <span data-ttu-id="964db-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="964db-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="964db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="964db-102">SYNOPSIS</span></span>
<span data-ttu-id="964db-103">取得或列出主機。</span><span class="sxs-lookup"><span data-stu-id="964db-103">Get or list hosts.</span></span>

## <span data-ttu-id="964db-104">句法</span><span class="sxs-lookup"><span data-stu-id="964db-104">SYNTAX</span></span>

### <span data-ttu-id="964db-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="964db-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="964db-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="964db-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="964db-107">說明</span><span class="sxs-lookup"><span data-stu-id="964db-107">DESCRIPTION</span></span>
<span data-ttu-id="964db-108">這個 Cmdlet 會取得主機群組。</span><span class="sxs-lookup"><span data-stu-id="964db-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="964db-109">如果未指定主機組名稱，此 Cmdlet 也會列出資源群組中的所有主機組。</span><span class="sxs-lookup"><span data-stu-id="964db-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="964db-110">如果沒有提供主機組名稱或資源群組名稱，此 Cmdlet 也會列出訂閱中的所有主機組。</span><span class="sxs-lookup"><span data-stu-id="964db-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="964db-111">示例</span><span class="sxs-lookup"><span data-stu-id="964db-111">EXAMPLES</span></span>

### <span data-ttu-id="964db-112">範例1</span><span class="sxs-lookup"><span data-stu-id="964db-112">Example 1</span></span>
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

<span data-ttu-id="964db-113">這個命令會傳回主機群組。</span><span class="sxs-lookup"><span data-stu-id="964db-113">This command returns a host group.</span></span>

### <span data-ttu-id="964db-114">範例2</span><span class="sxs-lookup"><span data-stu-id="964db-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="964db-115">這個命令會傳回指定資源群組中的所有主機群組。</span><span class="sxs-lookup"><span data-stu-id="964db-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="964db-116">範例3</span><span class="sxs-lookup"><span data-stu-id="964db-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="964db-117">這個命令會傳回訂閱中的所有主機群組。</span><span class="sxs-lookup"><span data-stu-id="964db-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="964db-118">參數</span><span class="sxs-lookup"><span data-stu-id="964db-118">PARAMETERS</span></span>

### <span data-ttu-id="964db-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="964db-119">-DefaultProfile</span></span>
<span data-ttu-id="964db-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="964db-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="964db-121">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="964db-121">-InstanceView</span></span>
<span data-ttu-id="964db-122">展開傳回的物件，也會列出主機的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="964db-122">Expand the returned object to also list the host's instance views.</span></span> 

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

### <span data-ttu-id="964db-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="964db-123">-Name</span></span>
<span data-ttu-id="964db-124">主機群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="964db-124">The name of the host group.</span></span>

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

### <span data-ttu-id="964db-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="964db-125">-ResourceGroupName</span></span>
<span data-ttu-id="964db-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="964db-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="964db-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="964db-127">-ResourceId</span></span>
<span data-ttu-id="964db-128">資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="964db-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="964db-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="964db-129">CommonParameters</span></span>
<span data-ttu-id="964db-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="964db-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="964db-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="964db-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="964db-132">輸入</span><span class="sxs-lookup"><span data-stu-id="964db-132">INPUTS</span></span>

### <span data-ttu-id="964db-133">System.object</span><span class="sxs-lookup"><span data-stu-id="964db-133">System.String</span></span>

## <span data-ttu-id="964db-134">輸出</span><span class="sxs-lookup"><span data-stu-id="964db-134">OUTPUTS</span></span>

### <span data-ttu-id="964db-135">PSHostGroup 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="964db-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="964db-136">筆記</span><span class="sxs-lookup"><span data-stu-id="964db-136">NOTES</span></span>

## <span data-ttu-id="964db-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="964db-137">RELATED LINKS</span></span>

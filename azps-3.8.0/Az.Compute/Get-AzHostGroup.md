---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: 26030677743b95ebb11431118ccae8adf0b08bcd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959625"
---
# <span data-ttu-id="7b5bf-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="7b5bf-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="7b5bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b5bf-102">SYNOPSIS</span></span>
<span data-ttu-id="7b5bf-103">取得或列出主機。</span><span class="sxs-lookup"><span data-stu-id="7b5bf-103">Get or list hosts.</span></span>

## <span data-ttu-id="7b5bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="7b5bf-104">SYNTAX</span></span>

### <span data-ttu-id="7b5bf-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="7b5bf-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b5bf-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="7b5bf-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b5bf-107">說明</span><span class="sxs-lookup"><span data-stu-id="7b5bf-107">DESCRIPTION</span></span>
<span data-ttu-id="7b5bf-108">這個 Cmdlet 會取得主機群組。</span><span class="sxs-lookup"><span data-stu-id="7b5bf-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="7b5bf-109">如果未指定主機組名稱，此 Cmdlet 也會列出資源群組中的所有主機組。</span><span class="sxs-lookup"><span data-stu-id="7b5bf-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="7b5bf-110">如果沒有提供主機組名稱或資源群組名稱，此 Cmdlet 也會列出訂閱中的所有主機組。</span><span class="sxs-lookup"><span data-stu-id="7b5bf-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="7b5bf-111">示例</span><span class="sxs-lookup"><span data-stu-id="7b5bf-111">EXAMPLES</span></span>

### <span data-ttu-id="7b5bf-112">範例1</span><span class="sxs-lookup"><span data-stu-id="7b5bf-112">Example 1</span></span>
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

<span data-ttu-id="7b5bf-113">這個命令會傳回主機群組。</span><span class="sxs-lookup"><span data-stu-id="7b5bf-113">This command returns a host group.</span></span>

### <span data-ttu-id="7b5bf-114">範例2</span><span class="sxs-lookup"><span data-stu-id="7b5bf-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="7b5bf-115">這個命令會傳回指定資源群組中的所有主機群組。</span><span class="sxs-lookup"><span data-stu-id="7b5bf-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="7b5bf-116">範例3</span><span class="sxs-lookup"><span data-stu-id="7b5bf-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="7b5bf-117">這個命令會傳回訂閱中的所有主機群組。</span><span class="sxs-lookup"><span data-stu-id="7b5bf-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="7b5bf-118">參數</span><span class="sxs-lookup"><span data-stu-id="7b5bf-118">PARAMETERS</span></span>

### <span data-ttu-id="7b5bf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b5bf-119">-DefaultProfile</span></span>
<span data-ttu-id="7b5bf-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b5bf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b5bf-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="7b5bf-121">-Name</span></span>
<span data-ttu-id="7b5bf-122">主機群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b5bf-122">The name of the host group.</span></span>

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

### <span data-ttu-id="7b5bf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b5bf-123">-ResourceGroupName</span></span>
<span data-ttu-id="7b5bf-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b5bf-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="7b5bf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b5bf-125">-ResourceId</span></span>
<span data-ttu-id="7b5bf-126">資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7b5bf-126">The ID of the resource.</span></span>

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

### <span data-ttu-id="7b5bf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b5bf-127">CommonParameters</span></span>
<span data-ttu-id="7b5bf-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b5bf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b5bf-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7b5bf-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b5bf-130">輸入</span><span class="sxs-lookup"><span data-stu-id="7b5bf-130">INPUTS</span></span>

### <span data-ttu-id="7b5bf-131">System.object</span><span class="sxs-lookup"><span data-stu-id="7b5bf-131">System.String</span></span>

## <span data-ttu-id="7b5bf-132">輸出</span><span class="sxs-lookup"><span data-stu-id="7b5bf-132">OUTPUTS</span></span>

### <span data-ttu-id="7b5bf-133">PSHostGroup 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="7b5bf-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="7b5bf-134">筆記</span><span class="sxs-lookup"><span data-stu-id="7b5bf-134">NOTES</span></span>

## <span data-ttu-id="7b5bf-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b5bf-135">RELATED LINKS</span></span>

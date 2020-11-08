---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: ef984a1cbb1cf922ddc931a7924a5d39ba6c6a0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138980"
---
# <span data-ttu-id="32e5b-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="32e5b-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="32e5b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32e5b-102">SYNOPSIS</span></span>
<span data-ttu-id="32e5b-103">取得訂閱上的安全拓撲清單</span><span class="sxs-lookup"><span data-stu-id="32e5b-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="32e5b-104">句法</span><span class="sxs-lookup"><span data-stu-id="32e5b-104">SYNTAX</span></span>

### <span data-ttu-id="32e5b-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="32e5b-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32e5b-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="32e5b-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32e5b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="32e5b-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32e5b-108">說明</span><span class="sxs-lookup"><span data-stu-id="32e5b-108">DESCRIPTION</span></span>
<span data-ttu-id="32e5b-109">安全拓撲是由 Azure 安全中心自動探索，使用此 Cmdlet 來查看安全拓撲。</span><span class="sxs-lookup"><span data-stu-id="32e5b-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="32e5b-110">示例</span><span class="sxs-lookup"><span data-stu-id="32e5b-110">EXAMPLES</span></span>

### <span data-ttu-id="32e5b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="32e5b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="32e5b-112">在訂閱中查看所有安全拓撲</span><span class="sxs-lookup"><span data-stu-id="32e5b-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="32e5b-113">範例2</span><span class="sxs-lookup"><span data-stu-id="32e5b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="32e5b-114">取得特定的安全性拓撲</span><span class="sxs-lookup"><span data-stu-id="32e5b-114">Get a specific security topologies</span></span>

## <span data-ttu-id="32e5b-115">參數</span><span class="sxs-lookup"><span data-stu-id="32e5b-115">PARAMETERS</span></span>

### <span data-ttu-id="32e5b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32e5b-116">-DefaultProfile</span></span>
<span data-ttu-id="32e5b-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="32e5b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32e5b-118">-位置</span><span class="sxs-lookup"><span data-stu-id="32e5b-118">-Location</span></span>
<span data-ttu-id="32e5b-119">位於.</span><span class="sxs-lookup"><span data-stu-id="32e5b-119">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32e5b-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="32e5b-120">-Name</span></span>
<span data-ttu-id="32e5b-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="32e5b-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32e5b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32e5b-122">-ResourceGroupName</span></span>
<span data-ttu-id="32e5b-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="32e5b-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32e5b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32e5b-124">-ResourceId</span></span>
<span data-ttu-id="32e5b-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="32e5b-125">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32e5b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e5b-126">CommonParameters</span></span>
<span data-ttu-id="32e5b-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32e5b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e5b-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="32e5b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e5b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="32e5b-129">INPUTS</span></span>

### <span data-ttu-id="32e5b-130">System.object</span><span class="sxs-lookup"><span data-stu-id="32e5b-130">System.String</span></span>

## <span data-ttu-id="32e5b-131">輸出</span><span class="sxs-lookup"><span data-stu-id="32e5b-131">OUTPUTS</span></span>

### <span data-ttu-id="32e5b-132">PSSecurityTopologies （Security..。</span><span class="sxs-lookup"><span data-stu-id="32e5b-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="32e5b-133">筆記</span><span class="sxs-lookup"><span data-stu-id="32e5b-133">NOTES</span></span>

## <span data-ttu-id="32e5b-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="32e5b-134">RELATED LINKS</span></span>

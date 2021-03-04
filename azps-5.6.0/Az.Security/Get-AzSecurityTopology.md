---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: 0f6cbe88eaabb49a07bb0704f0d6ea547449a229
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911838"
---
# <span data-ttu-id="f23e9-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="f23e9-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="f23e9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f23e9-102">SYNOPSIS</span></span>
<span data-ttu-id="f23e9-103">在訂閱上獲得安全性拓撲清單</span><span class="sxs-lookup"><span data-stu-id="f23e9-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="f23e9-104">語法</span><span class="sxs-lookup"><span data-stu-id="f23e9-104">SYNTAX</span></span>

### <span data-ttu-id="f23e9-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="f23e9-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f23e9-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="f23e9-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f23e9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f23e9-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f23e9-108">描述</span><span class="sxs-lookup"><span data-stu-id="f23e9-108">DESCRIPTION</span></span>
<span data-ttu-id="f23e9-109">Azure 資訊安全中心會自動探索安全性拓撲，請使用此 Cmdlet 來查看安全性拓撲。</span><span class="sxs-lookup"><span data-stu-id="f23e9-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="f23e9-110">例子</span><span class="sxs-lookup"><span data-stu-id="f23e9-110">EXAMPLES</span></span>

### <span data-ttu-id="f23e9-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f23e9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="f23e9-112">在訂閱中查看所有安全性拓撲</span><span class="sxs-lookup"><span data-stu-id="f23e9-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="f23e9-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="f23e9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="f23e9-114">取得特定的安全性拓撲</span><span class="sxs-lookup"><span data-stu-id="f23e9-114">Get a specific security topologies</span></span>

## <span data-ttu-id="f23e9-115">參數</span><span class="sxs-lookup"><span data-stu-id="f23e9-115">PARAMETERS</span></span>

### <span data-ttu-id="f23e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f23e9-116">-DefaultProfile</span></span>
<span data-ttu-id="f23e9-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f23e9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f23e9-118">-位置</span><span class="sxs-lookup"><span data-stu-id="f23e9-118">-Location</span></span>
<span data-ttu-id="f23e9-119">位置。</span><span class="sxs-lookup"><span data-stu-id="f23e9-119">Location.</span></span>

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

### <span data-ttu-id="f23e9-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f23e9-120">-Name</span></span>
<span data-ttu-id="f23e9-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f23e9-121">Resource name.</span></span>

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

### <span data-ttu-id="f23e9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f23e9-122">-ResourceGroupName</span></span>
<span data-ttu-id="f23e9-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f23e9-123">Resource group name.</span></span>

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

### <span data-ttu-id="f23e9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f23e9-124">-ResourceId</span></span>
<span data-ttu-id="f23e9-125">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f23e9-125">Resource ID.</span></span>

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

### <span data-ttu-id="f23e9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f23e9-126">CommonParameters</span></span>
<span data-ttu-id="f23e9-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f23e9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f23e9-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f23e9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f23e9-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f23e9-129">INPUTS</span></span>

### <span data-ttu-id="f23e9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f23e9-130">System.String</span></span>

## <span data-ttu-id="f23e9-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f23e9-131">OUTPUTS</span></span>

### <span data-ttu-id="f23e9-132">Microsoft.Azure.Commands.Security.models.拓撲.PSSecurityTopologies</span><span class="sxs-lookup"><span data-stu-id="f23e9-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="f23e9-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f23e9-133">NOTES</span></span>

## <span data-ttu-id="f23e9-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f23e9-134">RELATED LINKS</span></span>

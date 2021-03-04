---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: 52b6a4b7c5f78359ffc046953101aaa01bb7a435
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912745"
---
# <span data-ttu-id="78acd-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78acd-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="78acd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="78acd-102">SYNOPSIS</span></span>
<span data-ttu-id="78acd-103">獲得應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="78acd-103">Gets an application security group.</span></span>

## <span data-ttu-id="78acd-104">語法</span><span class="sxs-lookup"><span data-stu-id="78acd-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78acd-105">描述</span><span class="sxs-lookup"><span data-stu-id="78acd-105">DESCRIPTION</span></span>
<span data-ttu-id="78acd-106">**Get-AzApplicationSecurityGroup** Cmdlet 會取得應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="78acd-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="78acd-107">例子</span><span class="sxs-lookup"><span data-stu-id="78acd-107">EXAMPLES</span></span>

### <span data-ttu-id="78acd-108">範例 1：取回所有應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="78acd-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="78acd-109">上述命令會返回訂閱中所有的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="78acd-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="78acd-110">範例 2：在資源群組中取回應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="78acd-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="78acd-111">上述命令會返回屬於資源群組 MyResourceGroup 的所有應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="78acd-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="78acd-112">範例 3：取回特定的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="78acd-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1
```

<span data-ttu-id="78acd-113">上述命令會返回資源群組 MyResourceGroup 下的應用程式安全性群組 MyApplicationSecurityGroup。</span><span class="sxs-lookup"><span data-stu-id="78acd-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="78acd-114">範例 4：使用篩選來取回應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="78acd-114">Example 4: Retrieve application security groups using filtering.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -Name MyApplicationSecurityGroup*

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="78acd-115">上述命令會返回以「MyApplicationSecurityGroup」為起始的所有應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="78acd-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="78acd-116">參數</span><span class="sxs-lookup"><span data-stu-id="78acd-116">PARAMETERS</span></span>

### <span data-ttu-id="78acd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78acd-117">-DefaultProfile</span></span>
<span data-ttu-id="78acd-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="78acd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78acd-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="78acd-119">-Name</span></span>
<span data-ttu-id="78acd-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="78acd-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="78acd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78acd-121">-ResourceGroupName</span></span>
<span data-ttu-id="78acd-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="78acd-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="78acd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78acd-123">CommonParameters</span></span>
<span data-ttu-id="78acd-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="78acd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78acd-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78acd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78acd-126">輸入</span><span class="sxs-lookup"><span data-stu-id="78acd-126">INPUTS</span></span>

### <span data-ttu-id="78acd-127">System.String</span><span class="sxs-lookup"><span data-stu-id="78acd-127">System.String</span></span>

## <span data-ttu-id="78acd-128">輸出</span><span class="sxs-lookup"><span data-stu-id="78acd-128">OUTPUTS</span></span>

### <span data-ttu-id="78acd-129">Microsoft.Azure.Commands.Network.models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78acd-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="78acd-130">筆記</span><span class="sxs-lookup"><span data-stu-id="78acd-130">NOTES</span></span>

## <span data-ttu-id="78acd-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="78acd-131">RELATED LINKS</span></span>

[<span data-ttu-id="78acd-132">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78acd-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="78acd-133">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78acd-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="78acd-134">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="78acd-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="78acd-135">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="78acd-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

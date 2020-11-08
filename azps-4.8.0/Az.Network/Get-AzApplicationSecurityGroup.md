---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: aa03f7d410d704e8e5b9ea4b974e3050a3304342
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126540"
---
# <span data-ttu-id="d245d-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d245d-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="d245d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d245d-102">SYNOPSIS</span></span>
<span data-ttu-id="d245d-103">取得應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d245d-103">Gets an application security group.</span></span>

## <span data-ttu-id="d245d-104">句法</span><span class="sxs-lookup"><span data-stu-id="d245d-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d245d-105">說明</span><span class="sxs-lookup"><span data-stu-id="d245d-105">DESCRIPTION</span></span>
<span data-ttu-id="d245d-106">**AzApplicationSecurityGroup** Cmdlet 會取得應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d245d-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="d245d-107">示例</span><span class="sxs-lookup"><span data-stu-id="d245d-107">EXAMPLES</span></span>

### <span data-ttu-id="d245d-108">範例1：檢索所有應用程式的安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d245d-108">Example 1: Retrieve all application security groups.</span></span>
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

<span data-ttu-id="d245d-109">上述命令會傳回訂閱中的所有應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d245d-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="d245d-110">範例2：在資源群組中取得應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d245d-110">Example 2: Retrieve application security groups in a resource group.</span></span>
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

<span data-ttu-id="d245d-111">上述命令會傳回屬於資源群組 MyResourceGroup 的所有應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d245d-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="d245d-112">範例3：檢索特定的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d245d-112">Example 3: Retrieve a specific application security group.</span></span>
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

<span data-ttu-id="d245d-113">上述命令會傳回 [資源] 群組 MyResourceGroup 底下的 [應用程式安全性群組 MyApplicationSecurityGroup]。</span><span class="sxs-lookup"><span data-stu-id="d245d-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="d245d-114">範例4：使用篩選來取得應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d245d-114">Example 4: Retrieve application security groups using filtering.</span></span>
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

<span data-ttu-id="d245d-115">上述命令會傳回所有以 "MyApplicationSecurityGroup" 為開頭的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d245d-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="d245d-116">參數</span><span class="sxs-lookup"><span data-stu-id="d245d-116">PARAMETERS</span></span>

### <span data-ttu-id="d245d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d245d-117">-DefaultProfile</span></span>
<span data-ttu-id="d245d-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d245d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d245d-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d245d-119">-Name</span></span>
<span data-ttu-id="d245d-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d245d-120">The resource name.</span></span>

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

### <span data-ttu-id="d245d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d245d-121">-ResourceGroupName</span></span>
<span data-ttu-id="d245d-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d245d-122">The resource group name.</span></span>

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

### <span data-ttu-id="d245d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d245d-123">CommonParameters</span></span>
<span data-ttu-id="d245d-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d245d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d245d-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d245d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d245d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="d245d-126">INPUTS</span></span>

### <span data-ttu-id="d245d-127">System.object</span><span class="sxs-lookup"><span data-stu-id="d245d-127">System.String</span></span>

## <span data-ttu-id="d245d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="d245d-128">OUTPUTS</span></span>

### <span data-ttu-id="d245d-129">PSApplicationSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d245d-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="d245d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="d245d-130">NOTES</span></span>

## <span data-ttu-id="d245d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="d245d-131">RELATED LINKS</span></span>

[<span data-ttu-id="d245d-132">新-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d245d-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="d245d-133">移除-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d245d-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="d245d-134">AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d245d-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="d245d-135">AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d245d-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

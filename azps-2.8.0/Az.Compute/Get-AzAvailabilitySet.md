---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: 63eba52ec3b2c383a9f2e1047e7b39a828e1dd04
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613430"
---
# <span data-ttu-id="ecf1f-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ecf1f-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="ecf1f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ecf1f-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf1f-103">取得資源群組中的 Azure 可用性集合。</span><span class="sxs-lookup"><span data-stu-id="ecf1f-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="ecf1f-104">句法</span><span class="sxs-lookup"><span data-stu-id="ecf1f-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecf1f-105">說明</span><span class="sxs-lookup"><span data-stu-id="ecf1f-105">DESCRIPTION</span></span>
<span data-ttu-id="ecf1f-106">**AzAvailabilitySet** Cmdlet 可在資源群組中取得 Azure 可用性集。</span><span class="sxs-lookup"><span data-stu-id="ecf1f-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="ecf1f-107">您可以指定要取得的特定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecf1f-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="ecf1f-108">示例</span><span class="sxs-lookup"><span data-stu-id="ecf1f-108">EXAMPLES</span></span>

### <span data-ttu-id="ecf1f-109">範例1：取得特定的可用性集</span><span class="sxs-lookup"><span data-stu-id="ecf1f-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="ecf1f-110">這個命令會在名為 ResourceGroup11 的資源群組中取得名為 AvailabilitySet03 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="ecf1f-110">This command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="ecf1f-111">範例2：取得所有的可用性集</span><span class="sxs-lookup"><span data-stu-id="ecf1f-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet10
Name                      : AvailabilitySet10
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="ecf1f-112">這個命令會在名為 ResourceGroup11 的資源群組中取得所有的可用性集。</span><span class="sxs-lookup"><span data-stu-id="ecf1f-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="ecf1f-113">範例3：使用篩選取得所有的可用性集</span><span class="sxs-lookup"><span data-stu-id="ecf1f-113">Example 3: Get all availability sets with filtering</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup1*" -Name "AvailabilitySet0*"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="ecf1f-114">這個命令會在名為 ResourceGroup11 的資源群組中，取得以 "AvailabilitySet0" 開頭的所有可用性集。</span><span class="sxs-lookup"><span data-stu-id="ecf1f-114">This command gets all the availability sets in the resource group named ResourceGroup11 that start with "AvailabilitySet0".</span></span>

### <span data-ttu-id="ecf1f-115">範例4：從 AvailabilitySet0 開始取得名稱的所有可用性集</span><span class="sxs-lookup"><span data-stu-id="ecf1f-115">Example 4: Get all availability sets with name starting with AvailabilitySet0</span></span>
```
PS C:\> Get-AzAvailabilitySet -Name AvailabilitySet0*

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup12
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup12/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="ecf1f-116">這個命令會取得所有以 "AvailabilitySet0" 開頭的可用性集。</span><span class="sxs-lookup"><span data-stu-id="ecf1f-116">This command gets all the availability sets that start with "AvailabilitySet0".</span></span>

## <span data-ttu-id="ecf1f-117">參數</span><span class="sxs-lookup"><span data-stu-id="ecf1f-117">PARAMETERS</span></span>

### <span data-ttu-id="ecf1f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf1f-118">-DefaultProfile</span></span>
<span data-ttu-id="ecf1f-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ecf1f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecf1f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ecf1f-120">-Name</span></span>
<span data-ttu-id="ecf1f-121">指定此 Cmdlet 所取得之可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecf1f-121">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ecf1f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf1f-122">-ResourceGroupName</span></span>
<span data-ttu-id="ecf1f-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecf1f-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ecf1f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf1f-124">CommonParameters</span></span>
<span data-ttu-id="ecf1f-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ecf1f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf1f-126">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ecf1f-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf1f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ecf1f-127">INPUTS</span></span>

### <span data-ttu-id="ecf1f-128">System.object</span><span class="sxs-lookup"><span data-stu-id="ecf1f-128">System.String</span></span>

## <span data-ttu-id="ecf1f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="ecf1f-129">OUTPUTS</span></span>

### <span data-ttu-id="ecf1f-130">PSAvailabilitySet 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="ecf1f-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="ecf1f-131">筆記</span><span class="sxs-lookup"><span data-stu-id="ecf1f-131">NOTES</span></span>

## <span data-ttu-id="ecf1f-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="ecf1f-132">RELATED LINKS</span></span>

[<span data-ttu-id="ecf1f-133">新-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ecf1f-133">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="ecf1f-134">移除-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ecf1f-134">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)



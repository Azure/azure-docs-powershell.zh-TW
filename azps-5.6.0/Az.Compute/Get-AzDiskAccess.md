---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
ms.openlocfilehash: 69f83b7c98850ba74476e6d81803e748f48bea6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906261"
---
# <span data-ttu-id="12c04-101">Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="12c04-101">Get-AzDiskAccess</span></span>

## <span data-ttu-id="12c04-102">簡介</span><span class="sxs-lookup"><span data-stu-id="12c04-102">SYNOPSIS</span></span>
<span data-ttu-id="12c04-103">取得磁片存取的屬性</span><span class="sxs-lookup"><span data-stu-id="12c04-103">Gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="12c04-104">語法</span><span class="sxs-lookup"><span data-stu-id="12c04-104">SYNTAX</span></span>

### <span data-ttu-id="12c04-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="12c04-105">DefaultParameterSet (Default)</span></span>
```
Get-AzDiskAccess [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12c04-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="12c04-106">ResourceIDParameterSet</span></span>
```
Get-AzDiskAccess [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12c04-107">描述</span><span class="sxs-lookup"><span data-stu-id="12c04-107">DESCRIPTION</span></span>
<span data-ttu-id="12c04-108">**Get-Az與Access** Cmdlet 取得磁片存取的屬性</span><span class="sxs-lookup"><span data-stu-id="12c04-108">The **Get-AzDiskAccess** cmdlet gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="12c04-109">例子</span><span class="sxs-lookup"><span data-stu-id="12c04-109">EXAMPLES</span></span>

### <span data-ttu-id="12c04-110">範例 1：使用預設參數集</span><span class="sxs-lookup"><span data-stu-id="12c04-110">Example 1: Using Default Parameter Set</span></span> 
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -Name 'DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="12c04-111">此命令會取得資源群組 'ResourceGroup01' 中名為 'DiskAccess01' 的磁片存取資源屬性。</span><span class="sxs-lookup"><span data-stu-id="12c04-111">This command gets the properties of a Disk Access resource named 'DiskAccess01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="12c04-112">範例 2：Get-AzDiskAccess資源群組</span><span class="sxs-lookup"><span data-stu-id="12c04-112">Example 2: Get-AzDiskAccess by Resource Group</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="12c04-113">此命令會取得資源群組 "ResourceGroup01" 中所有磁片存取的屬性。</span><span class="sxs-lookup"><span data-stu-id="12c04-113">This command gets the properties of all disk accesses in the resource group 'ResourceGroup01'.</span></span>


### <span data-ttu-id="12c04-114">範例 3：取得所有磁片存取</span><span class="sxs-lookup"><span data-stu-id="12c04-114">Example 3: Getting all Disk Access</span></span>
```
PS C:\> Get-AzDiskAccess

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup21/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup08/providers/Microsoft.Compute/diskAccesses/DiskAccess03
Name                       : DiskAccess03
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="12c04-115">此命令會取得訂閱下所有磁片存取的屬性。</span><span class="sxs-lookup"><span data-stu-id="12c04-115">This command gets the properties of all disk accesses under the subscription.</span></span>

### <span data-ttu-id="12c04-116">範例 4：使用萬用字元取得所有磁片存取</span><span class="sxs-lookup"><span data-stu-id="12c04-116">Example 4: Get all Disk Access using Wildcard Character</span></span>
```
PS C:\> Get-AzDiskAccess -Name DiskAccessMicrosoft*

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftAzure
Name                       : DiskAccessMicrosoftAzure
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftTeams
Name                       : DiskAccessMicrosoftTeams
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="12c04-117">此命令會從 'DiskAccessMicrosoft'開始，取得訂閱名稱下所有磁片存取的屬性。</span><span class="sxs-lookup"><span data-stu-id="12c04-117">This command gets the properties of all disk accesses under the subscription name starting with 'DiskAccessMicrosoft'.</span></span>

### <span data-ttu-id="12c04-118">範例 5：使用 ResourceId 取得磁片存取。</span><span class="sxs-lookup"><span data-stu-id="12c04-118">Example 5: Get Disk Access using ResourceId.</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceId '/subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="12c04-119">此命令會取得具有指定 ResourceId 的磁片存取屬性。</span><span class="sxs-lookup"><span data-stu-id="12c04-119">This command gets the properties of a Disk Access with the given ResourceId.</span></span>


## <span data-ttu-id="12c04-120">參數</span><span class="sxs-lookup"><span data-stu-id="12c04-120">PARAMETERS</span></span>

### <span data-ttu-id="12c04-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12c04-121">-DefaultProfile</span></span>
<span data-ttu-id="12c04-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="12c04-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12c04-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="12c04-123">-Name</span></span>
<span data-ttu-id="12c04-124">指定磁片存取的名稱。</span><span class="sxs-lookup"><span data-stu-id="12c04-124">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: diskAccessName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="12c04-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12c04-125">-ResourceGroupName</span></span>
<span data-ttu-id="12c04-126">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="12c04-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="12c04-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12c04-127">-ResourceId</span></span>
<span data-ttu-id="12c04-128">您磁片存取的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="12c04-128">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12c04-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c04-129">CommonParameters</span></span>
<span data-ttu-id="12c04-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="12c04-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12c04-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12c04-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c04-132">輸入</span><span class="sxs-lookup"><span data-stu-id="12c04-132">INPUTS</span></span>

### <span data-ttu-id="12c04-133">System.String</span><span class="sxs-lookup"><span data-stu-id="12c04-133">System.String</span></span>

## <span data-ttu-id="12c04-134">輸出</span><span class="sxs-lookup"><span data-stu-id="12c04-134">OUTPUTS</span></span>

### <span data-ttu-id="12c04-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="12c04-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="12c04-136">筆記</span><span class="sxs-lookup"><span data-stu-id="12c04-136">NOTES</span></span>

## <span data-ttu-id="12c04-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="12c04-137">RELATED LINKS</span></span>

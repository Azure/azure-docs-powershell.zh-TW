---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
ms.openlocfilehash: 69f83b7c98850ba74476e6d81803e748f48bea6a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449874"
---
# <span data-ttu-id="ba9fa-101">Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ba9fa-101">Get-AzDiskAccess</span></span>

## <span data-ttu-id="ba9fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba9fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ba9fa-103">取得磁片存取的屬性</span><span class="sxs-lookup"><span data-stu-id="ba9fa-103">Gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="ba9fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba9fa-104">SYNTAX</span></span>

### <span data-ttu-id="ba9fa-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ba9fa-105">DefaultParameterSet (Default)</span></span>
```
Get-AzDiskAccess [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba9fa-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba9fa-106">ResourceIDParameterSet</span></span>
```
Get-AzDiskAccess [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba9fa-107">說明</span><span class="sxs-lookup"><span data-stu-id="ba9fa-107">DESCRIPTION</span></span>
<span data-ttu-id="ba9fa-108">**AzDiskAccess** Cmdlet 會取得磁片存取的屬性</span><span class="sxs-lookup"><span data-stu-id="ba9fa-108">The **Get-AzDiskAccess** cmdlet gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="ba9fa-109">示例</span><span class="sxs-lookup"><span data-stu-id="ba9fa-109">EXAMPLES</span></span>

### <span data-ttu-id="ba9fa-110">範例1：使用預設參數集</span><span class="sxs-lookup"><span data-stu-id="ba9fa-110">Example 1: Using Default Parameter Set</span></span> 
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

<span data-ttu-id="ba9fa-111">這個命令會取得資源群組 ' ResourceGroup01 ' 中名為「DiskAccess01」的磁片存取資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="ba9fa-111">This command gets the properties of a Disk Access resource named 'DiskAccess01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ba9fa-112">範例2：依資源群組 Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ba9fa-112">Example 2: Get-AzDiskAccess by Resource Group</span></span>
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

<span data-ttu-id="ba9fa-113">這個命令會取得資源群組 ' ResourceGroup01」中所有磁片存取的屬性。</span><span class="sxs-lookup"><span data-stu-id="ba9fa-113">This command gets the properties of all disk accesses in the resource group 'ResourceGroup01'.</span></span>


### <span data-ttu-id="ba9fa-114">範例3：取得所有磁片存取權</span><span class="sxs-lookup"><span data-stu-id="ba9fa-114">Example 3: Getting all Disk Access</span></span>
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

<span data-ttu-id="ba9fa-115">這個命令會取得訂閱下所有磁片存取的屬性。</span><span class="sxs-lookup"><span data-stu-id="ba9fa-115">This command gets the properties of all disk accesses under the subscription.</span></span>

### <span data-ttu-id="ba9fa-116">範例4：使用萬用字元取得所有磁片存取權</span><span class="sxs-lookup"><span data-stu-id="ba9fa-116">Example 4: Get all Disk Access using Wildcard Character</span></span>
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

<span data-ttu-id="ba9fa-117">這個命令會取得以「DiskAccessMicrosoft」開頭的訂閱名稱底下所有磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="ba9fa-117">This command gets the properties of all disk accesses under the subscription name starting with 'DiskAccessMicrosoft'.</span></span>

### <span data-ttu-id="ba9fa-118">範例5：使用 ResourceId 取得磁片存取權。</span><span class="sxs-lookup"><span data-stu-id="ba9fa-118">Example 5: Get Disk Access using ResourceId.</span></span>
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

<span data-ttu-id="ba9fa-119">這個命令會取得擁有指定 ResourceId 的磁片訪問屬性。</span><span class="sxs-lookup"><span data-stu-id="ba9fa-119">This command gets the properties of a Disk Access with the given ResourceId.</span></span>


## <span data-ttu-id="ba9fa-120">參數</span><span class="sxs-lookup"><span data-stu-id="ba9fa-120">PARAMETERS</span></span>

### <span data-ttu-id="ba9fa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba9fa-121">-DefaultProfile</span></span>
<span data-ttu-id="ba9fa-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba9fa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba9fa-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="ba9fa-123">-Name</span></span>
<span data-ttu-id="ba9fa-124">指定磁片存取的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba9fa-124">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="ba9fa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba9fa-125">-ResourceGroupName</span></span>
<span data-ttu-id="ba9fa-126">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba9fa-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ba9fa-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba9fa-127">-ResourceId</span></span>
<span data-ttu-id="ba9fa-128">您的磁片存取資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ba9fa-128">Resource ID for your disk access.</span></span>

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

### <span data-ttu-id="ba9fa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba9fa-129">CommonParameters</span></span>
<span data-ttu-id="ba9fa-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba9fa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba9fa-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ba9fa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba9fa-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fa-132">INPUTS</span></span>

### <span data-ttu-id="ba9fa-133">System.object</span><span class="sxs-lookup"><span data-stu-id="ba9fa-133">System.String</span></span>

## <span data-ttu-id="ba9fa-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fa-134">OUTPUTS</span></span>

### <span data-ttu-id="ba9fa-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ba9fa-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="ba9fa-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ba9fa-136">NOTES</span></span>

## <span data-ttu-id="ba9fa-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba9fa-137">RELATED LINKS</span></span>

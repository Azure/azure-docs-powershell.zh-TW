---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
ms.openlocfilehash: 6122bd17828b07e47f41c3f2d087f88d468ca6be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906237"
---
# <span data-ttu-id="14222-101">Get-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="14222-101">Get-AzGalleryImageVersion</span></span>

## <span data-ttu-id="14222-102">簡介</span><span class="sxs-lookup"><span data-stu-id="14222-102">SYNOPSIS</span></span>
<span data-ttu-id="14222-103">取得或列出圖庫圖像版本。</span><span class="sxs-lookup"><span data-stu-id="14222-103">Get or list gallery image versions.</span></span>

## <span data-ttu-id="14222-104">語法</span><span class="sxs-lookup"><span data-stu-id="14222-104">SYNTAX</span></span>

### <span data-ttu-id="14222-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="14222-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14222-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="14222-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14222-107">描述</span><span class="sxs-lookup"><span data-stu-id="14222-107">DESCRIPTION</span></span>
<span data-ttu-id="14222-108">取得或列出圖庫圖像版本。</span><span class="sxs-lookup"><span data-stu-id="14222-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="14222-109">例子</span><span class="sxs-lookup"><span data-stu-id="14222-109">EXAMPLES</span></span>

### <span data-ttu-id="14222-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="14222-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1 -GalleryImageVersionName 1.0.0

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="14222-111">取得圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="14222-111">Get the gallery image version.</span></span>

### <span data-ttu-id="14222-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="14222-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1 -GalleryImageVersionName 1*

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="14222-113">取得以「1」開頭的圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="14222-113">Get the gallery image versions that starts with "1".</span></span>

### <span data-ttu-id="14222-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="14222-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="14222-115">取得所有圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="14222-115">Get all gallery image versions.</span></span>

## <span data-ttu-id="14222-116">參數</span><span class="sxs-lookup"><span data-stu-id="14222-116">PARAMETERS</span></span>

### <span data-ttu-id="14222-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14222-117">-DefaultProfile</span></span>
<span data-ttu-id="14222-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="14222-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14222-119">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="14222-119">-ExpandReplicationStatus</span></span>
<span data-ttu-id="14222-120">顯示覆制狀態。</span><span class="sxs-lookup"><span data-stu-id="14222-120">Show replication status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14222-121">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="14222-121">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="14222-122">圖庫圖像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="14222-122">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14222-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="14222-123">-GalleryName</span></span>
<span data-ttu-id="14222-124">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="14222-124">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14222-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="14222-125">-Name</span></span>
<span data-ttu-id="14222-126">圖庫圖像版本的名稱。</span><span class="sxs-lookup"><span data-stu-id="14222-126">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="14222-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14222-127">-ResourceGroupName</span></span>
<span data-ttu-id="14222-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="14222-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14222-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14222-129">-ResourceId</span></span>
<span data-ttu-id="14222-130">圖庫圖像版本的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="14222-130">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="14222-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14222-131">CommonParameters</span></span>
<span data-ttu-id="14222-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="14222-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14222-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14222-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14222-134">輸入</span><span class="sxs-lookup"><span data-stu-id="14222-134">INPUTS</span></span>

### <span data-ttu-id="14222-135">System.String</span><span class="sxs-lookup"><span data-stu-id="14222-135">System.String</span></span>

### <span data-ttu-id="14222-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="14222-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="14222-137">輸出</span><span class="sxs-lookup"><span data-stu-id="14222-137">OUTPUTS</span></span>

### <span data-ttu-id="14222-138">Microsoft.Azure.Commands.Compute.Automation.models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="14222-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="14222-139">筆記</span><span class="sxs-lookup"><span data-stu-id="14222-139">NOTES</span></span>

## <span data-ttu-id="14222-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="14222-140">RELATED LINKS</span></span>

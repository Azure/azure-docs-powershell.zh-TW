---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
ms.openlocfilehash: cd09679117a964cc28e24d28f4097d511304a9a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788537"
---
# <span data-ttu-id="0ce36-101">Get-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0ce36-101">Get-AzGalleryImageVersion</span></span>

## <span data-ttu-id="0ce36-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0ce36-102">SYNOPSIS</span></span>
<span data-ttu-id="0ce36-103">[取得] 或 [清單庫] 影像版本。</span><span class="sxs-lookup"><span data-stu-id="0ce36-103">Get or list gallery image versions.</span></span>

## <span data-ttu-id="0ce36-104">句法</span><span class="sxs-lookup"><span data-stu-id="0ce36-104">SYNTAX</span></span>

### <span data-ttu-id="0ce36-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="0ce36-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ce36-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="0ce36-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ce36-107">說明</span><span class="sxs-lookup"><span data-stu-id="0ce36-107">DESCRIPTION</span></span>
<span data-ttu-id="0ce36-108">[取得] 或 [清單庫] 影像版本。</span><span class="sxs-lookup"><span data-stu-id="0ce36-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="0ce36-109">示例</span><span class="sxs-lookup"><span data-stu-id="0ce36-109">EXAMPLES</span></span>

### <span data-ttu-id="0ce36-110">範例1</span><span class="sxs-lookup"><span data-stu-id="0ce36-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -ImageDefinitionName image1 -GalleryImageVersionName 1.0.0

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

<span data-ttu-id="0ce36-111">取得圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="0ce36-111">Get the gallery image version.</span></span>

### <span data-ttu-id="0ce36-112">範例2</span><span class="sxs-lookup"><span data-stu-id="0ce36-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -ImageDefinitionName image1 -GalleryImageVersionName 1*

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

<span data-ttu-id="0ce36-113">取得以 "1" 開頭的圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="0ce36-113">Get the gallery image versions that starts with "1".</span></span>

### <span data-ttu-id="0ce36-114">範例3</span><span class="sxs-lookup"><span data-stu-id="0ce36-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -ImageDefinitionName image1

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

<span data-ttu-id="0ce36-115">取得所有圖庫影像版本。</span><span class="sxs-lookup"><span data-stu-id="0ce36-115">Get all gallery image versions.</span></span>

## <span data-ttu-id="0ce36-116">參數</span><span class="sxs-lookup"><span data-stu-id="0ce36-116">PARAMETERS</span></span>

### <span data-ttu-id="0ce36-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce36-117">-DefaultProfile</span></span>
<span data-ttu-id="0ce36-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0ce36-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ce36-119">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="0ce36-119">-ExpandReplicationStatus</span></span>
<span data-ttu-id="0ce36-120">顯示覆制狀態。</span><span class="sxs-lookup"><span data-stu-id="0ce36-120">Show replication status.</span></span>

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

### <span data-ttu-id="0ce36-121">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0ce36-121">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="0ce36-122">圖庫影像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ce36-122">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="0ce36-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="0ce36-123">-GalleryName</span></span>
<span data-ttu-id="0ce36-124">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ce36-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="0ce36-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="0ce36-125">-Name</span></span>
<span data-ttu-id="0ce36-126">圖庫影像版本的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ce36-126">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="0ce36-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ce36-127">-ResourceGroupName</span></span>
<span data-ttu-id="0ce36-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ce36-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="0ce36-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ce36-129">-ResourceId</span></span>
<span data-ttu-id="0ce36-130">畫廊影像版本的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0ce36-130">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="0ce36-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce36-131">CommonParameters</span></span>
<span data-ttu-id="0ce36-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0ce36-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce36-133">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0ce36-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce36-134">輸入</span><span class="sxs-lookup"><span data-stu-id="0ce36-134">INPUTS</span></span>

### <span data-ttu-id="0ce36-135">System.object</span><span class="sxs-lookup"><span data-stu-id="0ce36-135">System.String</span></span>

### <span data-ttu-id="0ce36-136">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="0ce36-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0ce36-137">輸出</span><span class="sxs-lookup"><span data-stu-id="0ce36-137">OUTPUTS</span></span>

### <span data-ttu-id="0ce36-138">PSGalleryImageVersion 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="0ce36-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="0ce36-139">筆記</span><span class="sxs-lookup"><span data-stu-id="0ce36-139">NOTES</span></span>

## <span data-ttu-id="0ce36-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ce36-140">RELATED LINKS</span></span>
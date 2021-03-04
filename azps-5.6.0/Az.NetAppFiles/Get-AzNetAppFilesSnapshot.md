---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 80d8a27aaf0d2aa27f9924d93669548c1d0dda93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906070"
---
# <span data-ttu-id="4cc4c-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="4cc4c-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="4cc4c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4cc4c-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc4c-103">在 ANF 快照中 (Azure NetApp 檔案) 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4cc4c-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="4cc4c-104">語法</span><span class="sxs-lookup"><span data-stu-id="4cc4c-104">SYNTAX</span></span>

### <span data-ttu-id="4cc4c-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4cc4c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cc4c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cc4c-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cc4c-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cc4c-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cc4c-108">描述</span><span class="sxs-lookup"><span data-stu-id="4cc4c-108">DESCRIPTION</span></span>
<span data-ttu-id="4cc4c-109">**Get-AzNetAppFilesSnapshot** Cmdlet 會取得 ANF 快照的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4cc4c-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="4cc4c-110">例子</span><span class="sxs-lookup"><span data-stu-id="4cc4c-110">EXAMPLES</span></span>

### <span data-ttu-id="4cc4c-111">範例 1：取得 ANF 快照</span><span class="sxs-lookup"><span data-stu-id="4cc4c-111">Example 1: Get an ANF snapshot</span></span>
```
PS C:\>Get-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="4cc4c-112">此命令會從「MyAnfVolume」的音量中，獲得名為 MyAnfSnapshot 的快照。</span><span class="sxs-lookup"><span data-stu-id="4cc4c-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="4cc4c-113">參數</span><span class="sxs-lookup"><span data-stu-id="4cc4c-113">PARAMETERS</span></span>

### <span data-ttu-id="4cc4c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4cc4c-114">-AccountName</span></span>
<span data-ttu-id="4cc4c-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="4cc4c-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc4c-116">-DefaultProfile</span></span>
<span data-ttu-id="4cc4c-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4cc4c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cc4c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="4cc4c-118">-Name</span></span>
<span data-ttu-id="4cc4c-119">ANF 快照的名稱</span><span class="sxs-lookup"><span data-stu-id="4cc4c-119">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc4c-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="4cc4c-120">-PoolName</span></span>
<span data-ttu-id="4cc4c-121">ANF 組名</span><span class="sxs-lookup"><span data-stu-id="4cc4c-121">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc4c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cc4c-122">-ResourceGroupName</span></span>
<span data-ttu-id="4cc4c-123">ANF 音量的資源群組</span><span class="sxs-lookup"><span data-stu-id="4cc4c-123">The resource group of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc4c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cc4c-124">-ResourceId</span></span>
<span data-ttu-id="4cc4c-125">ANF 快照的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="4cc4c-125">The resource id of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cc4c-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="4cc4c-126">-VolumeName</span></span>
<span data-ttu-id="4cc4c-127">ANF 音量的名稱</span><span class="sxs-lookup"><span data-stu-id="4cc4c-127">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc4c-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="4cc4c-128">-VolumeObject</span></span>
<span data-ttu-id="4cc4c-129">包含要返回之快照的卷積物件</span><span class="sxs-lookup"><span data-stu-id="4cc4c-129">The volume object containing the snapshot to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cc4c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc4c-130">CommonParameters</span></span>
<span data-ttu-id="4cc4c-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4cc4c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc4c-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4cc4c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc4c-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4cc4c-133">INPUTS</span></span>

### <span data-ttu-id="4cc4c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4cc4c-134">System.String</span></span>

### <span data-ttu-id="4cc4c-135">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="4cc4c-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="4cc4c-136">輸出</span><span class="sxs-lookup"><span data-stu-id="4cc4c-136">OUTPUTS</span></span>

### <span data-ttu-id="4cc4c-137">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="4cc4c-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="4cc4c-138">筆記</span><span class="sxs-lookup"><span data-stu-id="4cc4c-138">NOTES</span></span>

## <span data-ttu-id="4cc4c-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cc4c-139">RELATED LINKS</span></span>

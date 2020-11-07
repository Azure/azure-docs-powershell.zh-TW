---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 8f34145a65cde73ea1a5b925064c2b9a1d3f92a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790366"
---
# <span data-ttu-id="d2481-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="d2481-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="d2481-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2481-102">SYNOPSIS</span></span>
<span data-ttu-id="d2481-103">取得 (ANF) 快照的 Azure NetApp 檔案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d2481-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="d2481-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2481-104">SYNTAX</span></span>

### <span data-ttu-id="d2481-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d2481-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2481-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2481-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2481-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2481-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2481-108">說明</span><span class="sxs-lookup"><span data-stu-id="d2481-108">DESCRIPTION</span></span>
<span data-ttu-id="d2481-109">**AzNetAppFilesSnapshot** Cmdlet 會取得 ANF 快照的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d2481-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="d2481-110">示例</span><span class="sxs-lookup"><span data-stu-id="d2481-110">EXAMPLES</span></span>

### <span data-ttu-id="d2481-111">範例1：取得 ANF 快照</span><span class="sxs-lookup"><span data-stu-id="d2481-111">Example 1: Get an ANF snapshot</span></span>
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
CreationDate      :
ProvisioningState : Succeeded
```

<span data-ttu-id="d2481-112">這個命令會從 [MyAnfVolume] 卷中取得名為 MyAnfSnapshot 的快照。</span><span class="sxs-lookup"><span data-stu-id="d2481-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="d2481-113">參數</span><span class="sxs-lookup"><span data-stu-id="d2481-113">PARAMETERS</span></span>

### <span data-ttu-id="d2481-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d2481-114">-AccountName</span></span>
<span data-ttu-id="d2481-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="d2481-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2481-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2481-116">-DefaultProfile</span></span>
<span data-ttu-id="d2481-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2481-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2481-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2481-118">-Name</span></span>
<span data-ttu-id="d2481-119">ANF 快照的名稱</span><span class="sxs-lookup"><span data-stu-id="d2481-119">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2481-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d2481-120">-PoolName</span></span>
<span data-ttu-id="d2481-121">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="d2481-121">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2481-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2481-122">-ResourceGroupName</span></span>
<span data-ttu-id="d2481-123">ANF 體積中的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="d2481-123">The resource group of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2481-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2481-124">-ResourceId</span></span>
<span data-ttu-id="d2481-125">ANF 快照的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d2481-125">The resource id of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2481-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="d2481-126">-VolumeName</span></span>
<span data-ttu-id="d2481-127">ANF 體積的名稱</span><span class="sxs-lookup"><span data-stu-id="d2481-127">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2481-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="d2481-128">-VolumeObject</span></span>
<span data-ttu-id="d2481-129">包含要傳回之快照的 volume 物件</span><span class="sxs-lookup"><span data-stu-id="d2481-129">The volume object containing the snapshot to return</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2481-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2481-130">CommonParameters</span></span>
<span data-ttu-id="d2481-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2481-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d2481-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d2481-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2481-133">輸入</span><span class="sxs-lookup"><span data-stu-id="d2481-133">INPUTS</span></span>

### <span data-ttu-id="d2481-134">System.object</span><span class="sxs-lookup"><span data-stu-id="d2481-134">System.String</span></span>

### <span data-ttu-id="d2481-135">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="d2481-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d2481-136">輸出</span><span class="sxs-lookup"><span data-stu-id="d2481-136">OUTPUTS</span></span>

### <span data-ttu-id="d2481-137">PSNetAppFilesSnapshot 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="d2481-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="d2481-138">筆記</span><span class="sxs-lookup"><span data-stu-id="d2481-138">NOTES</span></span>

## <span data-ttu-id="d2481-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2481-139">RELATED LINKS</span></span>

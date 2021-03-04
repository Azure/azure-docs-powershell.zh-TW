---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: 73efd000f6889675c3daf9f99821640a8b6fbb99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906074"
---
# <span data-ttu-id="1af36-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="1af36-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="1af36-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1af36-102">SYNOPSIS</span></span>
<span data-ttu-id="1af36-103">取得複製的狀態</span><span class="sxs-lookup"><span data-stu-id="1af36-103">Get the status of the replication</span></span>

## <span data-ttu-id="1af36-104">語法</span><span class="sxs-lookup"><span data-stu-id="1af36-104">SYNTAX</span></span>

### <span data-ttu-id="1af36-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1af36-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1af36-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1af36-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1af36-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1af36-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1af36-108">描述</span><span class="sxs-lookup"><span data-stu-id="1af36-108">DESCRIPTION</span></span>
<span data-ttu-id="1af36-109">取得複製的狀態</span><span class="sxs-lookup"><span data-stu-id="1af36-109">Get the status of the replication</span></span>

## <span data-ttu-id="1af36-110">例子</span><span class="sxs-lookup"><span data-stu-id="1af36-110">EXAMPLES</span></span>

### <span data-ttu-id="1af36-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="1af36-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="1af36-112">此命令會獲得 MyVol 上的複製狀態</span><span class="sxs-lookup"><span data-stu-id="1af36-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="1af36-113">參數</span><span class="sxs-lookup"><span data-stu-id="1af36-113">PARAMETERS</span></span>

### <span data-ttu-id="1af36-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1af36-114">-AccountName</span></span>
<span data-ttu-id="1af36-115">複製目的地大量之 ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="1af36-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="1af36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af36-116">-DefaultProfile</span></span>
<span data-ttu-id="1af36-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1af36-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1af36-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1af36-118">-InputObject</span></span>
<span data-ttu-id="1af36-119">ANF 複製目標大量物件以取得複製狀態</span><span class="sxs-lookup"><span data-stu-id="1af36-119">The ANF replication destination volume object to get replication status</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1af36-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1af36-120">-Name</span></span>
<span data-ttu-id="1af36-121">ANF 複製目的地音量的名稱</span><span class="sxs-lookup"><span data-stu-id="1af36-121">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af36-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="1af36-122">-PoolName</span></span>
<span data-ttu-id="1af36-123">複製目的地音量的 ANF 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="1af36-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="1af36-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af36-124">-ResourceGroupName</span></span>
<span data-ttu-id="1af36-125">ANF 複製目的地大量資源群組</span><span class="sxs-lookup"><span data-stu-id="1af36-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="1af36-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1af36-126">-ResourceId</span></span>
<span data-ttu-id="1af36-127">ANF 複製目的地大量資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1af36-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="1af36-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af36-128">CommonParameters</span></span>
<span data-ttu-id="1af36-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1af36-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af36-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1af36-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af36-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1af36-131">INPUTS</span></span>

### <span data-ttu-id="1af36-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1af36-132">System.String</span></span>

### <span data-ttu-id="1af36-133">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="1af36-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="1af36-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1af36-134">OUTPUTS</span></span>

### <span data-ttu-id="1af36-135">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="1af36-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="1af36-136">筆記</span><span class="sxs-lookup"><span data-stu-id="1af36-136">NOTES</span></span>

## <span data-ttu-id="1af36-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="1af36-137">RELATED LINKS</span></span>

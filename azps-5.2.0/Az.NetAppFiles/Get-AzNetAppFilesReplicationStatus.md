---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: e59ce4f5e3b0f1b07744e0754cf0e1cae3de7da6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281781"
---
# <span data-ttu-id="7281e-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="7281e-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="7281e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7281e-102">SYNOPSIS</span></span>
<span data-ttu-id="7281e-103">取得複製狀態</span><span class="sxs-lookup"><span data-stu-id="7281e-103">Get the status of the replication</span></span>

## <span data-ttu-id="7281e-104">句法</span><span class="sxs-lookup"><span data-stu-id="7281e-104">SYNTAX</span></span>

### <span data-ttu-id="7281e-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7281e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7281e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7281e-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7281e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7281e-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7281e-108">說明</span><span class="sxs-lookup"><span data-stu-id="7281e-108">DESCRIPTION</span></span>
<span data-ttu-id="7281e-109">取得複製狀態</span><span class="sxs-lookup"><span data-stu-id="7281e-109">Get the status of the replication</span></span>

## <span data-ttu-id="7281e-110">示例</span><span class="sxs-lookup"><span data-stu-id="7281e-110">EXAMPLES</span></span>

### <span data-ttu-id="7281e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7281e-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="7281e-112">這個命令會在 MyVol 上取得複製狀態</span><span class="sxs-lookup"><span data-stu-id="7281e-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="7281e-113">參數</span><span class="sxs-lookup"><span data-stu-id="7281e-113">PARAMETERS</span></span>

### <span data-ttu-id="7281e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7281e-114">-AccountName</span></span>
<span data-ttu-id="7281e-115">複製目標量的 ANF 帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="7281e-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="7281e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7281e-116">-DefaultProfile</span></span>
<span data-ttu-id="7281e-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7281e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7281e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7281e-118">-InputObject</span></span>
<span data-ttu-id="7281e-119">要取得複製狀態的 ANF 複製目標卷物件</span><span class="sxs-lookup"><span data-stu-id="7281e-119">The ANF replication destination volume object to get replication status</span></span>

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

### <span data-ttu-id="7281e-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="7281e-120">-Name</span></span>
<span data-ttu-id="7281e-121">ANF 複製目標量的名稱</span><span class="sxs-lookup"><span data-stu-id="7281e-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="7281e-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="7281e-122">-PoolName</span></span>
<span data-ttu-id="7281e-123">複製目標量的 ANF 池名稱</span><span class="sxs-lookup"><span data-stu-id="7281e-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="7281e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7281e-124">-ResourceGroupName</span></span>
<span data-ttu-id="7281e-125">ANF 複製目標量的資源群組</span><span class="sxs-lookup"><span data-stu-id="7281e-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="7281e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7281e-126">-ResourceId</span></span>
<span data-ttu-id="7281e-127">ANF 複製目標量的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7281e-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="7281e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7281e-128">CommonParameters</span></span>
<span data-ttu-id="7281e-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7281e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7281e-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7281e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7281e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="7281e-131">INPUTS</span></span>

### <span data-ttu-id="7281e-132">System.object</span><span class="sxs-lookup"><span data-stu-id="7281e-132">System.String</span></span>

### <span data-ttu-id="7281e-133">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="7281e-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="7281e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7281e-134">OUTPUTS</span></span>

### <span data-ttu-id="7281e-135">PSNetAppFilesReplicationStatus 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="7281e-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="7281e-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7281e-136">NOTES</span></span>

## <span data-ttu-id="7281e-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7281e-137">RELATED LINKS</span></span>

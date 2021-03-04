---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolgeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
ms.openlocfilehash: d1c0b6439b148d51506861a6bfffc6a6681343ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903389"
---
# <span data-ttu-id="7dc46-101">Get-AzSynapseSqlPoolGeoBackup</span><span class="sxs-lookup"><span data-stu-id="7dc46-101">Get-AzSynapseSqlPoolGeoBackup</span></span>

## <span data-ttu-id="7dc46-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7dc46-102">SYNOPSIS</span></span>
<span data-ttu-id="7dc46-103">為 Sql Pool 進行異地備份。</span><span class="sxs-lookup"><span data-stu-id="7dc46-103">Gets a geo-redundant backup of a Sql Pool.</span></span>

## <span data-ttu-id="7dc46-104">語法</span><span class="sxs-lookup"><span data-stu-id="7dc46-104">SYNTAX</span></span>

### <span data-ttu-id="7dc46-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7dc46-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dc46-106">SqlPoolGeoBackupResourceId</span><span class="sxs-lookup"><span data-stu-id="7dc46-106">SqlPoolGeoBackupResourceId</span></span>
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7dc46-107">描述</span><span class="sxs-lookup"><span data-stu-id="7dc46-107">DESCRIPTION</span></span>
<span data-ttu-id="7dc46-108">**Get-AzSynapseSqlPoolGeoBackup** Cmdlet 會取得 SQL 集區或指定工作區上所有可用之異地重複備份的指定異地備份。</span><span class="sxs-lookup"><span data-stu-id="7dc46-108">The **Get-AzSynapseSqlPoolGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL Pool or all available geo-redundant backups on a specified workspace.</span></span>
<span data-ttu-id="7dc46-109">異地重複備份是使用個別地理位置的資料檔案可還原的資源。</span><span class="sxs-lookup"><span data-stu-id="7dc46-109">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="7dc46-110">您可以在Geo-Restore中斷時還原異地重複備份，以將 Sql 集區復原至新區域。</span><span class="sxs-lookup"><span data-stu-id="7dc46-110">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your Sql Pool to a new region.</span></span>

## <span data-ttu-id="7dc46-111">例子</span><span class="sxs-lookup"><span data-stu-id="7dc46-111">EXAMPLES</span></span>

### <span data-ttu-id="7dc46-112">範例 1：取得指定的異地重複備份</span><span class="sxs-lookup"><span data-stu-id="7dc46-112">Example 1: Get a specified geo-redundant backup</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName ContosoResourceGroup -WorkspaceName "ContosoWorkspace" -Name "ContosoSqlPool"
```
<span data-ttu-id="7dc46-113">Cmdlet 會針對 sql 集區取回地理位置備份。</span><span class="sxs-lookup"><span data-stu-id="7dc46-113">The cmdlet retrieves Geo Backup for a sql pool.</span></span>

### <span data-ttu-id="7dc46-114">範例 2：在工作區上取得所有異地重複備份</span><span class="sxs-lookup"><span data-stu-id="7dc46-114">Example 2: Get all geo-redundant backups on a workspace</span></span>
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
<span data-ttu-id="7dc46-115">此命令會獲得指定工作區上所有可用的異地重複備份。</span><span class="sxs-lookup"><span data-stu-id="7dc46-115">This command gets all available geo-redundant backups on a specified workspace.</span></span>

### <span data-ttu-id="7dc46-116">範例 3：使用篩選在工作區上取得所有異地重複備份</span><span class="sxs-lookup"><span data-stu-id="7dc46-116">Example 3: Get all geo-redundant backups on a workspace using filtering</span></span>
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Name "Contoso*"
```
<span data-ttu-id="7dc46-117">此命令可在以 「Contoso」為開始的指定工作區上，獲得所有可用的異地重複備份。</span><span class="sxs-lookup"><span data-stu-id="7dc46-117">This command gets all available geo-redundant backups on a specified workspace that start with "Contoso".</span></span>

## <span data-ttu-id="7dc46-118">參數</span><span class="sxs-lookup"><span data-stu-id="7dc46-118">PARAMETERS</span></span>

### <span data-ttu-id="7dc46-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dc46-119">-DefaultProfile</span></span>
<span data-ttu-id="7dc46-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7dc46-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dc46-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="7dc46-121">-Name</span></span>
<span data-ttu-id="7dc46-122">Synapse Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="7dc46-122">The Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: The Synapse Sql pool.

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dc46-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7dc46-123">-ResourceId</span></span>
<span data-ttu-id="7dc46-124">輸入 Sql 集區地理位置備份資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7dc46-124">Input a Sql Pool Geo Backup Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolGeoBackupResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dc46-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dc46-125">-ResourceGroupName</span></span>
<span data-ttu-id="7dc46-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="7dc46-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dc46-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7dc46-127">-WorkspaceName</span></span>
<span data-ttu-id="7dc46-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="7dc46-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dc46-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dc46-129">CommonParameters</span></span>
<span data-ttu-id="7dc46-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7dc46-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dc46-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7dc46-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dc46-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7dc46-132">INPUTS</span></span>

### <span data-ttu-id="7dc46-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7dc46-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7dc46-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7dc46-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span></span>

## <span data-ttu-id="7dc46-135">輸出</span><span class="sxs-lookup"><span data-stu-id="7dc46-135">OUTPUTS</span></span>

### <span data-ttu-id="7dc46-136">Microsoft.Azure.Commands.Synapse.models.PSBackupModel</span><span class="sxs-lookup"><span data-stu-id="7dc46-136">Microsoft.Azure.Commands.Synapse.Models.PSBackupModel</span></span>

## <span data-ttu-id="7dc46-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7dc46-137">NOTES</span></span>

## <span data-ttu-id="7dc46-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="7dc46-138">RELATED LINKS</span></span>

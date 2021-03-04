---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedroppedsqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
ms.openlocfilehash: 26e4e5c77913f01b8a7097f6baebd68977ceed22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909381"
---
# <span data-ttu-id="902e4-101">Get-AzSynapseDroppedSqlPool</span><span class="sxs-lookup"><span data-stu-id="902e4-101">Get-AzSynapseDroppedSqlPool</span></span>

## <span data-ttu-id="902e4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="902e4-102">SYNOPSIS</span></span>
<span data-ttu-id="902e4-103">為 Synapse Sql Pool 進行刪除的 Sql 集區備份。</span><span class="sxs-lookup"><span data-stu-id="902e4-103">Gets a dropped Sql pool backup of a Synapse Sql Pool.</span></span>

## <span data-ttu-id="902e4-104">語法</span><span class="sxs-lookup"><span data-stu-id="902e4-104">SYNTAX</span></span>

### <span data-ttu-id="902e4-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="902e4-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseDroppedSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="902e4-106">DroppedSqlPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="902e4-106">DroppedSqlPoolResourceId</span></span>
```
Get-AzSynapseDroppedSqlPool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="902e4-107">描述</span><span class="sxs-lookup"><span data-stu-id="902e4-107">DESCRIPTION</span></span>
<span data-ttu-id="902e4-108">**Get-AzSynapseDroppedSqlPool** Cmdlet 會取得指定的已刪除 SQL 集區備份，您可以還原備份，或所有可以在工作區還原的已刪除備份。</span><span class="sxs-lookup"><span data-stu-id="902e4-108">The **Get-AzSynapseDroppedSqlPool** cmdlet gets a specified deleted SQL pool backup that you can restore, or all deleted backups that you can restore in a workspace.</span></span> 


## <span data-ttu-id="902e4-109">例子</span><span class="sxs-lookup"><span data-stu-id="902e4-109">EXAMPLES</span></span>

### <span data-ttu-id="902e4-110">範例 1：從 sql 資料庫取得指定的刪除 sqlpools</span><span class="sxs-lookup"><span data-stu-id="902e4-110">Example 1: Get a specified dropped sqlpools from a sql pool</span></span>
```powershell
PS C:\> Get-AzSynapseDroppedSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name "ContosoSqlPool"
```
<span data-ttu-id="902e4-111">Cmdlet 會針對 sql 資料庫取回已中斷的 sqlpools。</span><span class="sxs-lookup"><span data-stu-id="902e4-111">The cmdlet retrieves dropped sqlpools for a sql pool.</span></span>

### <span data-ttu-id="902e4-112">範例 2：在工作區上取得所有刪除的 sqlpool</span><span class="sxs-lookup"><span data-stu-id="902e4-112">Example 2: Get all dropped sqlpool on a workspace</span></span>
```
PS C:\>Get-AzSynapseDroppedSqlPool -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
<span data-ttu-id="902e4-113">此命令會獲得指定工作區上所有可用的 Sqlpool。</span><span class="sxs-lookup"><span data-stu-id="902e4-113">This command gets all available dropped sqlpool on a specified workspace.</span></span>

## <span data-ttu-id="902e4-114">參數</span><span class="sxs-lookup"><span data-stu-id="902e4-114">PARAMETERS</span></span>

### <span data-ttu-id="902e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="902e4-115">-DefaultProfile</span></span>
<span data-ttu-id="902e4-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="902e4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="902e4-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="902e4-117">-Name</span></span>
<span data-ttu-id="902e4-118">Synapse Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="902e4-118">The Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: AzSynapseDroppedSqlPool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="902e4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="902e4-119">-ResourceId</span></span>
<span data-ttu-id="902e4-120">輸入刪除的 Sql 資料庫資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="902e4-120">Input a Dropped Sql Pool Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DroppedSqlPoolResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902e4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="902e4-121">-ResourceGroupName</span></span>
<span data-ttu-id="902e4-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="902e4-122">Resource group name.</span></span>

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

### <span data-ttu-id="902e4-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="902e4-123">-WorkspaceName</span></span>
<span data-ttu-id="902e4-124">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="902e4-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="902e4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="902e4-125">CommonParameters</span></span>
<span data-ttu-id="902e4-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="902e4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="902e4-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="902e4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="902e4-128">輸入</span><span class="sxs-lookup"><span data-stu-id="902e4-128">INPUTS</span></span>

### <span data-ttu-id="902e4-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="902e4-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="902e4-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span><span class="sxs-lookup"><span data-stu-id="902e4-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span></span>

## <span data-ttu-id="902e4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="902e4-131">OUTPUTS</span></span>

### <span data-ttu-id="902e4-132">Microsoft.Azure.Commands.Synapse.Models.PSDroppedSqlPoolBackupModel</span><span class="sxs-lookup"><span data-stu-id="902e4-132">Microsoft.Azure.Commands.Synapse.Models.PSDroppedSqlPoolBackupModel</span></span>

## <span data-ttu-id="902e4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="902e4-133">NOTES</span></span>

## <span data-ttu-id="902e4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="902e4-134">RELATED LINKS</span></span>

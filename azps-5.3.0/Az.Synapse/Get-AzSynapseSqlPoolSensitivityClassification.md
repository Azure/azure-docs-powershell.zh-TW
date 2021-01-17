---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 6affe94fdbfa7a698ad7d666d1847365fc8e25ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288252"
---
# <span data-ttu-id="e1bcf-101">Get-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="e1bcf-101">Get-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="e1bcf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="e1bcf-103">取得 SQL 池中各欄的目前資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="e1bcf-103">Gets the current information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="e1bcf-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1bcf-104">SYNTAX</span></span>

### <span data-ttu-id="e1bcf-105">SqlPoolObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e1bcf-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1bcf-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1bcf-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1bcf-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1bcf-107">ColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1bcf-108">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1bcf-108">SqlPoolObjectColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1bcf-109">說明</span><span class="sxs-lookup"><span data-stu-id="e1bcf-109">DESCRIPTION</span></span>
<span data-ttu-id="e1bcf-110">Get-AzSynapseSqlPoolSensitivityClassification Cmdlet 會傳回 Azure Synapse SQL pool 中資料行的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="e1bcf-110">The Get-AzSynapseSqlPoolSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure Synapse SQL pool.</span></span>

## <span data-ttu-id="e1bcf-111">示例</span><span class="sxs-lookup"><span data-stu-id="e1bcf-111">EXAMPLES</span></span>

### <span data-ttu-id="e1bcf-112">範例1：取得 Azure Synapse SQL pool 的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="e1bcf-112">Example 1: Get current information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="e1bcf-113">範例2：使用管道取得 Azure Synapse SQL pool 的目前資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="e1bcf-113">Example 2: Get current information types and sensitivity labels of an Azure Synapse SQL pool with Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="e1bcf-114">範例3：取得 Azure Synapse SQL pool 之特定資料行的目前資訊類型與敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="e1bcf-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="e1bcf-115">範例4：使用管道取得 Azure Synapse SQL pool 之特定資料行的目前資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="e1bcf-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="e1bcf-116">參數</span><span class="sxs-lookup"><span data-stu-id="e1bcf-116">PARAMETERS</span></span>

### <span data-ttu-id="e1bcf-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1bcf-117">-AsJob</span></span>
<span data-ttu-id="e1bcf-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e1bcf-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bcf-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="e1bcf-119">-ColumnName</span></span>
<span data-ttu-id="e1bcf-120">資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1bcf-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bcf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1bcf-121">-DefaultProfile</span></span>
<span data-ttu-id="e1bcf-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1bcf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1bcf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1bcf-123">-ResourceGroupName</span></span>
<span data-ttu-id="e1bcf-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e1bcf-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bcf-125">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e1bcf-125">-SchemaName</span></span>
<span data-ttu-id="e1bcf-126">架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1bcf-126">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bcf-127">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="e1bcf-127">-SqlPoolName</span></span>
<span data-ttu-id="e1bcf-128">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1bcf-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bcf-129">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="e1bcf-129">-SqlPoolObject</span></span>
<span data-ttu-id="e1bcf-130">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="e1bcf-130">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bcf-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="e1bcf-131">-TableName</span></span>
<span data-ttu-id="e1bcf-132">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1bcf-132">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bcf-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e1bcf-133">-WorkspaceName</span></span>
<span data-ttu-id="e1bcf-134">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1bcf-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bcf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1bcf-135">CommonParameters</span></span>
<span data-ttu-id="e1bcf-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1bcf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1bcf-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e1bcf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1bcf-138">輸入</span><span class="sxs-lookup"><span data-stu-id="e1bcf-138">INPUTS</span></span>

### <span data-ttu-id="e1bcf-139">System.object</span><span class="sxs-lookup"><span data-stu-id="e1bcf-139">System.String</span></span>

### <span data-ttu-id="e1bcf-140">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e1bcf-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e1bcf-141">輸出</span><span class="sxs-lookup"><span data-stu-id="e1bcf-141">OUTPUTS</span></span>

### <span data-ttu-id="e1bcf-142">Synapse DataClassification. SqlPoolSensitivityClassificationModel （）</span><span class="sxs-lookup"><span data-stu-id="e1bcf-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="e1bcf-143">筆記</span><span class="sxs-lookup"><span data-stu-id="e1bcf-143">NOTES</span></span>

## <span data-ttu-id="e1bcf-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1bcf-144">RELATED LINKS</span></span>

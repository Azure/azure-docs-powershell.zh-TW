---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 0942373dc3ad741f10d5a87d7b4713413f9db4f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916693"
---
# <span data-ttu-id="eadc4-101">Get-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="eadc4-101">Get-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="eadc4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eadc4-102">SYNOPSIS</span></span>
<span data-ttu-id="eadc4-103">在 SQL 資料庫中，獲得欄的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="eadc4-103">Gets the current information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="eadc4-104">語法</span><span class="sxs-lookup"><span data-stu-id="eadc4-104">SYNTAX</span></span>

### <span data-ttu-id="eadc4-105">SqlPoolObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="eadc4-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eadc4-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="eadc4-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eadc4-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="eadc4-107">ColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eadc4-108">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="eadc4-108">SqlPoolObjectColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eadc4-109">描述</span><span class="sxs-lookup"><span data-stu-id="eadc4-109">DESCRIPTION</span></span>
<span data-ttu-id="eadc4-110">Cmdlet Get-AzSynapseSqlPoolSensitivityClassification Azure Synapse SQL 集區中欄的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="eadc4-110">The Get-AzSynapseSqlPoolSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure Synapse SQL pool.</span></span>

## <span data-ttu-id="eadc4-111">例子</span><span class="sxs-lookup"><span data-stu-id="eadc4-111">EXAMPLES</span></span>

### <span data-ttu-id="eadc4-112">範例 1：取得 Azure Synapse SQL 資料庫的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="eadc4-112">Example 1: Get current information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="eadc4-113">範例 2：取得 Azure Synapse SQL 資料庫與管道的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="eadc4-113">Example 2: Get current information types and sensitivity labels of an Azure Synapse SQL pool with Piping.</span></span>
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

### <span data-ttu-id="eadc4-114">範例 3：取得 Azure Synapse SQL 資料庫特定資料行的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="eadc4-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="eadc4-115">範例 4：使用管道取得 Azure Synapse SQL 資料庫特定資料行的目前資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="eadc4-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool using Piping.</span></span>
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

## <span data-ttu-id="eadc4-116">參數</span><span class="sxs-lookup"><span data-stu-id="eadc4-116">PARAMETERS</span></span>

### <span data-ttu-id="eadc4-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eadc4-117">-AsJob</span></span>
<span data-ttu-id="eadc4-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eadc4-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eadc4-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="eadc4-119">-ColumnName</span></span>
<span data-ttu-id="eadc4-120">欄的名稱。</span><span class="sxs-lookup"><span data-stu-id="eadc4-120">Name of column.</span></span>

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

### <span data-ttu-id="eadc4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eadc4-121">-DefaultProfile</span></span>
<span data-ttu-id="eadc4-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eadc4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eadc4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eadc4-123">-ResourceGroupName</span></span>
<span data-ttu-id="eadc4-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="eadc4-124">Resource group name.</span></span>

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

### <span data-ttu-id="eadc4-125">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="eadc4-125">-SchemaName</span></span>
<span data-ttu-id="eadc4-126">架構名稱。</span><span class="sxs-lookup"><span data-stu-id="eadc4-126">Name of schema.</span></span>

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

### <span data-ttu-id="eadc4-127">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="eadc4-127">-SqlPoolName</span></span>
<span data-ttu-id="eadc4-128">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="eadc4-128">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="eadc4-129">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="eadc4-129">-SqlPoolObject</span></span>
<span data-ttu-id="eadc4-130">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="eadc4-130">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="eadc4-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="eadc4-131">-TableName</span></span>
<span data-ttu-id="eadc4-132">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="eadc4-132">Name of table.</span></span>

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

### <span data-ttu-id="eadc4-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eadc4-133">-WorkspaceName</span></span>
<span data-ttu-id="eadc4-134">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="eadc4-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="eadc4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eadc4-135">CommonParameters</span></span>
<span data-ttu-id="eadc4-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eadc4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eadc4-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eadc4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eadc4-138">輸入</span><span class="sxs-lookup"><span data-stu-id="eadc4-138">INPUTS</span></span>

### <span data-ttu-id="eadc4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="eadc4-139">System.String</span></span>

### <span data-ttu-id="eadc4-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="eadc4-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="eadc4-141">輸出</span><span class="sxs-lookup"><span data-stu-id="eadc4-141">OUTPUTS</span></span>

### <span data-ttu-id="eadc4-142">Microsoft.Azure.Commands.Synapse.models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="eadc4-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="eadc4-143">筆記</span><span class="sxs-lookup"><span data-stu-id="eadc4-143">NOTES</span></span>

## <span data-ttu-id="eadc4-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="eadc4-144">RELATED LINKS</span></span>

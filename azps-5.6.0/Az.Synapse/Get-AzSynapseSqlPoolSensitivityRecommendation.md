---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: d2949bf2d366dc64b0e55b82d0c90979042ea294
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910338"
---
# <span data-ttu-id="88397-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="88397-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="88397-102">簡介</span><span class="sxs-lookup"><span data-stu-id="88397-102">SYNOPSIS</span></span>
<span data-ttu-id="88397-103">在 SQL 資料庫中，獲得資料行的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="88397-103">Gets the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="88397-104">語法</span><span class="sxs-lookup"><span data-stu-id="88397-104">SYNTAX</span></span>

### <span data-ttu-id="88397-105">SqlPoolObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="88397-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88397-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="88397-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88397-107">描述</span><span class="sxs-lookup"><span data-stu-id="88397-107">DESCRIPTION</span></span>
<span data-ttu-id="88397-108">此Get-AzSynapseSqlPoolSensitivityRecommendation Cmdlet 會返回 SQL 資料庫中資料行的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="88397-108">The Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="88397-109">例子</span><span class="sxs-lookup"><span data-stu-id="88397-109">EXAMPLES</span></span>

### <span data-ttu-id="88397-110">範例 1：取得 Azure Synapse SQL 資料庫的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="88397-110">Example 1: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

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

### <span data-ttu-id="88397-111">範例 2：使用管道取得 Azure Synapse SQL 資料庫的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="88397-111">Example 2: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityRecommendation

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

## <span data-ttu-id="88397-112">參數</span><span class="sxs-lookup"><span data-stu-id="88397-112">PARAMETERS</span></span>

### <span data-ttu-id="88397-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88397-113">-AsJob</span></span>
<span data-ttu-id="88397-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="88397-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88397-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88397-115">-DefaultProfile</span></span>
<span data-ttu-id="88397-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="88397-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88397-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88397-117">-ResourceGroupName</span></span>
<span data-ttu-id="88397-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="88397-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88397-119">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="88397-119">-SqlPoolName</span></span>
<span data-ttu-id="88397-120">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="88397-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88397-121">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="88397-121">-SqlPoolObject</span></span>
<span data-ttu-id="88397-122">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="88397-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88397-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="88397-123">-WorkspaceName</span></span>
<span data-ttu-id="88397-124">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="88397-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88397-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88397-125">CommonParameters</span></span>
<span data-ttu-id="88397-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="88397-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88397-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88397-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88397-128">輸入</span><span class="sxs-lookup"><span data-stu-id="88397-128">INPUTS</span></span>

### <span data-ttu-id="88397-129">System.String</span><span class="sxs-lookup"><span data-stu-id="88397-129">System.String</span></span>

### <span data-ttu-id="88397-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="88397-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="88397-131">輸出</span><span class="sxs-lookup"><span data-stu-id="88397-131">OUTPUTS</span></span>

### <span data-ttu-id="88397-132">Microsoft.Azure.Commands.Synapse.models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="88397-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="88397-133">筆記</span><span class="sxs-lookup"><span data-stu-id="88397-133">NOTES</span></span>

## <span data-ttu-id="88397-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="88397-134">RELATED LINKS</span></span>

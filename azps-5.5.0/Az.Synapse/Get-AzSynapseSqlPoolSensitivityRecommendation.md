---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 89b9b5df2f8233254d4c1cb430a80f0a8a91c13b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136819"
---
# <span data-ttu-id="9a51c-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="9a51c-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="9a51c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a51c-102">SYNOPSIS</span></span>
<span data-ttu-id="9a51c-103">取得 SQL 池中各欄的建議資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="9a51c-103">Gets the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="9a51c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a51c-104">SYNTAX</span></span>

### <span data-ttu-id="9a51c-105">SqlPoolObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9a51c-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a51c-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a51c-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a51c-107">說明</span><span class="sxs-lookup"><span data-stu-id="9a51c-107">DESCRIPTION</span></span>
<span data-ttu-id="9a51c-108">Get-AzSynapseSqlPoolSensitivityRecommendation Cmdlet 會傳回建議的資訊類型，以及 SQL 池中欄的敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="9a51c-108">The Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="9a51c-109">示例</span><span class="sxs-lookup"><span data-stu-id="9a51c-109">EXAMPLES</span></span>

### <span data-ttu-id="9a51c-110">範例1：取得 Azure Synapse SQL pool 的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="9a51c-110">Example 1: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="9a51c-111">範例2：使用管道取得 Azure Synapse SQL pool 的建議資訊類型及敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="9a51c-111">Example 2: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool using Piping.</span></span>
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

## <span data-ttu-id="9a51c-112">參數</span><span class="sxs-lookup"><span data-stu-id="9a51c-112">PARAMETERS</span></span>

### <span data-ttu-id="9a51c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a51c-113">-AsJob</span></span>
<span data-ttu-id="9a51c-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9a51c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a51c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a51c-115">-DefaultProfile</span></span>
<span data-ttu-id="9a51c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a51c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a51c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a51c-117">-ResourceGroupName</span></span>
<span data-ttu-id="9a51c-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9a51c-118">Resource group name.</span></span>

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

### <span data-ttu-id="9a51c-119">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="9a51c-119">-SqlPoolName</span></span>
<span data-ttu-id="9a51c-120">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a51c-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="9a51c-121">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="9a51c-121">-SqlPoolObject</span></span>
<span data-ttu-id="9a51c-122">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="9a51c-122">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9a51c-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9a51c-123">-WorkspaceName</span></span>
<span data-ttu-id="9a51c-124">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a51c-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9a51c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a51c-125">CommonParameters</span></span>
<span data-ttu-id="9a51c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a51c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a51c-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9a51c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a51c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="9a51c-128">INPUTS</span></span>

### <span data-ttu-id="9a51c-129">System.object</span><span class="sxs-lookup"><span data-stu-id="9a51c-129">System.String</span></span>

### <span data-ttu-id="9a51c-130">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="9a51c-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="9a51c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="9a51c-131">OUTPUTS</span></span>

### <span data-ttu-id="9a51c-132">Synapse DataClassification. SqlPoolSensitivityClassificationModel （）</span><span class="sxs-lookup"><span data-stu-id="9a51c-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="9a51c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="9a51c-133">NOTES</span></span>

## <span data-ttu-id="9a51c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a51c-134">RELATED LINKS</span></span>

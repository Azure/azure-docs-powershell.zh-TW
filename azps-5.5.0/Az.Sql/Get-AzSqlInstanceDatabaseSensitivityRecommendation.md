---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: cf9250080e0d8e079257a4996b7d263bd96a2093
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137099"
---
# <span data-ttu-id="a148f-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="a148f-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="a148f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a148f-102">SYNOPSIS</span></span>
<span data-ttu-id="a148f-103">取得 Azure SQL managed 實例資料庫中資料行的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="a148f-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="a148f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a148f-104">SYNTAX</span></span>

### <span data-ttu-id="a148f-105">DatabaseObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a148f-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a148f-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="a148f-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a148f-107">說明</span><span class="sxs-lookup"><span data-stu-id="a148f-107">DESCRIPTION</span></span>
<span data-ttu-id="a148f-108">Get-AzSqlInstanceDatabaseSensitivityRecommendation Cmdlet 會傳回 Azure SQL managed 實例資料庫中資料行的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="a148f-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="a148f-109">示例</span><span class="sxs-lookup"><span data-stu-id="a148f-109">EXAMPLES</span></span>

### <span data-ttu-id="a148f-110">範例1：取得 Azure SQL managed 實例資料庫的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="a148f-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
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

### <span data-ttu-id="a148f-111">範例2：使用管道取得 Azure SQL managed 實例資料庫的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="a148f-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
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

## <span data-ttu-id="a148f-112">參數</span><span class="sxs-lookup"><span data-stu-id="a148f-112">PARAMETERS</span></span>

### <span data-ttu-id="a148f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a148f-113">-AsJob</span></span>
<span data-ttu-id="a148f-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a148f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a148f-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a148f-115">-DatabaseName</span></span>
<span data-ttu-id="a148f-116">Azure SQL managed 實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a148f-116">The name of the Azure SQL managed instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a148f-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="a148f-117">-DatabaseObject</span></span>
<span data-ttu-id="a148f-118">Azure SQL managed 實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="a148f-118">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a148f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a148f-119">-DefaultProfile</span></span>
<span data-ttu-id="a148f-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a148f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a148f-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a148f-121">-InstanceName</span></span>
<span data-ttu-id="a148f-122">Azure SQL managed 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="a148f-122">Azure SQL managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a148f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a148f-123">-ResourceGroupName</span></span>
<span data-ttu-id="a148f-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a148f-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a148f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a148f-125">CommonParameters</span></span>
<span data-ttu-id="a148f-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a148f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a148f-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a148f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a148f-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a148f-128">INPUTS</span></span>

### <span data-ttu-id="a148f-129">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="a148f-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="a148f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a148f-130">OUTPUTS</span></span>

### <span data-ttu-id="a148f-131">ManagedDatabaseSensitivityClassificationModel 中的 [DataClassification]</span><span class="sxs-lookup"><span data-stu-id="a148f-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="a148f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a148f-132">NOTES</span></span>

## <span data-ttu-id="a148f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a148f-133">RELATED LINKS</span></span>

[<span data-ttu-id="a148f-134">深入瞭解 Azure SQL 資料庫資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="a148f-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)

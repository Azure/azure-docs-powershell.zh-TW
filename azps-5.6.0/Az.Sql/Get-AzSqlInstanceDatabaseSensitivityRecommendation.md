---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 0d40e03b26481b5e974b294533566549646ba628
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914305"
---
# <span data-ttu-id="1d89f-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="1d89f-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="1d89f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1d89f-102">SYNOPSIS</span></span>
<span data-ttu-id="1d89f-103">在 Azure SQL 受管理的實例資料庫中，獲得資料行的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="1d89f-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="1d89f-104">語法</span><span class="sxs-lookup"><span data-stu-id="1d89f-104">SYNTAX</span></span>

### <span data-ttu-id="1d89f-105">DatabaseObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1d89f-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d89f-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d89f-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d89f-107">描述</span><span class="sxs-lookup"><span data-stu-id="1d89f-107">DESCRIPTION</span></span>
<span data-ttu-id="1d89f-108">Cmdlet Get-AzSqlInstanceDatabaseSensitivityRecommendation Azure SQL 受管理的實例資料庫中，會返回建議的欄資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="1d89f-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="1d89f-109">例子</span><span class="sxs-lookup"><span data-stu-id="1d89f-109">EXAMPLES</span></span>

### <span data-ttu-id="1d89f-110">範例 1：取得 Azure SQL 受管理實例資料庫的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="1d89f-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
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

### <span data-ttu-id="1d89f-111">範例 2：使用管道取得 Azure SQL 受管理實例資料庫的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="1d89f-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
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

## <span data-ttu-id="1d89f-112">參數</span><span class="sxs-lookup"><span data-stu-id="1d89f-112">PARAMETERS</span></span>

### <span data-ttu-id="1d89f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d89f-113">-AsJob</span></span>
<span data-ttu-id="1d89f-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d89f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d89f-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1d89f-115">-DatabaseName</span></span>
<span data-ttu-id="1d89f-116">Azure SQL 受管理的實例資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="1d89f-116">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="1d89f-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="1d89f-117">-DatabaseObject</span></span>
<span data-ttu-id="1d89f-118">Azure SQL 受管理的實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="1d89f-118">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="1d89f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d89f-119">-DefaultProfile</span></span>
<span data-ttu-id="1d89f-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1d89f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d89f-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="1d89f-121">-InstanceName</span></span>
<span data-ttu-id="1d89f-122">Azure SQL 受管理的實例名稱。</span><span class="sxs-lookup"><span data-stu-id="1d89f-122">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="1d89f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d89f-123">-ResourceGroupName</span></span>
<span data-ttu-id="1d89f-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d89f-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="1d89f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d89f-125">CommonParameters</span></span>
<span data-ttu-id="1d89f-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1d89f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d89f-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d89f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d89f-128">輸入</span><span class="sxs-lookup"><span data-stu-id="1d89f-128">INPUTS</span></span>

### <span data-ttu-id="1d89f-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1d89f-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="1d89f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="1d89f-130">OUTPUTS</span></span>

### <span data-ttu-id="1d89f-131">Microsoft.Azure.Commands.sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="1d89f-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="1d89f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="1d89f-132">NOTES</span></span>

## <span data-ttu-id="1d89f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d89f-133">RELATED LINKS</span></span>

[<span data-ttu-id="1d89f-134">深入瞭解 Azure SQL Database 資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="1d89f-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)

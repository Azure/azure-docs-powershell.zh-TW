---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: a7aadc195be162db5f612dae47451f0b118fce19
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141045"
---
# <span data-ttu-id="fe104-101">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="fe104-101">Get-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="fe104-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe104-102">SYNOPSIS</span></span>
<span data-ttu-id="fe104-103">取得資料庫地域備份原則。</span><span class="sxs-lookup"><span data-stu-id="fe104-103">Gets a database geo backup policy.</span></span>

## <span data-ttu-id="fe104-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe104-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe104-105">說明</span><span class="sxs-lookup"><span data-stu-id="fe104-105">DESCRIPTION</span></span>
<span data-ttu-id="fe104-106">**AzSqlDatabaseGeoBackupPolicy** Cmdlet 會取得已登錄至此資料庫的 geo 備份原則。</span><span class="sxs-lookup"><span data-stu-id="fe104-106">The **Get-AzSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="fe104-107">這是用來定義備份儲存原則的 Azure 備份資源。</span><span class="sxs-lookup"><span data-stu-id="fe104-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="fe104-108">示例</span><span class="sxs-lookup"><span data-stu-id="fe104-108">EXAMPLES</span></span>

### <span data-ttu-id="fe104-109">範例1</span><span class="sxs-lookup"><span data-stu-id="fe104-109">Example 1</span></span>

<span data-ttu-id="fe104-110">取得資料庫地域備份原則。</span><span class="sxs-lookup"><span data-stu-id="fe104-110">Gets a database geo backup policy.</span></span> <span data-ttu-id="fe104-111"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="fe104-111">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlDatabaseGeoBackupPolicy -DatabaseName db1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="fe104-112">參數</span><span class="sxs-lookup"><span data-stu-id="fe104-112">PARAMETERS</span></span>

### <span data-ttu-id="fe104-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fe104-113">-DatabaseName</span></span>
<span data-ttu-id="fe104-114">指定此 Cmdlet 取得 geo 備份原則之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe104-114">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe104-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe104-115">-DefaultProfile</span></span>
<span data-ttu-id="fe104-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fe104-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe104-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe104-117">-ResourceGroupName</span></span>
<span data-ttu-id="fe104-118">指定包含此資料庫之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe104-118">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe104-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fe104-119">-ServerName</span></span>
<span data-ttu-id="fe104-120">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="fe104-120">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe104-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe104-121">CommonParameters</span></span>
<span data-ttu-id="fe104-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe104-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe104-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fe104-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe104-124">輸入</span><span class="sxs-lookup"><span data-stu-id="fe104-124">INPUTS</span></span>

### <span data-ttu-id="fe104-125">System.object</span><span class="sxs-lookup"><span data-stu-id="fe104-125">System.String</span></span>

## <span data-ttu-id="fe104-126">輸出</span><span class="sxs-lookup"><span data-stu-id="fe104-126">OUTPUTS</span></span>

### <span data-ttu-id="fe104-127">AzureSqlDatabaseGeoBackupPolicyModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="fe104-127">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="fe104-128">筆記</span><span class="sxs-lookup"><span data-stu-id="fe104-128">NOTES</span></span>

## <span data-ttu-id="fe104-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe104-129">RELATED LINKS</span></span>

[<span data-ttu-id="fe104-130">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="fe104-130">Set-AzSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="fe104-131">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="fe104-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 97373d35cee4efb80ca2953c0085fe6b153ea138
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620477"
---
# <span data-ttu-id="53068-101">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="53068-101">Get-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="53068-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53068-102">SYNOPSIS</span></span>
<span data-ttu-id="53068-103">取得資料庫地域備份原則。</span><span class="sxs-lookup"><span data-stu-id="53068-103">Gets a database geo backup policy.</span></span>

## <span data-ttu-id="53068-104">句法</span><span class="sxs-lookup"><span data-stu-id="53068-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53068-105">說明</span><span class="sxs-lookup"><span data-stu-id="53068-105">DESCRIPTION</span></span>
<span data-ttu-id="53068-106">**AzSqlDatabaseGeoBackupPolicy** Cmdlet 會取得已登錄至此資料庫的 geo 備份原則。</span><span class="sxs-lookup"><span data-stu-id="53068-106">The **Get-AzSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="53068-107">這是用來定義備份儲存原則的 Azure 備份資源。</span><span class="sxs-lookup"><span data-stu-id="53068-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="53068-108">示例</span><span class="sxs-lookup"><span data-stu-id="53068-108">EXAMPLES</span></span>

## <span data-ttu-id="53068-109">參數</span><span class="sxs-lookup"><span data-stu-id="53068-109">PARAMETERS</span></span>

### <span data-ttu-id="53068-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="53068-110">-DatabaseName</span></span>
<span data-ttu-id="53068-111">指定此 Cmdlet 取得 geo 備份原則之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="53068-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

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

### <span data-ttu-id="53068-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53068-112">-DefaultProfile</span></span>
<span data-ttu-id="53068-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="53068-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53068-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53068-114">-ResourceGroupName</span></span>
<span data-ttu-id="53068-115">指定包含此資料庫之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="53068-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="53068-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="53068-116">-ServerName</span></span>
<span data-ttu-id="53068-117">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="53068-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="53068-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53068-118">CommonParameters</span></span>
<span data-ttu-id="53068-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53068-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53068-120">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="53068-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53068-121">輸入</span><span class="sxs-lookup"><span data-stu-id="53068-121">INPUTS</span></span>

### <span data-ttu-id="53068-122">System.object</span><span class="sxs-lookup"><span data-stu-id="53068-122">System.String</span></span>

## <span data-ttu-id="53068-123">輸出</span><span class="sxs-lookup"><span data-stu-id="53068-123">OUTPUTS</span></span>

### <span data-ttu-id="53068-124">AzureSqlDatabaseGeoBackupPolicyModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="53068-124">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="53068-125">筆記</span><span class="sxs-lookup"><span data-stu-id="53068-125">NOTES</span></span>

## <span data-ttu-id="53068-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="53068-126">RELATED LINKS</span></span>

[<span data-ttu-id="53068-127">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="53068-127">Set-AzSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="53068-128">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="53068-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

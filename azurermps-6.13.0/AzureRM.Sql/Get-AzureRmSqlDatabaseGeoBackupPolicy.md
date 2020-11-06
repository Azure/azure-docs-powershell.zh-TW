---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: f17619fcdb16574a1fc755843e0084200031085d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451016"
---
# <span data-ttu-id="40938-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="40938-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="40938-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40938-102">SYNOPSIS</span></span>
<span data-ttu-id="40938-103">取得資料庫地域備份原則。</span><span class="sxs-lookup"><span data-stu-id="40938-103">Gets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40938-104">句法</span><span class="sxs-lookup"><span data-stu-id="40938-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40938-105">說明</span><span class="sxs-lookup"><span data-stu-id="40938-105">DESCRIPTION</span></span>
<span data-ttu-id="40938-106">**AzureRmSqlDatabaseGeoBackupPolicy** Cmdlet 會取得已登錄至此資料庫的 geo 備份原則。</span><span class="sxs-lookup"><span data-stu-id="40938-106">The **Get-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="40938-107">這是用來定義備份儲存原則的 Azure 備份資源。</span><span class="sxs-lookup"><span data-stu-id="40938-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="40938-108">示例</span><span class="sxs-lookup"><span data-stu-id="40938-108">EXAMPLES</span></span>

## <span data-ttu-id="40938-109">參數</span><span class="sxs-lookup"><span data-stu-id="40938-109">PARAMETERS</span></span>

### <span data-ttu-id="40938-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="40938-110">-DatabaseName</span></span>
<span data-ttu-id="40938-111">指定此 Cmdlet 取得 geo 備份原則之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="40938-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

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

### <span data-ttu-id="40938-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40938-112">-DefaultProfile</span></span>
<span data-ttu-id="40938-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="40938-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40938-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40938-114">-ResourceGroupName</span></span>
<span data-ttu-id="40938-115">指定包含此資料庫之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="40938-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="40938-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="40938-116">-ServerName</span></span>
<span data-ttu-id="40938-117">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="40938-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="40938-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40938-118">CommonParameters</span></span>
<span data-ttu-id="40938-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40938-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40938-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40938-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40938-121">輸入</span><span class="sxs-lookup"><span data-stu-id="40938-121">INPUTS</span></span>

### <span data-ttu-id="40938-122">System.object</span><span class="sxs-lookup"><span data-stu-id="40938-122">System.String</span></span>

## <span data-ttu-id="40938-123">輸出</span><span class="sxs-lookup"><span data-stu-id="40938-123">OUTPUTS</span></span>

### <span data-ttu-id="40938-124">AzureSqlDatabaseGeoBackupPolicyModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="40938-124">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="40938-125">筆記</span><span class="sxs-lookup"><span data-stu-id="40938-125">NOTES</span></span>

## <span data-ttu-id="40938-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="40938-126">RELATED LINKS</span></span>

[<span data-ttu-id="40938-127">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="40938-127">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="40938-128">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="40938-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

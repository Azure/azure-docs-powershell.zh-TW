---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: cfd8df9bc329ef252c28ef826b1ba68a1946bab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905581"
---
# <span data-ttu-id="37402-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="37402-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="37402-102">簡介</span><span class="sxs-lookup"><span data-stu-id="37402-102">SYNOPSIS</span></span>
<span data-ttu-id="37402-103">建立一個新的連接資訊物件，指定連接的伺服器類型和名稱。</span><span class="sxs-lookup"><span data-stu-id="37402-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="37402-104">語法</span><span class="sxs-lookup"><span data-stu-id="37402-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37402-105">描述</span><span class="sxs-lookup"><span data-stu-id="37402-105">DESCRIPTION</span></span>
<span data-ttu-id="37402-106">Cmdlet New-AzDataMigrationConnectionInfo會建立一個新的連接資訊物件，指定連接的伺服器類型。</span><span class="sxs-lookup"><span data-stu-id="37402-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="37402-107">例子</span><span class="sxs-lookup"><span data-stu-id="37402-107">EXAMPLES</span></span>

### <span data-ttu-id="37402-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="37402-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="37402-109">上述範例會建立提供 SQL 為 ServerType 參數的新連接資訊物件。</span><span class="sxs-lookup"><span data-stu-id="37402-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="37402-110">參數</span><span class="sxs-lookup"><span data-stu-id="37402-110">PARAMETERS</span></span>

### <span data-ttu-id="37402-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37402-111">-DefaultProfile</span></span>
<span data-ttu-id="37402-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="37402-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37402-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="37402-113">-ServerType</span></span>
<span data-ttu-id="37402-114">描述要連接之伺服器類型的 Enum。</span><span class="sxs-lookup"><span data-stu-id="37402-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="37402-115">目前支援的值為 SQL Server 的 SQL、Azure SQL Managed 實例、MongoDb、集中處理和 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="37402-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL, MongoDb, SQLMI

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37402-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37402-116">CommonParameters</span></span>
<span data-ttu-id="37402-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="37402-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37402-118">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="37402-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37402-119">輸入</span><span class="sxs-lookup"><span data-stu-id="37402-119">INPUTS</span></span>

### <span data-ttu-id="37402-120">沒有</span><span class="sxs-lookup"><span data-stu-id="37402-120">None</span></span>

## <span data-ttu-id="37402-121">輸出</span><span class="sxs-lookup"><span data-stu-id="37402-121">OUTPUTS</span></span>

### <span data-ttu-id="37402-122">Microsoft.Azure.management.DataMigration.models.ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="37402-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="37402-123">筆記</span><span class="sxs-lookup"><span data-stu-id="37402-123">NOTES</span></span>

## <span data-ttu-id="37402-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="37402-124">RELATED LINKS</span></span>

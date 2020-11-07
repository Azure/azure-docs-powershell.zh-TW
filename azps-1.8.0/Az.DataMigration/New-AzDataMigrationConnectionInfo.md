---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: 871b6c09832e4b857a616c93cc33102f2dd0ad8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787889"
---
# <span data-ttu-id="37f42-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="37f42-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="37f42-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37f42-102">SYNOPSIS</span></span>
<span data-ttu-id="37f42-103">建立新的連線資訊物件，以指定連線的伺服器類型和名稱。</span><span class="sxs-lookup"><span data-stu-id="37f42-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="37f42-104">句法</span><span class="sxs-lookup"><span data-stu-id="37f42-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37f42-105">說明</span><span class="sxs-lookup"><span data-stu-id="37f42-105">DESCRIPTION</span></span>
<span data-ttu-id="37f42-106">New-AzDataMigrationConnectionInfo Cmdlet 會建立新的連接資訊物件，以指定連線的伺服器類型。</span><span class="sxs-lookup"><span data-stu-id="37f42-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="37f42-107">示例</span><span class="sxs-lookup"><span data-stu-id="37f42-107">EXAMPLES</span></span>

### <span data-ttu-id="37f42-108">範例1</span><span class="sxs-lookup"><span data-stu-id="37f42-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="37f42-109">前面的範例會建立新的連線資訊物件，提供 SQL 作為 ServerType 參數。</span><span class="sxs-lookup"><span data-stu-id="37f42-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="37f42-110">參數</span><span class="sxs-lookup"><span data-stu-id="37f42-110">PARAMETERS</span></span>

### <span data-ttu-id="37f42-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37f42-111">-DefaultProfile</span></span>
<span data-ttu-id="37f42-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37f42-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37f42-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="37f42-113">-ServerType</span></span>
<span data-ttu-id="37f42-114">列舉描述要連線的伺服器類型的列舉。</span><span class="sxs-lookup"><span data-stu-id="37f42-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="37f42-115">目前支援的值為 SQL Server、Azure SQL Managed Instance、MongoDb、CosmosDb 和 Azure SQL Database 的 SQL。</span><span class="sxs-lookup"><span data-stu-id="37f42-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

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

### <span data-ttu-id="37f42-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37f42-116">CommonParameters</span></span>
<span data-ttu-id="37f42-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37f42-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37f42-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="37f42-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37f42-119">輸入</span><span class="sxs-lookup"><span data-stu-id="37f42-119">INPUTS</span></span>

### <span data-ttu-id="37f42-120">所有</span><span class="sxs-lookup"><span data-stu-id="37f42-120">None</span></span>

## <span data-ttu-id="37f42-121">輸出</span><span class="sxs-lookup"><span data-stu-id="37f42-121">OUTPUTS</span></span>

### <span data-ttu-id="37f42-122">ConnectionInfo 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="37f42-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="37f42-123">筆記</span><span class="sxs-lookup"><span data-stu-id="37f42-123">NOTES</span></span>

## <span data-ttu-id="37f42-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="37f42-124">RELATED LINKS</span></span>

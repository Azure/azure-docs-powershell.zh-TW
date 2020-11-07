---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: 77559f5858c26d665d062f822a5c65258625bb14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624398"
---
# <span data-ttu-id="f4457-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="f4457-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="f4457-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4457-102">SYNOPSIS</span></span>
<span data-ttu-id="f4457-103">建立新的連線資訊物件，以指定連線的伺服器類型和名稱。</span><span class="sxs-lookup"><span data-stu-id="f4457-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4457-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4457-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4457-105">說明</span><span class="sxs-lookup"><span data-stu-id="f4457-105">DESCRIPTION</span></span>
<span data-ttu-id="f4457-106">New-AzureRmDataMigrationConnectionInfo Cmdlet 會建立新的連接資訊物件，以指定連線的伺服器類型。</span><span class="sxs-lookup"><span data-stu-id="f4457-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="f4457-107">示例</span><span class="sxs-lookup"><span data-stu-id="f4457-107">EXAMPLES</span></span>

### <span data-ttu-id="f4457-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f4457-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="f4457-109">前面的範例會建立新的連線資訊物件，提供 SQL 作為 ServerType 參數。</span><span class="sxs-lookup"><span data-stu-id="f4457-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="f4457-110">參數</span><span class="sxs-lookup"><span data-stu-id="f4457-110">PARAMETERS</span></span>

### <span data-ttu-id="f4457-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4457-111">-DefaultProfile</span></span>
<span data-ttu-id="f4457-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4457-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4457-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="f4457-113">-ServerType</span></span>
<span data-ttu-id="f4457-114">列舉描述要連線的伺服器類型的列舉。</span><span class="sxs-lookup"><span data-stu-id="f4457-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="f4457-115">目前支援的值是 sql Server、Azure SQL Managed 實例和 Azure SQL 資料庫的 SQL。</span><span class="sxs-lookup"><span data-stu-id="f4457-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4457-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4457-116">CommonParameters</span></span>
<span data-ttu-id="f4457-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4457-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4457-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f4457-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4457-119">輸入</span><span class="sxs-lookup"><span data-stu-id="f4457-119">INPUTS</span></span>

### <span data-ttu-id="f4457-120">所有</span><span class="sxs-lookup"><span data-stu-id="f4457-120">None</span></span>

## <span data-ttu-id="f4457-121">輸出</span><span class="sxs-lookup"><span data-stu-id="f4457-121">OUTPUTS</span></span>

### <span data-ttu-id="f4457-122">ConnectionInfo 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="f4457-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="f4457-123">筆記</span><span class="sxs-lookup"><span data-stu-id="f4457-123">NOTES</span></span>

## <span data-ttu-id="f4457-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4457-124">RELATED LINKS</span></span>

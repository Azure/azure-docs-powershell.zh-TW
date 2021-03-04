---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: b30f9fd4b29a1be064a9e0925e39faa71485b58f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905566"
---
# <span data-ttu-id="6bc2a-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="6bc2a-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="6bc2a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6bc2a-102">SYNOPSIS</span></span>
<span data-ttu-id="6bc2a-103">為 Azure 資料庫移移服務建立 FileShare 物件，指定要執行源資料庫備份的局網共用。</span><span class="sxs-lookup"><span data-stu-id="6bc2a-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="6bc2a-104">語法</span><span class="sxs-lookup"><span data-stu-id="6bc2a-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bc2a-105">描述</span><span class="sxs-lookup"><span data-stu-id="6bc2a-105">DESCRIPTION</span></span>
<span data-ttu-id="6bc2a-106">此New-AzDataMigrationFileShare Cmdlet 會建立 FileShare 物件，指定 Azure 資料庫移轉服務可進行源資料庫備份的局網共用。</span><span class="sxs-lookup"><span data-stu-id="6bc2a-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="6bc2a-107">執行來源 SQL Server 實例的服務帳戶必須擁有此網路共用上的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="6bc2a-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="6bc2a-108">例子</span><span class="sxs-lookup"><span data-stu-id="6bc2a-108">EXAMPLES</span></span>

### <span data-ttu-id="6bc2a-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="6bc2a-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="6bc2a-110">參數</span><span class="sxs-lookup"><span data-stu-id="6bc2a-110">PARAMETERS</span></span>

### <span data-ttu-id="6bc2a-111">-認證</span><span class="sxs-lookup"><span data-stu-id="6bc2a-111">-Credential</span></span>
<span data-ttu-id="6bc2a-112">存取檔案共用之認證。</span><span class="sxs-lookup"><span data-stu-id="6bc2a-112">Credentials to access the file share.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bc2a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bc2a-113">-DefaultProfile</span></span>
<span data-ttu-id="6bc2a-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6bc2a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bc2a-115">-路徑</span><span class="sxs-lookup"><span data-stu-id="6bc2a-115">-Path</span></span>
<span data-ttu-id="6bc2a-116">檔案共用路徑。</span><span class="sxs-lookup"><span data-stu-id="6bc2a-116">File share path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bc2a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bc2a-117">CommonParameters</span></span>
<span data-ttu-id="6bc2a-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6bc2a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bc2a-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6bc2a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bc2a-120">輸入</span><span class="sxs-lookup"><span data-stu-id="6bc2a-120">INPUTS</span></span>

### <span data-ttu-id="6bc2a-121">沒有</span><span class="sxs-lookup"><span data-stu-id="6bc2a-121">None</span></span>

## <span data-ttu-id="6bc2a-122">輸出</span><span class="sxs-lookup"><span data-stu-id="6bc2a-122">OUTPUTS</span></span>

### <span data-ttu-id="6bc2a-123">Microsoft.Azure.management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="6bc2a-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="6bc2a-124">筆記</span><span class="sxs-lookup"><span data-stu-id="6bc2a-124">NOTES</span></span>

## <span data-ttu-id="6bc2a-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="6bc2a-125">RELATED LINKS</span></span>

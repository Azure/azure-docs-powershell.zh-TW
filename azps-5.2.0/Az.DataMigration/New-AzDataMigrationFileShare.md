---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: c0b88b60127162d895eeb642269240b699836d4f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274543"
---
# <span data-ttu-id="45b12-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="45b12-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="45b12-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45b12-102">SYNOPSIS</span></span>
<span data-ttu-id="45b12-103">建立 Azure Database 遷移服務的 [資料庫共用] 物件，該物件會指定要進行來源資料庫備份的本機網路共用。</span><span class="sxs-lookup"><span data-stu-id="45b12-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="45b12-104">句法</span><span class="sxs-lookup"><span data-stu-id="45b12-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45b12-105">說明</span><span class="sxs-lookup"><span data-stu-id="45b12-105">DESCRIPTION</span></span>
<span data-ttu-id="45b12-106">New-AzDataMigrationFileShare Cmdlet 會建立一個可共用的物件，以指定可供 Azure 資料庫移轉服務進行源資料庫備份的 [本機網路共用]。</span><span class="sxs-lookup"><span data-stu-id="45b12-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="45b12-107">執行源 SQL Server 實例的服務帳戶必須擁有此網路共用的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="45b12-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="45b12-108">示例</span><span class="sxs-lookup"><span data-stu-id="45b12-108">EXAMPLES</span></span>

### <span data-ttu-id="45b12-109">範例1</span><span class="sxs-lookup"><span data-stu-id="45b12-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="45b12-110">參數</span><span class="sxs-lookup"><span data-stu-id="45b12-110">PARAMETERS</span></span>

### <span data-ttu-id="45b12-111">-認證</span><span class="sxs-lookup"><span data-stu-id="45b12-111">-Credential</span></span>
<span data-ttu-id="45b12-112">存取檔案共用的認證。</span><span class="sxs-lookup"><span data-stu-id="45b12-112">Credentials to access the file share.</span></span>

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

### <span data-ttu-id="45b12-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b12-113">-DefaultProfile</span></span>
<span data-ttu-id="45b12-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45b12-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45b12-115">-Path</span><span class="sxs-lookup"><span data-stu-id="45b12-115">-Path</span></span>
<span data-ttu-id="45b12-116">檔案共用路徑。</span><span class="sxs-lookup"><span data-stu-id="45b12-116">File share path.</span></span>

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

### <span data-ttu-id="45b12-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b12-117">CommonParameters</span></span>
<span data-ttu-id="45b12-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45b12-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b12-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45b12-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b12-120">輸入</span><span class="sxs-lookup"><span data-stu-id="45b12-120">INPUTS</span></span>

### <span data-ttu-id="45b12-121">所有</span><span class="sxs-lookup"><span data-stu-id="45b12-121">None</span></span>

## <span data-ttu-id="45b12-122">輸出</span><span class="sxs-lookup"><span data-stu-id="45b12-122">OUTPUTS</span></span>

### <span data-ttu-id="45b12-123">MigrateSqlServerSqlDbDatabaseInput 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="45b12-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="45b12-124">筆記</span><span class="sxs-lookup"><span data-stu-id="45b12-124">NOTES</span></span>

## <span data-ttu-id="45b12-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="45b12-125">RELATED LINKS</span></span>

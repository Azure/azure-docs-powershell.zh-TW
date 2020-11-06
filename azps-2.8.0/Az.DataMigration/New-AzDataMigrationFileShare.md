---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: cc09f7ac0a5f4378c65700cd9681118200d629ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612716"
---
# <span data-ttu-id="20d6c-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="20d6c-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="20d6c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="20d6c-103">建立 Azure Database 遷移服務的 [資料庫共用] 物件，該物件會指定要進行來源資料庫備份的本機網路共用。</span><span class="sxs-lookup"><span data-stu-id="20d6c-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="20d6c-104">句法</span><span class="sxs-lookup"><span data-stu-id="20d6c-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20d6c-105">說明</span><span class="sxs-lookup"><span data-stu-id="20d6c-105">DESCRIPTION</span></span>
<span data-ttu-id="20d6c-106">New-AzDataMigrationFileShare Cmdlet 會建立一個可共用的物件，以指定可供 Azure 資料庫移轉服務進行源資料庫備份的 [本機網路共用]。</span><span class="sxs-lookup"><span data-stu-id="20d6c-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="20d6c-107">執行源 SQL Server 實例的服務帳戶必須擁有此網路共用的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="20d6c-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="20d6c-108">示例</span><span class="sxs-lookup"><span data-stu-id="20d6c-108">EXAMPLES</span></span>

### <span data-ttu-id="20d6c-109">範例1</span><span class="sxs-lookup"><span data-stu-id="20d6c-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="20d6c-110">參數</span><span class="sxs-lookup"><span data-stu-id="20d6c-110">PARAMETERS</span></span>

### <span data-ttu-id="20d6c-111">-認證</span><span class="sxs-lookup"><span data-stu-id="20d6c-111">-Credential</span></span>
<span data-ttu-id="20d6c-112">存取檔案共用的認證。</span><span class="sxs-lookup"><span data-stu-id="20d6c-112">Credentials to access the file share.</span></span>

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

### <span data-ttu-id="20d6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20d6c-113">-DefaultProfile</span></span>
<span data-ttu-id="20d6c-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="20d6c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20d6c-115">-Path</span><span class="sxs-lookup"><span data-stu-id="20d6c-115">-Path</span></span>
<span data-ttu-id="20d6c-116">檔案共用路徑。</span><span class="sxs-lookup"><span data-stu-id="20d6c-116">File share path.</span></span>

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

### <span data-ttu-id="20d6c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d6c-117">CommonParameters</span></span>
<span data-ttu-id="20d6c-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20d6c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d6c-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="20d6c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d6c-120">輸入</span><span class="sxs-lookup"><span data-stu-id="20d6c-120">INPUTS</span></span>

### <span data-ttu-id="20d6c-121">所有</span><span class="sxs-lookup"><span data-stu-id="20d6c-121">None</span></span>

## <span data-ttu-id="20d6c-122">輸出</span><span class="sxs-lookup"><span data-stu-id="20d6c-122">OUTPUTS</span></span>

### <span data-ttu-id="20d6c-123">MigrateSqlServerSqlDbDatabaseInput 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="20d6c-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="20d6c-124">筆記</span><span class="sxs-lookup"><span data-stu-id="20d6c-124">NOTES</span></span>

## <span data-ttu-id="20d6c-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="20d6c-125">RELATED LINKS</span></span>